---
title: 'Q # 문 | Microsoft Docs'
description: 'Q # 문'
author: QuantumWriter
uid: microsoft.quantum.language.statements
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 5bcbee868c76aaf53d0b7969e6e634da62689aaa
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184868"
---
# <a name="statements-and-other-constructs"></a>문 및 기타 구문

## <a name="comments"></a>의견

주석은 두 개의 슬래시, `//`로 시작 하 고 줄의 끝까지 계속 됩니다.
설명은 Q # 소스 파일의 어디에 나 나타날 수 있습니다.

### <a name="documentation-comments"></a>문서 주석

세 개의 슬래시 (`///`)로 시작 하는 주석은 네임 스페이스, 작업, 특수화, 함수 또는 형식 정의 바로 앞에 표시 될 때 컴파일러에서 특수 하 게 처리 됩니다.
이 경우 다른 .NET 언어의 경우와 같이 정의 된 호출 가능 또는 사용자 정의 형식에 대 한 설명서로 해당 내용이 사용 됩니다.

`///` 주석 내에서 API 설명서의 일부로 표시 되는 텍스트는 특수 하 게 명명 된 헤더로 표시 되는 설명서의 여러 부분을 사용 하 여 [Markdown](https://daringfireball.net/projects/markdown/syntax)로 형식이 지정 됩니다.
Markdown에 대 한 확장으로, Q #의 작업, 함수 및 사용자 정의 형식에 대 한 상호 참조는 참조 되는 코드 개체의 정규화 된 이름으로 대체 되는 `@"<ref target>"``<ref target>`을 사용 하 여 포함할 수 있습니다.
선택적으로 설명서 엔진에서 추가 Markdown 확장을 지원할 수도 있습니다.

다음은 그 예입니다.

```qsharp
/// # Summary
/// Given an operation and a target for that operation,
/// applies the given operation twice.
///
/// # Input
/// ## op
/// The operation to be applied.
/// ## target
/// The target to which the operation is to be applied.
///
/// # Type Parameters
/// ## 'T
/// The type expected by the given operation as its input.
///
/// # Example
/// ```Q#
/// // Should be equivalent to the identity.
/// ApplyTwice(H, qubit);
/// ```
///
/// # See Also
/// - Microsoft.Quantum.Intrinsic.H
operation ApplyTwice<'T>(op : ('T => Unit), target : 'T) : Unit
{
    op(target);
    op(target);
}
```

다음 이름은 문서 주석 헤더로 인식 됩니다.

- **요약**: 함수 또는 작업의 동작에 대 한 간략 한 요약 또는 형식의 용도입니다. 요약의 첫 번째 단락은 가리키기 정보에 사용 됩니다. 일반 텍스트 여야 합니다.
- **설명**: 함수 또는 작업의 동작에 대 한 설명 또는 형식의 용도에 대 한 설명입니다. 요약 및 설명은 함수, 작업 또는 형식에 대해 생성 된 설명서 파일을 구성 하기 위해 연결 됩니다.
  설명에는 인라인 LaTeX 형식의 기호 및 수식이 포함 될 수 있습니다.
- **Input**: 작업 또는 함수에 대 한 입력 튜플의 설명입니다.
  입력 튜플의 각 개별 요소를 나타내는 추가 Markdown 하위 섹션이 포함 될 수 있습니다.
- **Output**: 작업 또는 함수에서 반환 된 튜플에 대 한 설명입니다.
- **형식 매개 변수**: 각 제네릭 형식 매개 변수에 대 한 추가 하위 섹션을 하나씩 포함 하는 빈 섹션입니다.
- **예**: 사용 중인 작업, 함수 또는 형식에 대 한 간단한 예입니다.
- **주의**: 작업, 함수 또는 형식에 대 한 몇 가지 측면을 설명 하는 기타 prose.
- **참고**항목: 관련 된 함수, 작업 또는 사용자 정의 형식을 나타내는 정규화 된 이름 목록입니다.
- **참조**: 문서화 되는 항목에 대 한 참조 및 인용의 목록입니다.

## <a name="namespaces"></a>네임스페이스

모든 Q # 작업, 함수 및 사용자 정의 형식은 네임 스페이스 내에서 정의 됩니다.
Q #은 다른 .NET 언어로 이름을 지정 하는 것과 동일한 규칙을 따릅니다.
그러나 Q #에서는 네임 스페이스에 대 한 상대 참조를 지원 하지 않습니다.
즉, `a.b` 네임 스페이스를 연 경우 `c.d` 작업 이름에 대 한 참조는 전체 이름이 `a.b.c.d`된 작업으로 확인 되지 않습니다.

네임 스페이스 블록 내에서 `open` 지시어를 사용 하 여 특정 네임 스페이스에서 선언 된 모든 형식 및 callables을 가져와서 정규화 되지 않은 이름으로 참조할 수 있습니다. 필요에 따라 열린 네임 스페이스의 짧은 이름을 정의 하 여 해당 네임 스페이스의 모든 요소를 정의 된 약식 이름으로 정규화 하 고 필요에 따라 정규화 할 수 있습니다. `open` 지시문은 파일 내의 전체 네임 스페이스 블록에 적용 됩니다.

현재 네임 스페이스에서 열려 있지 않은 다른 네임 스페이스에 정의 된 형식 또는 호출 가능 이름은 정규화 된 이름으로 참조 되어야 합니다.
예를 들어 `X.Y` 네임 스페이스가 현재 블록에서 아직 열려 있지 않은 경우 `X.Y` 네임 스페이스에 `Op` 이름이 지정 된 작업은 정규화 된 이름 `X.Y.Op`에서 참조 해야 합니다. 위에서 언급 한 대로 `X` 네임 스페이스를 연 경우에도 `Y.Op`작업을 참조할 수 없습니다.
`X.Y`의 약식 `Z` 이름이 해당 네임 스페이스 및 파일에 정의 된 경우 `Op`를 `Z.Op`로 참조 해야 합니다. 

```qsharp
namespace NS {

    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace
}
```

일반적으로 `open` 지시어를 사용 하 여 네임 스페이스를 포함 하는 것이 좋습니다.
두 네임 스페이스가 같은 이름을 사용 하 여 구문을 정의 하 고 현재 소스가 양쪽에서 구문을 사용 하는 경우 정규화 된 이름을 사용 해야 합니다.

## <a name="formatting"></a>서식 지정

대부분의 Q # 문과 지시문은 종료 세미콜론 (`;`)으로 끝납니다.
문 및 선언 (예: 문 블록으로 끝나는 `for` 및 `operation`)에는 종료 세미콜론이 필요 하지 않습니다.
각 문 설명에는 종료 세미콜론이 필요한 지 여부에 대 한 설명이 나와 있습니다.

식, 선언 및 지시문과 같은 문은 여러 줄에 걸쳐 분할 될 수 있습니다.
한 줄에 문이 여러 개 있는 것은 피해 야 합니다.

## <a name="statement-blocks"></a>문 블록

Q # 문은 문 블록으로 그룹화 됩니다.
문 블록은 여는 `{` 시작 하 고 닫는 `}`로 끝납니다.

다른 블록 내에 어휘를 싸인 문 블록은 포함 하는 블록의 하위 블록으로 간주 됩니다. 포함 및 하위 블록은 외부 및 내부 블록이 라고도 합니다.

## <a name="symbol-binding-and-assignment"></a>기호 바인딩 및 할당

Q #은 변경 가능 하 고 변경할 수 없는 기호를 구분 합니다.
일반적으로 컴파일러에서 더 많은 최적화를 수행할 수 있기 때문에 변경할 수 없는 기호를 사용 하는 것이 좋습니다.

바인딩의 왼쪽은 기호 튜플 및 식의 오른쪽으로 구성 되어 있습니다.

모든 Q # 형식은 값 형식이 며,이 경우에는 값이 기호에 바인딩되거나 기호가 바인딩 되었을 때 "복사"가 생성 됩니다. 즉, Q #의 동작은 할당 시 복사본이 생성 된 경우와 동일 합니다. 특히 배열도 포함 됩니다. 물론 관련 된 부분만 실제로 필요에 따라 다시 생성 됩니다. 

### <a name="tuple-deconstruction"></a>튜플 분해

바인딩의 오른쪽이 튜플이 면 할당 시 해당 튜플을 분해 수 있습니다.
이러한 분해에는 중첩 된 튜플이 포함 될 수 있으며, 모든 전체 또는 부분 분해은 오른쪽에 있는 튜플의 모양이 기호 튜플의 셰이프와 호환 되는 한 유효 합니다.
`=`의 오른쪽이 튜플 값 식인 경우에도 특히 튜플 분해 사용할 수 있습니다.

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

### <a name="immutable-symbols"></a>변경할 수 없는 기호

변경할 수 없는 기호는 `let` 문을 사용 하 여 바인딩됩니다.
이는와 C#같은 언어의 변수 선언 및 초기화와 거의 동일 합니다. 단,이 경우는 Q # 기호가 바인딩된 후에는 변경할 수 없습니다. `let` 바인딩은 변경할 수 없습니다.

변경할 수 없는 바인딩은 키워드 `let`로 구성 된 다음 기호 또는 기호 튜플, 등호 `=`, 기호를 바인딩할 식, 종료 세미콜론으로 구성 됩니다.
바인딩된 기호의 형식은 오른쪽에 있는 식을 기반으로 유추 됩니다.

### <a name="mutable-symbols"></a>변경 가능한 기호

변경 가능한 기호는 `mutable` 문을 사용 하 여 정의 및 초기화 됩니다.
`mutable` 문의 일부로 선언 되 고 바인딩된 기호는 코드에서 나중에 다른 값으로 다시 바인딩할 수 있습니다. 

변경 가능한 바인딩 문은 `mutable`키워드와 기호 또는 기호 튜플, 등호 `=`, 기호를 바인딩할 식, 종료 세미콜론으로 구성 됩니다.
바인딩된 기호의 형식은 오른쪽에 있는 식을 기반으로 유추 됩니다. 기호를 코드에서 나중에 다시 바인딩하는 경우 해당 형식은 변경 되지 않으며 바인딩된 값은 해당 형식과 호환 되어야 합니다.

### <a name="rebinding-of-mutable-symbols"></a>변경 가능한 기호 리바인딩

변경 가능한 변수는 `set` 문을 사용 하 여 바인딩할 수 있습니다.
이러한 리바인딩은 키워드 `set`로 구성 된 다음 기호 또는 기호 튜플, 등호 `=`, 기호를에 다시 바인딩하는 식 및 종료 세미콜론으로 구성 됩니다.
값은 바인딩되는 기호의 형식과 호환 되어야 합니다 (s).

#### <a name="apply-and-reassign-statement"></a>적용 및 재할당 문

적용 및 재할당 문으로 참조 하는 특정 종류의 set 문은 오른쪽이 이항 연산자의 응용 프로그램으로 구성 되 고 결과가 연산자의 왼쪽 인수에 다시 바인딩 되는 경우 편리 하 게 연결 하는 방법을 제공 합니다. 예를 들면 다음과 같습니다.
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
`for` 루프의 각 반복에서 카운터 `counter`의 값을 증가 시킵니다. 위의 코드는와 동일 합니다. 
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```
왼쪽의 형식이 식 형식과 일치 하는 모든 이항 연산자에 대해 비슷한 문을 사용할 수 있습니다. 예를 들어 다음과 같이 값을 누적 하는 편리한 방법을 제공 합니다.
```qsharp
mutable results = new Result[0];
for (q in qubits) {
    set results += [M(q)];
    // ...
}
```
#### <a name="update-and-reassign-statement"></a>업데이트 및 재할당 문

오른쪽에 복사 및 업데이트 식에 대 한 유사한 연결이 있습니다. 마찬가지로, 사용자 정의 형식의 명명 된 항목 뿐만 아니라 배열 항목에 대해 업데이트 및 재할당 문이 존재 합니다.  

```qsharp
newtype Complex = (Re : Double, Im : Double);

function AddAll (reals : Double[], ims : Double[]) : Complex[] {
    mutable res = Complex(0.,0.);

    for (r in reals) {
        set res w/= Re <- res::Re + r; // update-and-reassign statement
    }
    for (i in ims) {
        set res w/= Im <- res::Im + i; // update-and-reassign statement
    }
    return res;
}
```

배열의 경우 표준 라이브러리에는 여러 일반적인 배열 초기화 및 조작 요구에 필요한 도구가 포함 되어 있으므로 첫 번째 위치의 배열 항목을 업데이트 하지 않아도 됩니다. 필요에 따라 업데이트 및 재할당 문이 대안을 제공 합니다.

```qsharp
operation RandomInts(maxInt : Int, nrSamples : Int) : Int[] {

    mutable samples = new Double[0];
    for (i in 1 .. nrSamples) {
        set samples += [RandomInt(maxInt)];
    }
    return samples;
}

operation SampleUniformDistr(nrSamples : Int, prec : Int) : Double[] {

    let normalization = 1. / IntAsDouble(prec);
    mutable samples = RandomInts(prec, nrSamples);
    
    for (i in IndexRange(samples) {
        let value = IntAsDouble(samples[i]);
        set samples w/= i <- normalization * value; // update-and-reassign statement
    }
}

```

> [!TIP]   
> <xref:microsoft.quantum.arrays>에서 제공 하는 도구를 활용 하 여 업데이트 및 재할당 문의 불필요 한 사용을 방지 합니다.

함수
```qsharp
function EmbedPauli (pauli : Pauli, location : Int, n : Int) : Pauli[]
{
    mutable pauliArray = new Pauli[n];
    for (index in 0 .. n - 1) {
        set pauliArray w/= index <- 
            index == location ? pauli | PauliI;
    }    
    return pauliArray;
}
```
예를 들어 `Microsoft.Quantum.Arrays`에서 `ConstantArray` 함수를 사용 하 고 복사 및 업데이트 식을 반환 하는 것은 간단 합니다.

```qsharp
function EmbedPauli (pauli : Pauli, i : Int, n : Int) : Pauli[] {
    return ConstantArray(n, PauliI) w/ i <- pauli;
}
```

### <a name="binding-scopes"></a>바인딩 범위

일반적으로 기호 바인딩은 범위를 벗어난 것으로,에서 발생 하는 문 블록의 끝에서 사용할 수 없게 됩니다.
이 규칙에는 다음과 같은 두 가지 예외가 있습니다.

- `for` 루프의 루프 변수 바인딩은 for 루프 본문의 범위 내에 있지만 루프가 끝난 후에는 범위 내에 있지 않습니다.
- `repeat`/`until` 루프 (본문, 테스트 및 픽스업)의 세 부분은 모두 단일 범위로 처리 되므로 본문에 바인딩된 기호는 테스트 및 픽스업에서 사용할 수 있습니다.

두 가지 유형의 루프 모두 루프를 통과 하는 각은 자체 범위에서 실행 되므로 이전 패스의 바인딩은 이후 단계에서 사용할 수 없습니다.

외부 블록의 기호 바인딩은 내부 블록에 의해 상속 됩니다.
기호는 블록 당 한 번만 바인딩할 수 있습니다. 범위 내에 있는 다른 기호와 동일한 이름을 사용 하 여 기호를 정의할 수 없습니다 ("숨김" 없음).
다음 시퀀스는 유효 합니다.

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

및

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
} else {
    ...
    let n = 8;
    ...             // n is 8
}
```

그러나이는 올바르지 않습니다.

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

다음과 같이 합니다.

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="control-flow"></a>제어 흐름

### <a name="for-loop"></a>For 루프

`for` 문은 정수 범위 또는 배열에 대 한 반복을 지원 합니다.
문은 키워드 `for`, 여는 괄호 `(`, 기호 또는 기호 튜플, 키워드 `in`, `Range` 또는 배열 형식의 식, 닫는 괄호 `)`및 문 블록으로 구성 됩니다.

문 블록 (루프의 본문)은 범위 또는 배열의 각 값에 바인딩된 정의 된 기호 (루프 변수)를 사용 하 여 반복적으로 실행 됩니다.
범위 식이 빈 범위 또는 배열로 계산 되는 경우 본문은 실행 되지 않습니다.
식은 루프를 시작 하기 전에 완전히 계산 되며 루프가 실행 되는 동안에는 변경 되지 않습니다.

선언 된 기호의 바인딩은 변경할 수 없으며 다른 변수 바인딩과 동일한 규칙을 따릅니다. 특히 루프 변수에 할당 될 때 배열에 대 한 반복의 배열 항목을 소멸 시킬 수 있습니다.

예를 들면 다음과 같습니다.

```qsharp
// ...
for (qb in qubits) { // qubits contains a Qubit[]
    H(qb);
}

mutable results = new (Int, Results)[Length(qubits)];
for (index in 0 .. Length(qubits) - 1) {
    set results w/= index <- (index, M(qubits[index]));
}

mutable accumulated = 0;
for ((index, measured) in results) {
    if (measured == One) {
        set accumulated += 1 <<< index;
    }
}
```

루프 변수는 루프 본문에 대 한 각 입구에 바인딩되고 본문의 끝에서 바인딩되지 않습니다.
특히 for 루프가 완료 된 후 루프 변수가 바인딩되지 않습니다.

### <a name="repeat-until-success-loop"></a>반복-성공 루프

`repeat` 문은 "성공 될 때까지 반복" 패턴을 지원 합니다.
`repeat`키워드, 문 블록 ( _루프_ 본문), 키워드 `until`, 부울 식, 종료 세미콜론 또는 키워드 `fixup` 뒤에 다른 문 블록 ( _픽스업_)이 오는 키워드로 구성 됩니다.
루프 본문, 조건 및 픽스업은 모두 단일 범위로 간주 되므로 본문에 바인딩된 기호는 조건 및 픽스업에서 사용할 수 있습니다.

```qsharp
mutable iter = 1;
repeat {
    ProbabilisticCircuit(qs);
    let success = ComputeSuccessIndicator(qs);
}
until (success || iter > maxIter)
fixup {
    iter += 1;
    ComputeCorrection(qs);
}
```

루프 본문이 실행 된 후 조건이 평가 됩니다.
조건이 true 이면 문이 완료 된 것입니다. 그렇지 않으면 픽스업이 실행 되 고 문이 루프 본문부터 다시 실행 됩니다.
픽스업 실행을 완료 하면 해당 문의 범위가 끝나기 때문에 본문 또는 픽스업 중에 만든 기호 바인딩을 후속 반복에서 사용할 수 없습니다.

예를 들어 다음 코드는 Hadamard 및 T 게이트를 사용 하 여 $V _3 = (\boldone + 2 i Z)/\sqrt{5}$ 중요 한 회전 게이트를 구현 하는 확률 회로입니다.
루프는 평균 8/5 회 반복에서 종료 됩니다.
자세한 내용은 [*반복-성공--성공: 단일 기능 비트 unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick 및 svore, 2014)의 비결 정적 분해를 참조 하세요.

```qsharp
using (anc = Qubit()) {
    repeat {
        H(anc);
        T(anc);
        CNOT(target,anc);
        H(anc);
        Adjoint T(anc);
        H(anc);
        T(anc);
        H(anc);
        CNOT(target,anc);
        T(anc);
        Z(target);
        H(anc);
        let result = M(anc);
    } until (result == Zero);
}
```

> [!TIP]   
> 함수 내에서-success 루프를 사용 하지 마십시오. 함수에서 루프를 통해 해당 기능을 제공 합니다. 

### <a name="while-loop"></a>While 루프

반복-성공 패턴에는 퀀텀 별 connotation가 있을 수 있습니다. 이러한 클래스는 특정 퀀텀 알고리즘 클래스에서 널리 사용 되므로 Q #에서 전용 언어 구문을 사용 합니다. 그러나 조건에 따라 중단 되 고 해당 실행 길이는 컴파일 시간에 알 수 없는 루프는 퀀텀 런타임에서 특히 주의 해 서 처리 해야 합니다. 반면에 함수 내에서의 사용은 기존 (비 퀀텀) 하드웨어에서 실행 되는 코드만 포함 하기 때문에 문제가 되지 않습니다. 

따라서 Q #은 함수 내 에서만 while 루프를 사용할 수 있도록 지원 합니다. `while` 문은 키워드 `while`, 여는 괄호 `(`, 조건 (예: 부울 식), 닫는 괄호 `)`및 문 블록으로 구성 됩니다.
문 블록 (루프의 본문)은 조건이 `true`로 평가 되는 동안 실행 됩니다.

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

### <a name="conditional-statement"></a>조건문

`if` 문은 조건부 실행을 지원 합니다.
키워드 `if`, 여는 괄호 `(`, 부울 식, 닫는 괄호 `)`및 문 블록 ( _then_ 블록)으로 구성 됩니다.
다음에는 여러 개의 else if 절이 올 수 있습니다. 각 절은 `elif`, 여는 괄호 `(`, 부울 식, 닫는 괄호 `)`및 문 블록 ( _else if_ 블록)으로 구성 됩니다.
마지막으로, 다른 문 블록 ( _else_ 블록) 뒤에 오는 키워드 `else` 구성 된 else 절을 사용 하 여 문을 선택적으로 완료할 수 있습니다.
조건이 평가 되 고 true 이면 then 블록이 실행 됩니다.
조건이 false 이면 첫 번째 else 조건이 평가 됩니다. true 이면 else 블록을 실행 합니다.
그렇지 않으면 두 번째 else if 블록이 테스트 되 고, 세 번째는 조건이 true 인 절이 발생 하거나 else if 절이 더 이상 없을 때까지 테스트 됩니다.
원래 if 조건과 모든 else if 절이 false 이면 else 블록이 제공 된 경우 실행 됩니다.

실행 되는 블록은 자체 범위에서 실행 됩니다.
Then, else-if 또는 else 블록 내부에서 만든 바인딩은 if 문의 끝 뒤에 표시 되지 않습니다.

예를 들면 다음과 같습니다.

```qsharp
if (result == One) {
    X(target);
} 
```

or

```qsharp
if (i == 1) {
    X(target);
} elif (i == 2) {
    Y(target);
} else {
    Z(target);
}
```

### <a name="return"></a>Return

Return 문은 작업 또는 함수의 실행을 종료 하 고 호출자에 게 값을 반환 합니다.
`return`키워드와 해당 형식의 식, 종료 세미콜론으로 구성 됩니다.

빈 튜플 `()`반환 하는 호출 가능에는 return 문이 필요 하지 않습니다.
초기 종료를 사용 하는 경우이 경우 `return ()` 사용할 수 있습니다.
다른 형식을 반환 하는 callables에는 최종 return 문이 필요 합니다.

작업 내에는 최대 개수의 return 문이 없습니다.
문이 블록 내의 return 문 뒤에 오는 경우 컴파일러는 경고를 생성할 수 있습니다.

예를 들면 다음과 같습니다.

```qsharp
return 1;
```

or

```qsharp
return ();
```

or

```qsharp
return (results, qubits);
```

### <a name="fail"></a>불합격

Fail 문은 작업 실행을 종료 하 고 호출자에 게 오류 값을 반환 합니다.
`fail`키워드와 문자열 및 종료 세미콜론으로 구성 됩니다.
문자열은 오류 메시지로 기존 드라이버에 반환 됩니다.

작업 내의 실패 문 수에 대 한 제한은 없습니다.
문이 블록 내의 fail 문 뒤에 오는 경우 컴파일러는 경고를 생성할 수 있습니다.

예를 들면 다음과 같습니다.

```qsharp
fail $"Impossible state reached";
```

or

```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="qubit-management"></a>이상 비트 관리

이러한 문은 함수 본문 내에서 허용 되지 않습니다.
작업 내 에서만 유효 합니다.

### <a name="clean-qubits"></a>정리 비트

`using` 문은 문 블록 중에 사용할 새 요소를 가져오는 데 사용 됩니다.
이는 계산 `Zero` 상태로 초기화 되도록 보장 됩니다.
이 요소는 문 블록의 끝에서 계산 `Zero` 상태 여야 합니다. 시뮬레이터는이를 적용 하는 것이 좋습니다.

문은 키워드 `using`으로 구성 되 고, 여는 괄호 `(`, 바인딩, 닫는 괄호 `)`및 해당 요소를 사용할 수 있는 문 블록으로 구성 됩니다.
바인딩은 `let` 문과 동일한 패턴을 따릅니다. 단일 기호 또는 기호의 튜플, 등호 `=`, 단일 값 또는 이니셜라이저의 일치 하는 튜플 중 하나입니다.
이니셜라이저는 `Qubit()`로 표시 되는 단일의 비트 또는 `Qubit[`, `Int` 식 및 `]`로 표시 되는 비트 배열로 사용할 수 있습니다.

예를 들면 다음과 같습니다.

```qsharp
using (q = Qubit()) {
    // ...
}
using ((ancilla, qubits) = (Qubit(), Qubit[bits * 2 + 3])) {
    // ...
}
```

### <a name="dirty-qubits"></a>더티 비트

`borrowing` 문은 임시 사용을 위해 필요한 비트를 가져오는 데 사용 됩니다. 문은 키워드 `borrowing`으로 구성 되 고, 여는 괄호 `(`, 바인딩, 닫는 괄호 `)`및 해당 요소를 사용할 수 있는 문 블록으로 구성 됩니다.
바인딩은 `using` 문에 있는 것과 동일한 패턴 및 규칙을 따릅니다.

예를 들면 다음과 같습니다.

```qsharp
borrowing (q = Qubit()) {
    // ...
}
borrowing ((ancilla, qubits) = (Qubit(), Qubit[bits * 2 + 3])) {
    // ...
}
```

인 중 한 비트는 알 수 없는 상태 이며 문 블록의 끝에 있는 범위를 벗어났습니다.
대출자는가 중에 있던 상태와 동일한 상태를 유지 하도록 커밋 합니다. 즉, 문 블록의 시작과 끝에 있는 상태는 동일 해야 합니다.
특히 borrowing 범위에는 측정값이 포함 되지 않아야 하는 일반적인 상태가 아닐 수도 있습니다. 

이러한 비트를 종종 "더티 ancilla" 이라고 합니다.
더티 ancilla use의 예제를 보려면 Toffoli 기반 모듈식 곱하기 (Haner, Roet2n Er 및 Svs2017) [*와 함께 + 2를 사용 하 여 팩터링*](https://arxiv.org/abs/1611.07995) 을 참조 하세요.

Borrowing를 사용 하는 경우 시스템은 먼저 사용 중인에서 요청을 채우려고 시도 하지만,이는 `borrowing` 문의 본문 중에는 액세스 되지 않습니다.
이러한 것이 충분 하지 않은 경우 요청을 완료 하기 위해 새 비트를 할당 합니다.

## <a name="conjugations"></a>변화

기존 비트와는 달리, 더 이상 필요 하지 않은 계산에 대 한 의도 하지 않은 영향이 있을 경우이를 무조건 다시 설정 하면 나머지 계산에 원치 않는 영향이 있을 수 있으므로 퀀텀 메모리 해제는 약간 더 복잡 합니다. 메모리를 해제 하기 전에 수행 된 계산을 적절히 "실행 취소" 하 여이를 방지할 수 있습니다. 따라서 퀀텀 컴퓨팅의 일반적인 패턴은 다음과 같습니다. 

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    outerOperation(target);
    innerOperation(target);
    Adjoint outerOperation(target);
}
```

: new: 0.9 릴리스부터는 위의 변환을 구현 하는 활용 문을 지원 합니다. 이 문을 사용 하 여 다음과 같은 방법으로 `ApplyWith` 작업을 구현할 수 있습니다.

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    within{ 
        outerOperation(target);
    }
    apply {
        innerOperation(target);
    }
}
```
이러한 활용은 외부 및 내부 변환을 작업으로 쉽게 사용할 수 없지만 대신 여러 문으로 구성 된 블록에서 더 편리 하 게 사용할 수 있는 경우 훨씬 더 유용 합니다. 

블록 내에서 정의 된 문에 대 한 역 변환은 컴파일러에서 자동으로 생성 되 고 적용 블록이 완료 된 후에 실행 됩니다. 블록 내에 사용 되는 변경할 수 있는 변수는 적용 블록에서 바인딩 가능 하지 않으므로 생성 된 변환은 블록 내에서 계산의 adjoint로 보장 됩니다. 

## <a name="expression-evaluation-statements"></a>식 계산 문

`Unit` 형식의 호출 식은 문으로 사용 될 수 있습니다.
이는 `Unit`을 반환 하는 stbits에서 작업을 호출할 때 주로 사용 됩니다 .이는 문의 목적이 암시적 퀀텀 상태를 수정 하는 것 이기 때문입니다.
식 계산 문에는 종료 세미콜론이 필요 합니다.

예를 들면 다음과 같습니다.

```qsharp
X(q);
CNOT(control, target);
Adjoint T(q);
```
