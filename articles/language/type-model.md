---
title: 'Q # 데이터 형식'
description: '기본 제공 형식, 배열, 튜플, 작업, 함수 및 사용자 정의 형식을 포함 하 여 Q # 프로그래밍 언어에서 사용 되는 다양 한 형식에 대해 알아봅니다.'
author: QuantumWriter
uid: microsoft.quantum.language.type-model
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 1fc4c0b3fed9277c7f9f3ac421330df03c1b30e4
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904658"
---
# <a name="the-type-model"></a>형식 모델

이 섹션에서는 Q # 형식 모델을 설명 하 고 형식을 지정 하 고 사용 하는 구문을 설명 합니다.
Q #은 *강력한* 형식의 언어 이므로 이러한 형식을 신중히 사용 하면 컴파일러가 컴파일 시간에 Q # 프로그램에 대 한 강력한 보증을 제공 하는 데 도움이 될 수 있습니다.

가장 강력한 보증을 제공 하기 위해 해당 변환을 표현 하는 함수에 대 한 호출을 사용 하 여 Q #의 형식 간 변환이 명시적 이어야 합니다. 이러한 여러 함수는 <xref:microsoft.quantum.convert> 네임 스페이스의 일부로 제공 됩니다.
반면에 호환 되는 형식으로의 수동 캐스팅은 암시적으로 수행 됩니다. 

Q #에서는 직접 사용할 수 있는 기본 형식과 다른 형식에서 새 형식을 생성 하는 다양 한 방법을 제공 합니다.
여기서는이 섹션의 나머지 부분에 대해 설명 합니다.

## <a name="primitive-types"></a>기본 유형

Q # 언어는 다른 형식을 구성할 수 있는 몇 가지 *기본 형식을*제공 합니다.

- `Int` 형식은 64 비트 부호 있는 정수를 나타냅니다 (예: `2`, `107`, `-5`).
- `BigInt` 형식은 임의 크기의 부호 있는 정수 (예: `2L`, `107L`, `-5L`)를 나타냅니다.
   이 형식은 .NET <xref:System.Numerics.BigInteger>을 기반으로 합니다.
   입력할.
- `Double` 형식은 배정밀도 부동 소수점 숫자를 나타냅니다 (예: `0.0`, `-1.3`, `4e-7`).
- `Bool` 형식은 `true` 하거나 `false`수 있는 부울 값을 나타냅니다.
- `Qubit` 형식은 퀀텀 비트 또는 비트를 나타냅니다.
   `Qubit`은 사용자에 게 불투명 합니다. 다른 작업에 전달 하는 것 외에도 가능한 유일한 작업은 id (같음)를 테스트 하는 것입니다.
   궁극적으로 `Qubit`s에 대 한 작업은 퀀텀 프로세서 또는 시뮬레이션에 대 한 기본 지침을 호출 하 여 구현 됩니다.
- `Pauli` 형식은 4 개의 단일 기능 비트 Pauli 연산자 중 하나를 나타냅니다.
   이 형식은 회전의 기본 연산을 나타내는 데 사용 되며 측정할 관찰 가능 개체를 지정 하는 데 사용 됩니다.
   이는 `PauliI`, `PauliX`, `PauliY`및 `PauliZ`의 네 가지 가능한 값이 있는 열거 형식으로, `Pauli`형식의 상수입니다.
- `Result` 형식은 측정 결과를 나타냅니다.
   이는 두 가지 가능한 값인 `One`와 `Zero``Result`형식의 상수인 열거형 형식입니다.
   `Zero` + 1 eigenvalue를 측정 했음을 나타냅니다. `One`-1 eigenvalue를 나타냅니다.
- `Range` 형식은 `start..step..stop`으로 표시 되는 정수 시퀀스를 나타냅니다. 여기서 단계는 옵션입니다. 
   이는 `start .. stop` `start..1..stop`에 해당 하며, 예를 들어 `1..2..7` $\{1, 3, 5, 7\}$ 시퀀스를 나타냅니다.
- `String` 형식은 사용자가 만든 후 불투명 한 유니코드 문자 시퀀스입니다.
  이 형식은 오류 또는 진단 이벤트의 경우 메시지를 기존 호스트에 보고 하는 데 사용 됩니다.
- `Unit` 형식은 하나의 값 `()`허용 하는 형식입니다. 
  이 형식은 Q # 함수 또는 연산이 정보를 반환 하지 않음을 나타내는 데 사용 됩니다. 

`true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`및 `Zero` 상수는 Q #에서 모든 예약 된 기호입니다.

## <a name="array-types"></a>배열 형식

유효한 Q # 형식 `'T`지정 된 경우 `'T`형식의 값 배열을 나타내는 형식이 있습니다.
이 배열 형식은 `'T[]`으로 표시 됩니다. 예를 들어 `Qubit[]` 또는 `Int[][]`입니다.
예를 들어, 정수 컬렉션은 `Int[]`로 표시 되 고, `(Bool, Pauli)` 값 배열의 배열은 `(Bool, Pauli)[][]`로 표시 됩니다.

두 번째 예제에서이는 사각형 2 차원 배열이 아니라 잠재적으로 가변 배열 배열을 나타냅니다.
Q #에서는 사각형 다차원 배열에 대 한 지원을 제공 하지 않습니다.

`[PauliI, PauliX, PauliY, PauliZ]`와 같이 배열의 요소 주위에 대괄호를 사용 하 여 Q # 소스 코드에서 배열 값을 작성할 수 있습니다.
배열 리터럴의 형식은 배열의 모든 항목에 대 한 공통 기본 형식에 의해 결정 됩니다. 

> [!WARNING]
> 배열을 만든 후에는 배열의 요소를 변경할 수 없습니다.
> 업데이트 및 재할당 문 및/또는 복사 및 업데이트 식은 수정 된 배열을 생성 하는 데 사용할 수 있습니다.

또는 `new` 키워드를 사용 하 여 크기에서 배열을 만들 수 있습니다.

```qsharp
let zeros = new Int[13];
// new also allows for creating empty arrays:
let emptyRegister = new Qubit[0];
```

두 경우 모두 배열이 생성 된 후에는 핵심 함수 `Length`를 사용 하 여 요소 수를 `Int`으로 가져올 수 있습니다.
배열에는 대괄호를 사용 하 여 첨자 수 있습니다. 아래 첨자는 형식 `Int` 또는 형식 `Range`를 사용 하 여 배열 요소의 하위 집합을 포함 하는 단일 요소나 새 배열을 가져옵니다.
배열의 첨자는 0부터 시작 합니다.

```qsharp
let arr = [10, 11, 36, 49];
let ten = arr[0]; // 10
let odds = arr[1..2..4]; // [11, 49]
```

## <a name="tuple-types"></a>튜플 형식

0 개 이상의 다른 형식 `T0`, `T1`, ..., `Tn`지정 된 경우 새 *튜플 형식을* `(T0, T1, ..., Tn)`로 나타낼 수 있습니다.
새 튜플 형식을 생성 하는 데 사용 되는 형식은 `(Int, (Qubit, Qubit))`처럼 튜플이 될 수 있습니다.
그러나 이러한 중첩은 항상 유한 하지만 튜플 형식은 어떤 경우에도 자체적으로 포함 될 수 없습니다.

새 튜플 형식의 값은 튜플의 각 형식에서 값의 시퀀스로 구성 된 튜플입니다.
예를 들어 `(3, false)`은 `(Int, Bool)`튜플 유형인 형식의 튜플입니다.
튜플, 배열의 튜플, 하위 튜플 튜플 등의 배열을 만들 수 있습니다.

Q # 0.3에서 `Unit`은 빈 튜플의 *형식* 이름입니다. `()`는 빈 튜플 *값*에 사용 됩니다.

튜플 인스턴스는 변경할 수 없습니다.
Q #에서는 생성 된 튜플의 콘텐츠를 변경 하는 메커니즘을 제공 하지 않습니다.

튜플은 값을 단일 값으로 수집 하 여 보다 쉽게 전달할 수 있도록 Q # 전체에서 사용 되는 강력한 개념입니다.
특히 튜플 표기법을 사용 하면 모든 작업 및 호출 가능에서 정확히 하나의 입력을 사용 하 고 정확히 하나의 출력을 반환 하도록 표현할 수 있습니다.

### <a name="singleton-tuple-equivalence"></a>단일 튜플 동등성

`(5)` 또는 `([1,2,3])`와 같이 singleton (단일 요소) 튜플 `('T1)`만들 수 있습니다.
그러나 Q #은 singleton 튜플을 포함 된 형식의 값과 완전히 동일 하 게 처리 합니다.
즉, `5`와 `(5)`간에 차이가 없으며 `5`와 `(((5)))`사이 또는 `(5, (6))` 간에 차이가 없습니다.`(5, 6)`

이러한 동등성은 할당 및 식을 비롯 한 모든 용도에 적용 됩니다.
`5+3`를 작성 하는 데 `(5)+3`를 작성 하는 것은 올바르지만 두 식이 모두 `8`으로 계산 됩니다.
특히이는 입력 튜플 또는 출력 튜플 형식이 하나의 필드를 갖는 작업 또는 함수가 단일 인수를 사용 하거나 단일 값을 반환 하는 것으로 간주할 수 있음을 의미 합니다.

이 속성은 _단일 튜플 동치_로 참조 됩니다.

## <a name="user-defined-types"></a>사용자 정의 형식

Q # 파일은 법적 형식의 단일 값을 포함 하는 새 명명 된 형식을 정의할 수 있습니다.
`T`모든 튜플 형식에 대해 `newtype` 문으로 `T`의 하위 형식인 새 사용자 정의 형식을 선언할 수 있습니다.
예를 들어 @"microsoft.quantum.math" 네임 스페이스에서 복소수는 사용자 정의 형식으로 정의 됩니다.

```qsharp
newtype Complex = (Double, Double);
```

이 문은 `Double`형식의 익명 항목 두 개를 사용 하 여 새 형식을 만듭니다.   
익명 항목 외에도 사용자 정의 형식은 Q # 버전 0.7 이상으로 명명 된 항목을 지원 합니다. 예를 들어 복소수의 실수 부분을 나타내는 double의 경우 `Re` 항목의 이름을로 지정 하 고 허수 부분에 대해 `Im` 수 있습니다. 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
사용자 정의 형식에서 한 항목의 이름을 지정 하는 것은 모든 항목의 이름을 지정 해야 한다는 의미는 아닙니다. 명명 된 항목 및 명명 되지 않은 항목의 모든 조합이 지원 됩니다. 또한 내부 항목의 이름을 지정할 수 있습니다.
예를 들어 아래에 정의 된 것 처럼 `Nested` 형식에는 `Int` 형식의 항목만 이름이 지정 되 고 다른 모든 항목은 익명 인 기본 형식 `(Double, (Int, String))`있습니다. 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```
명명 된 항목은 `::`액세스 연산자를 통해 직접 액세스할 수 있다는 장점이 있습니다. 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

반면에 익명 항목에 액세스 하려면 `!`후 위 연산자를 사용 하 여 래핑된 값을 먼저 추출 해야 합니다.
"래핑 해제" 연산자 `!`는 사용자 정의 형식에 포함 된 값을 추출할 수 있습니다.
이러한 "래핑 해제" 식의 형식은 사용자 정의 형식의 기본 형식입니다. 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

래핑 해제 연산자는 정확히 한 줄의의 래핑을 해제 합니다.
여러 래핑 연산자를 사용 하 여 곱하기 래핑된 값에 액세스할 수 있습니다.

예:

```qsharp
newtype WrappedInt = Int;
newtype DoublyWrappedInt = WrappedInt;

...
    let x = DoublyWrappedInt(WrappedInt(6));
    let y = x!;       // y is WrappedInt(6)
    let z = x!!;      // z is 6
    let a = x + 5;    // This is an error, a DoublyWrappedInt isn't an Int
    let b = x! + 5;   // Also an error
    let c = x!! + 5;  // This is valid, c will be 11
...
```

자세한 내용은 [래핑 해제 식](xref:microsoft.quantum.language.expressions#unwrap-expressions) 및 [연산자 우선 순위](xref:microsoft.quantum.language.expressions#operator-precedence) 에 대 한 섹션을 참조 하세요.

사용자 정의 형식의 값은 해당 형식 생성자를 호출 하 여 만들 수 있습니다.

```
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

또는 [복사 및 업데이트 식을](xref:microsoft.quantum.language.expressions#copy-and-update-expressions)사용 하 여 기존 값에서 새 값을 만들 수 있습니다. 배열의 경우와 같이 이러한 식은 지정 된 명명 된 항목을 제외 하 고 원래 식의 모든 항목 값을 복사 합니다. 이러한 값은 식의 오른쪽에 정의 된 값으로 설정 됩니다. 예를 들어 [업데이트 및 재할당 문과](xref:microsoft.quantum.language.statements#update-and-reassign-statement)같이 사용자 정의 형식에 명명 된 항목에 대 한 배열 항목에 사용할 수 있는 다른 언어 구문은 있습니다.

```qsharp
newtype ComplexArray = (Count : Int, Data : Complex[]);

function AsComplexArray (data : Double[]) : ComplexArray {

    mutable res = ComplexArray(0, new Complex[0]);
    for (item in data) {
        set res w/= Data <- res::Data + [Complex(item, 0.)]; // update-and-reassign statement
    }
    return res w/ Count <- Length(res::Data); // returning a copy-and-update expression
}
```

사용자 정의 형식은 다른 모든 형식을 사용할 수 있는 모든 위치에서 사용할 수 있습니다.
특히 사용자 정의 형식의 배열을 정의 하 고 사용자 정의 형식을 튜플 형식의 요소로 포함 하는 것이 가능 합니다.

재귀 형식 구조를 만들 수는 없습니다.
즉, 사용자 정의 형식을 정의 하는 형식은 사용자 정의 형식의 요소를 포함 하는 튜플 형식이 아닐 수 있습니다.
보다 일반적으로 사용자 정의 형식에는 순환 종속성이 있을 수 없으므로 다음과 같은 형식 정의 집합이 잘못 될 수 있습니다.

```qsharp
newtype TypeA = (Int, TypeB);
newtype TypeB = (Double, TypeC);
newtype TypeC = (TypeA, Range);
```

잠재적으로 복잡 한 튜플 형식에 대 한 짧은 별칭을 제공 하는 것 외에도 이러한 형식을 정의 하면 특정 값의 의도를 문서화할 수 있습니다.
`Complex`예제로 돌아가면 2D 극좌표 형 좌표를 사용자 정의 형식으로 정의할 수도 있습니다.

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

`Complex`와 `Polar` 모두 기본 형식이 `(Double, Double)`있지만 Q #에서 두 가지 형식이 모두 호환 되지 않습니다. 또한 극좌표로 복잡 한 수학 함수를 실수로 호출 하는 위험을 최소화 하 고 그 반대의 경우도 마찬가지입니다.
이러한 방식으로 사용자 정의 형식은와 비슷한 역할 F# 을 합니다. 예를 들면입니다. 


## <a name="operation-and-function-types"></a>작업 및 함수 형식

Q # _작업_ 은 퀀텀 서브루틴입니다.
즉, 양자 연산을 포함하는 호출 가능 루틴입니다.

Q # _함수_ 는 퀀텀 알고리즘 내에서 사용 되는 기존 서브루틴입니다.
기존 코드를 포함할 수 있지만 퀀텀 작업은 포함 되지 않습니다.
특히 함수는 이러한 기능을 할당 하거나 빌려 서 작업을 호출할 수 없습니다.
그러나 처리를 위해 작업 또는 원하는 비트를 전달할 수도 있습니다.
따라서 함수는 동일한 인수를 사용 하 여 호출 하면 항상 동일한 결과를 생성 한다는 점에서 완전히 결정적입니다. 

작업 및 함수를 함께 _callables_이라고 합니다.  아래에 대 한 몇 가지 [예](#examples) 를 확인할 수 있습니다.

모든 Q # callables은 단일 값을 입력으로 사용 하 고 단일 값을 출력으로 반환 하는 것으로 간주 됩니다.
입력 값과 출력 값 모두 튜플이 될 수 있습니다.
결과를 반환 하지 않는 callables `Unit`입니다.
입력이 없는 callables은 빈 튜플을 입력으로 사용 합니다.

호출할 수 있는 기본 형식은 `('Tinput => 'Tresult)` 또는 `('Tinput -> 'Tresult)`으로 작성 됩니다. 여기서 `'Tinput`와 `'Tresult`는 모두 형식입니다.
`=>`를 사용 하는 첫 번째 폼은 작업에 사용 됩니다. 함수의 두 번째 형태 (`->`)입니다.
예를 들어 `((Qubit, Pauli) => Result)`은 가능한 단일 수준 비트 측정 작업의 시그니처를 나타냅니다.

함수 형식은 해당 시그니처로 완전히 지정 됩니다.
예를 들어, 각도의 사인을 계산 하는 함수에는 `(Double -> Double)`형식이 있습니다.

작업 (함수 아님)에는 작업 유형의 일부로 표시 되는 특정 추가 _특징이_ 있습니다. 이러한 특성에는 작업에서 지 원하는 함수에 대 한 정보가 포함 됩니다.
함수는 기본 작업의 특수화를 생성 하는 meta 작업입니다. 아래의 [함수](#functors)을 참조 하세요.

작업 유형은 입력 유형, 출력 유형 및 해당 특성에 의해 지정 됩니다.    
작업 형식에서 `Controlled` 및/또는 `Adjoint` 함수를 지원 하도록 요구 하려면 해당 특성을 나타내는 주석을 추가 해야 합니다.
예를 들어 `is Ctl` 주석은 작업을 제어할 수 있음을 나타냅니다. 해당 형식의 작업에서 `Adjoint` 및 `Controlled` 함수를 모두 지원 하도록 요구 하려는 경우이를 `(Qubit => Unit is Adj + Ctl)`로 표현할 수 있습니다. `Adj` 사용 되는 작업 특성 및 `Ctl`에 대 한 자세한 내용은 미리 정의 된 두 개의 레이블 집합입니다. 각 레이블은 특정 함수에 대 한 지원 등의 특정 작업 특징을 나타냅니다.
따라서 `+`은 이러한 두 집합의 합집합을 나타내는 데 사용 되며, 교집합을 나타내는 데 사용 되는 `*` (예: 두 집합에 공통 된 레이블).  

예를 들어 Pauli `X` 작업에는 `(Qubit => Unit is Adj + Ctl)`형식이 있습니다.
함수을 지원 하지 않는 작업 형식은 입력 및 출력 형식 만으로 지정 되 고 추가 주석은 포함 하지 않습니다.


### <a name="type-parameterized-functions-and-operations"></a>형식 매개 변수화 된 함수 및 작업

호출 가능 형식에는 형식 매개 변수가 포함 될 수 있습니다.
형식 매개 변수는 작은따옴표가 접두사로 붙는 기호로 표시 됩니다. 예를 들어 `'A`은 올바른 형식 매개 변수입니다.

단일 서명에서 형식 매개 변수가 두 번 이상 나타날 수 있습니다.
예를 들어, 배열의 각 요소에 다른 함수를 적용 하 고 수집 된 결과를 반환 하는 함수는 시그니처를 `(('A[], 'A->'A) -> 'A[])`합니다.
마찬가지로 두 작업의 컴퍼지션을 반환 하는 함수에는 서명 `((('A=>'B), ('B=>'C)) -> ('A=>'C))`있을 수 있습니다.

형식이 매개 변수가 있는 호출 가능 매개 변수를 호출 하는 경우 동일한 형식 매개 변수를 갖는 모든 인수는 동일한 형식 이어야 합니다.

Q #에서는 형식 매개 변수를 대체할 수 있는 가능한 형식을 제한 하는 메커니즘을 제공 하지 않습니다.

### <a name="type-compatibility"></a>형식 호환성

추가 함수 지원 되는 작업은 함수가 더 작은 작업에 사용 될 수 있지만 동일한 서명이 필요 합니다.
예를 들어 형식 `(Qubit => Unit is Adj)`의 작업은 `(Qubit => Unit)` 형식의 작업이 예상 되는 모든 위치에서 사용 될 수 있습니다.

Q #은 호출 가능 반환 형식과 관련 하 여 공변 (covariant)이 있습니다. `'A` 형식을 반환 하는 호출 가능은 입력 형식이 동일한 호출 가능 및 `'A`와 호환 되는 결과 형식에 호환 됩니다.

Q #은 입력 유형과 관련 하 여 반공 변 (contravariant)입니다. 입력으로 `'A` 형식을 사용 하는 호출 가능은 같은 결과 형식 및 `'A`와 호환 되는 입력 형식으로 호출할 수 있는와 호환 됩니다.

즉, 다음과 같은 정의가 제공 됩니다.

```qsharp
operation Invert(qubits : Qubit[]) : Unit 
is Adj {...} 

operation ApplyUnitary(qubits : Qubit[]) : Unit 
is Adj + Ctl {...} 

function ConjugateInvertWith(
    inner : (Qubit[] => Unit is Adj),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj) {...}

function ConjugateUnitaryWith(
    inner : (Qubit[] => Unit is Adj + Ctl),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj + Ctl) {...}
```

다음은 true입니다.

- `Invert` 또는 `ApplyUnitary`의 `inner` 인수를 사용 하 여 `ConjugateInvertWith` 함수를 호출할 수 있습니다.
- `ConjugateUnitaryWith` 함수는 `ApplyUnitary`의 `inner` 인수를 사용 하 여 호출할 수 있지만 `Invert`는 호출할 수 없습니다.
- `ConjugateInvertWith`에서 반환 될 수 `(Qubit[] => Unit is Adj + Ctl)` 형식의 값입니다.

> [!IMPORTANT]
> Q # 0.3에서는 사용자 정의 형식의 동작에 상당한 차이가 있습니다.

사용자 정의 형식은 하위 형식이 아니라 기본 형식의 래핑된 버전으로 취급 됩니다.
이는 기본 형식의 값이 필요한 경우 사용자 정의 형식의 값을 사용할 수 없음을 의미 합니다.

### <a name="functors"></a>함수

Q #의 함수는 다른 작업에서 새 작업을 정의 하는 팩터리입니다.
함수는 새 작업의 구현을 정의할 때 기본 작업의 구현에 액세스할 수 있습니다.
따라서 함수는 기존의 상위 수준 함수 보다 더 복잡 한 함수를 수행할 수 있습니다.

함수에는 Q # 형식 시스템에 대 한 표현이 없습니다. 따라서 현재 변수를 변수에 바인딩하거나 인수로 전달할 수 없습니다. 

함수는 작업에 적용 하 여 새 작업을 반환 하는 데 사용 됩니다.
예를 들어 `Adjoint` 함수를 `Y` 작업에 적용 하 여 발생 하는 작업은 `Adjoint Y`으로 작성 됩니다.
그런 다음 다른 작업과 마찬가지로 새 작업을 호출할 수 있습니다.
따라서 `Adjoint Y(q1)`는 Adjoint 함수를 `Y` 작업에 적용 하 여 새 작업을 생성 하 고 `q1`에 새 작업을 적용 합니다.

마찬가지로 `Controlled X(controls, target)`는 제어 되는 함수를 `X` 작업에 적용 하 여 새 작업을 생성 하 고 `controls` 및 `target`에 새 작업을 적용 합니다.

Q #의 두 표준 함수 `Adjoint` `Controlled`됩니다.

#### <a name="adjoint"></a>Adjoint

퀀텀 컴퓨팅에서 작업의 adjoint는 작업의 복잡 한 복소수 바꾸기입니다.
단일 연산자를 구현 하는 작업의 경우 adjoint는 작업의 역함수입니다.
특정 집합에 대 한 다른 단일 작업의 시퀀스를 호출 하는 간단한 작업의 경우, 역방향 시퀀스에서 동일한의 하위 작업에 대 한 adjoint를 적용 하 여 adjoint를 계산할 수 있습니다.

작업 식이 지정 된 경우 `Adjoint` 함수를 사용 하 여 새 작업 식을 설정할 수 있습니다.
예를 들어 `Adjoint QFT`은 `QFT` 작업의 adjoint를 지정 합니다.
새 작업의 시그니처와 형식이 기본 작업과 동일 합니다.
특히, 새 작업은 `Adjoint`를 허용 하며, 기본 작업에서 수행한 경우에만 `Controlled`를 허용 합니다.

Adjoint 함수는 자체적으로 반전 됩니다. 즉 `Adjoint Adjoint Op` 항상 `Op`와 동일 합니다.

#### <a name="controlled"></a>제어

제어 되는 작업 버전은 모든 컨트롤이 지정 된 상태에 있는 경우에만 기본 작업을 효과적으로 적용 하는 새 작업입니다.
컨트롤의 superposition에 있는 경우 기본 작업은 superposition의 해당 부분에 coherently 적용 됩니다.
따라서 제어 된 작업은 종종 되거나 얽 히을 생성 하는 데 사용 됩니다.

Q #에서 제어 되는 버전은 항상 컨트롤의 배열을 사용 하 고, 지정 된 상태는 항상 계산 (`PauliZ`) `One` 상태, $ \ket{1}$에 있는 모든 컨트롤에 대해 지정 됩니다.
제어 된 작업 이전에 적절 한 단일 작업을 제어 된 작업 이전에 적용 한 다음, 제어 된 작업 후에 단일 작업의 반대을 적용 하 여 다른 상태를 기반으로 하는 제어를 달성할 수 있습니다.
예를 들어 제어 되는 작업 전후에 `X` 연산을 컨트롤에 적용 하면 작업에서 해당 하는 작업의 `Zero` 상태 ($ \ket{0}$)를 제어 합니다. 이전 및 이후 `H` 작업을 적용 하면 `PauliX` `One` 상태가 제어 됩니다. 즉,{0}{1}상태가 아닌 Pauli X, $ \ket{-} \mathrel{: =} (\ket{2}-\ket `PauliZ`)/\sqrt `One` $의-1 eigenvalue입니다.

작업 식이 지정 된 경우 `Controlled` 함수를 사용 하 여 새 작업 식을 설정할 수 있습니다.
새 작업의 서명은 원래 작업의 서명을 기반으로 합니다.
결과 형식은 동일 하지만 입력 형식은 두 번째 요소로 서, 컨트롤의 요소를 첫 번째 요소로 사용 하 고 원래 작업의 인수를 두 번째 요소로 보유 하 고 있는 두 번째 튜플입니다.
새 작업은 `Controlled`를 지원 하 고 원래 작업에서 수행한 경우에만 `Adjoint`를 지원 합니다.

원래 작업에 단일 인수만 사용한 경우 단일 튜플 동등성은 여기에서 재생 됩니다.
예를 들어 `Controlled X`은 `X` 작업의 제어 된 버전입니다.
`X` 형식 `(Qubit => Unit is Adj + Ctl)`이므로 `Controlled X` `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`형식입니다. 단일 튜플 때문에 `((Qubit[], Qubit) => Unit is Adj + Ctl)`와 동일 합니다.

기본 작업에서 여러 인수를 사용한 경우에는 작업의 제어 되는 버전에 대 한 해당 인수를 괄호로 묶어 튜플로 변환 해야 합니다.
예를 들어 `Controlled Rz`은 `Rz` 작업의 제어 된 버전입니다.
`Rz` 형식 `((Double, Qubit) => Unit is Adj + Ctl)`이므로 `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`형식이 `Controlled Rz` 있습니다.
따라서 `Controlled Rz(controls, (0.1, target))`은 `Controlled Rz`의 유효한 호출입니다 (`0.1, target`괄호로 묶은 괄호를 참고).

또 다른 예로 `CNOT(control, target)` `Controlled X([control], target)`로 구현할 수 있습니다. 대상이 CCNOT (2 컨트롤)로 제어 되어야 하는 경우 `Controlled X([control1, control2], target)` 문을 사용할 수 있습니다.

### <a name="examples"></a>예

Q # 작업의이 예제는 [측정](https://github.com/microsoft/Quantum/tree/master/samples/getting-started/measurement) 샘플에서 제공 됩니다. 작업 내에서, `H` 및 `X`와 같은 해당 기능에 대 한 퀀텀 작업을 할당 하 고이를 사용할 수 있습니다.

```qsharp
/// # Summary
/// Prepares a state and measures it in the Pauli-Z basis.
operation MeasureOneQubit() : Result {
        mutable result = Zero;

        using (qubit = Qubit()) { // Allocate a qubit
            H(qubit);               // Use a quantum operation on that qubit
            set result = M(qubit);      // Measure the qubit
            if (result == One) {    // Reset the qubit so that it can be released
                X(qubit);
            }

            return result;
        }
 }
```

이 함수의 예는 [PhaseEstimation](https://github.com/microsoft/Quantum/tree/master/samples/characterization/phase-estimation) 샘플에서 가져온 것입니다. 순수 하 게 클래식 코드를 포함 합니다. 위의 예제와는 달리, 더 이상 할당 되지 않으며 퀀텀 작업을 사용 하지 않는 것을 볼 수 있습니다.

```qsharp
/// # Summary
/// Given two arrays, returns a new array that is the pointwise product
/// of each of the given arrays.
function PointwiseProduct(left : Double[], right : Double[]) : Double[] {
    mutable product = new Double[Length(left)];

    for (idxElement in IndexRange(left)) {
        set product w/= idxElement <- left[idxElement] * right[idxElement];
    }
    return product;
}
```

[ReversibleLogicSynthesis](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/reversible-logic-synthesis) 샘플의이 예제와 같이 함수를 처리에 사용할 수 있습니다. 이 함수에 전달 되 고 처리에 사용 되는 것은 아니지만, 아무 것도 수정 되지 않습니다.

```qsharp
/// # Summary
/// Translate MCT masks into multiple-controlled Toffoli gates (with single
/// targets).
function GateMasksToToffoliGates(
    qubits : Qubit[], 
    masks : MCMTMask[]) 
: MCTGate[] {

    mutable result = new MCTGate[0];
    let n = Length(qubits);

    for (i in 0 .. Length(masks) - 1) {
        let (controls, targets) = (masks[i])!;
        let controlBits = IntegerBits(controls, n);
        let targetBits = IntegerBits(targets, n);
        let cQubits = Subarray(controlBits, qubits);
        let tQubits = Subarray(targetBits, qubits);

        for (target in tQubits) {
            set result += [MCTGate(cQubits, target)];
        }
    }

    return result;
}
```
