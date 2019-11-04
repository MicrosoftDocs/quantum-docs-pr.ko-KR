---
title: 파일 구조 | Microsoft Docs
description: 'Q # 파일 구조'
author: QuantumWriter
uid: microsoft.quantum.language.file-structure
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 40b2e7ddf5def6285250dffe130b152429dce1f8
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185191"
---
# <a name="file-structure"></a>파일 구조

Q # 파일은 네임 스페이스 선언 시퀀스로 구성 됩니다.
각 네임 스페이스 선언에는 사용자 정의 형식, 작업 및 함수에 대 한 선언이 포함 됩니다.
네임 스페이스 선언에는 임의의 순서 대로 각 선언 형식이 포함 될 수 있습니다.
네임 스페이스 선언 외부에 나타날 수 있는 유일한 텍스트는 주석입니다.
특히 네임 스페이스에 대 한 문서 주석은 선언 앞에 나옵니다.

## <a name="namespace-declarations"></a>네임 스페이스 선언

Q # 파일은 일반적으로 정확히 하나의 네임 스페이스 선언을 포함 하지만, 없거나 비어 있거나 주석을 포함 하거나, 여러 네임 스페이스를 포함할 수 있습니다.
네임 스페이스 선언은 중첩 될 수 없습니다.

동일한 네임 스페이스는 동일한 이름을 가진 형식, 작업 또는 함수 선언이 없으면 함께 컴파일되는 여러 Q # 파일에 선언할 수 있습니다.
특히 선언이 동일한 경우에도 여러 파일에서 동일한 네임 스페이스에 동일한 형식을 정의 하는 것은 유효 하지 않습니다.

네임 스페이스 선언은 `namespace`키워드와 네임 스페이스 이름, 여는 중괄호 `{`, 네임 스페이스에 포함 된 선언 및 닫는 중괄호 `}`으로 구성 됩니다.
네임 스페이스 이름은 마침표로 구분 된 하나 이상의 법적 기호 시퀀스의 .NET 패턴을 따릅니다 `.`.
예를 들어 `MyQuantumStuff` 및 `Microsoft.Quantum.Canon`는 유효한 네임 스페이스 이름입니다.
규칙에 따라 네임 스페이스 이름의 기호는 대문자로 되어 있지만 반드시 필요한 것은 아닙니다.

선언은 네임 스페이스 선언에서 임의의 순서로 나타날 수 있습니다.
파일에서 나중에 선언 된 형식 또는 callables에 대 한 참조가 제대로 확인 됩니다. 형식, 작업 또는 함수 선언이 참조 앞에 오지 않아도 됩니다.

## <a name="open-directives"></a>지시문 열기

네임 스페이스 블록 내에서 `open` 지시어를 사용 하 여 특정 네임 스페이스에 정의 된 모든 형식 및 callables을 가져와서 정규화 되지 않은 이름으로 참조할 수 있습니다. 

이러한 `open` 지시어는 `open` 키워드로 구성 된 다음 열 네임 스페이스와 종료 세미콜론으로 구성 됩니다.

예를 들어

```qsharp
open Microsoft.Quantum.Canon;
```

필요에 따라 열린 네임 스페이스의 짧은 이름을 정의 하 여 해당 네임 스페이스의 모든 요소를 정의 된 약식 이름으로 정규화 하 고 필요에 따라 정규화 할 수 있습니다. 이러한 짧은 이름은 `open` 지시문에서 세미콜론 앞에 `as` 키워드를 추가 하 여 정의 됩니다.

```qsharp
open Microsoft.Quantum.Math as Math;
```

모든 `open` 지시문은 네임 스페이스 블록의 `function`, `operation`또는 `newtype` 선언 앞에 나와야 합니다.
`open` 지시문은 파일 내의 전체 네임 스페이스 블록에 적용 됩니다.

## <a name="user-defined-type-declarations"></a>사용자 정의 형식 선언

Q #에서는 [q # 형식 모델](xref:microsoft.quantum.language.type-model) 섹션에 설명 된 대로 사용자가 새 사용자 정의 형식을 선언할 수 있는 방법을 제공 합니다.
사용자 정의 형식은 기본 형식이 동일한 경우에도 고유 합니다.
특히 기본 형식이 동일한 경우에도 두 사용자 정의 형식의 값 사이에 자동 변환이 없습니다.

사용자 정의 형식 선언은 `newtype`키워드로 구성 된 다음 사용자 정의 형식 이름, `=`, 유효한 형식 사양 및 종료 세미콜론으로 구성 됩니다.

다음은 그 예입니다.

```qsharp
newtype PairOfInts = (Int, Int);
```

각 Q # 소스 파일은 원하는 수의 사용자 정의 형식을 선언할 수 있습니다.
형식 이름은 네임 스페이스 내에서 고유 해야 하며 작업 및 함수 이름과 충돌 하지 않을 수 있습니다.

사용자 정의 형식 간에 순환 종속성을 정의할 수는 없습니다. 따라서 Q # 내에서 재귀 형식을 사용할 수 없습니다.

## <a name="operation-declarations"></a>작업 선언

작업은 Q #의 핵심 이며, 다른 언어의 함수와 거의 유사 합니다.
각 Q # 소스 파일은 원하는 수의 작업을 정의할 수 있습니다.

작업 이름은 네임 스페이스 내에서 고유 해야 하며 형식 및 함수 이름과 충돌 하지 않을 수 있습니다.

작업 선언은 `operation`키워드로 구성 된 다음 작업의 이름인 기호, 작업에 대 한 인수를 정의 하는 형식화 된 식별자 튜플, 콜론 `:`, 작업의 결과 형식을 설명 하는 형식 주석으로 구성 됩니다. 선택적으로 작업 특징, 여는 중괄호 `{`, 작업 선언의 본문 및 최종 닫는 중괄호 `}`포함 된 주석입니다.

작업 선언의 본문은 기본 구현 또는 특수화 목록으로 구성 됩니다.
기본 본문 특수화의 구현만 명시적으로 지정 해야 하는 경우에는 선언 내에서 직접 기본 구현을 지정할 수 있습니다.
이 경우 선언에서 작업 특성이 포함 된 주석은 컴파일러가 기본 구현을 기반으로 하 여 다른 특수화를 자동으로 생성 하는지 확인 하는 데 유용 합니다. 

예를 들면 다음과 같습니다. 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```

작업 특성은 선언 된 작업에 적용할 수 있는 함수의 종류와 적용 되는 결과를 정의 합니다. 작업에서 단일 변환을 구현 하는 경우 *adjointed* 또는 *제어*될 때 작업이 작동 하는 방식을 정의할 수 있습니다.
이러한 특수화의 존재는 작업 시그니처의 일부로 선언할 수 있습니다. 이렇게 암시적으로 선언 된 각 특수화에 해당 하는 구현은 컴파일러에 의해 생성 됩니다. 위의 예제에서 adjoint, 제어 된 adjoint 특수화는 컴파일러에 의해 생성 됩니다. 

컴파일러가 구현을 생성할 수 없는 경우에는 명시적으로 지정할 수 있습니다. 이러한 명시적 특수화 선언은 특정 특수화를 빌드하는 방법이 나 사용자 정의 구현을 명확 하 게 하는 적절 한 세대 지시문으로 구성 될 수 있습니다. 위의 `PrepareEntangledPair` 코드는 다음 코드와 같이 명시적 특수화 선언이 포함 된 코드와 같습니다. 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    adjoint auto; // auto-generate adjoint specialization
    controlled auto; // auto-generate controlled specialization
    controlled adjoint auto; // auto-generate controlled adjoint specialization
}
```
키워드 `auto`은 컴파일러가 특수화 구현을 생성 하는 방법을 결정 해야 함을 나타냅니다.
컴파일러가 더 정확한 생성 지시문과 같은 추가 지침 없이 특정 특수화에 대 한 구현을 생성할 수 없는 경우 또는 보다 효율적인 구현을 지정할 수 있는 경우에도 구현이 수동으로 정의 될 수 있습니다.

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```

위의 예제에서 `adjoint invert;`는 본문 구현을 반전 하 여 adjoint 특수화가 생성 되 고 `controlled adjoint invert;`는 지정 된 구현을 반전 하 여 제어 된 adjoint 특수화가 생성 됨을 나타냅니다. 제어 된 특수화.

`Adjoint` 및/또는 `Controlled` 함수의 응용 프로그램을 지 원하는 작업의 경우 반환 형식은 반드시 `Unit`해야 합니다. 


### <a name="explicit-specialization-declarations"></a>명시적 특수화 선언

Q # 작업에는 다음과 같은 명시적 특수화 선언이 포함 될 수 있습니다.

- `body` 특수화는 함수 적용 되지 않은 작업의 구현을 지정 합니다.
- `adjoint` 특수화는 적용 된 `Adjoint` 함수를 사용 하 여 작업의 구현을 지정 합니다.
- `controlled` 특수화는 적용 된 `Controlled` 함수를 사용 하 여 작업의 구현을 지정 합니다.
- `controlled adjoint` 특수화는 `Adjoint` 및 `Controlled` 함수 적용 된 작업의 구현을 지정 합니다.
  두 함수 commute 이후이 특수화의 이름을 `adjoint controlled`로 지정할 수도 있습니다.


작업 특수화는 특수화 태그 (예: `body`, `adjoint`등)와 다음 중 하나입니다.

- 아래에 설명 된 명시적 선언입니다.
- 다음 중 하나에 해당 하는 특수화를 생성 하는 방법을 컴파일러에 지시 하는 지시문입니다.
  - `intrinsic`는 대상 컴퓨터에서 특수화가 제공 됨을 나타냅니다.
  - `distribute``controlled` 및 `controlled adjoint` 특수화와 함께 사용할 수 있습니다.
    `controlled`와 함께 사용 하는 경우 `body`의 모든 작업에 `Controlled`를 적용 하 여 컴파일러가 특수화를 계산 해야 함을 나타냅니다.
    `controlled adjoint`와 함께 사용 하는 경우 컴파일러는 `adjoint` 특수화의 모든 작업에 `Controlled`를 적용 하 여 특수화를 계산 해야 함을 나타냅니다.
  - `invert`: 컴파일러가 `body`를 반전 하 여 `adjoint` 특수화를 계산 해야 함을 나타냅니다. 즉, 작업 순서를 반대로 하 고 각 항목에 adjoint를 적용 합니다.
    `adjoint controlled`와 함께 사용 하는 경우 컴파일러에서 `controlled` 특수화를 반전 하 여 특수화를 계산 해야 함을 나타냅니다.
  - `self`adjoint 특수화가 `body` 특수화와 동일 함을 나타내는입니다.
    이는 `adjoint` 및 `adjoint controlled` 특수화에 대해 유효 합니다.
    `adjoint controlled`에서 `self` `adjoint controlled` 특수화가 `controlled` 특수화와 동일 하다는 것을 의미 합니다.
  - `auto`컴파일러에서 적용할 적절 한 지시문을 선택 해야 함을 나타내려면입니다.
    `auto` `body` 특수화에 사용할 수 없습니다.

지시문과 `auto` 모두에는 닫는 세미콜론 `;`필요 합니다.
`body`의 명시적 선언이 제공 되는 경우 `auto` 지시문은 다음 세대 지시문으로 확인 됩니다.

- `adjoint` 특수화는 지시문 `invert`에 따라 생성 됩니다.
- `controlled` 특수화는 지시문 `distribute`에 따라 생성 됩니다.
- `adjoint controlled` 특수화는 `controlled`에 대 한 명시적 선언이 `adjoint`에 대해 지정 되지 않은 경우 `invert` 지시문에 따라 생성 되 고 그렇지 않은 경우 `distribute`.

> [!TIP]   
> 작업이 자체 adjoint 인 경우 생성 `self` 지시문을 통해 adjoint 또는 제어 된 adjoint 특수화를 명시적으로 지정 하 여 컴파일러가 최적화를 위해 해당 정보를 사용할 수 있도록 합니다.

사용자 정의 구현을 포함 하는 특수화 선언은 인수 튜플 및 특수화를 구현 하는 Q # 코드가 포함 된 문 블록으로 구성 됩니다.
인수 목록에서 `...`는 작업에 대해 전체적으로 선언 된 인수를 나타내는 데 사용 됩니다.
`body` 및 `adjoint`의 경우 인수 목록은 항상 `(...)`해야 합니다. `controlled` 및 `adjoint controlled`의 경우 인수 목록은 컨트롤의 배열을 표시 하 고 그 뒤에 `...`를 괄호로 묶어 나타내는 기호 여야 합니다. 예를 들어 `(controls,...)`합니다.

기본 본문 외에도 하나 이상의 특수화를 명시적으로 선언 해야 하는 경우 기본 본문의 구현은 적절 한 특수화 선언에도 래핑해야 합니다.

```qsharp
operation CountOnes(qs: Qubit[]) : Int {

    body (...) // default body specialization
    {
        mutable n = 0;
        for (q in qs) {
            set n += M(q) == One ? 1 | 0;
        }
        return n;
    }

    ...
```

### <a name="adjoint"></a>Adjoint

작업의 adjoint는 작업의 복합 복소수를 구현 하는 방법, 즉 "역방향으로 실행" 시 작업의 작동 방식을 지정 합니다.
Adjoint 없이 작업을 지정 하는 것은 유효 합니다. 예를 들어 측정 작업은 반전할 수 없으므로 adjoint를 갖지 않습니다.
작업은 해당 선언에 adjoint 특수화의 암시적 또는 명시적 선언이 포함 된 경우 `Adjoint` 함수를 지원 합니다.
명시적으로 선언 된 adjoint 특수화는 adjoint 특수화가 있음을 의미 합니다. 

본문이-success 루프, set 문, 측정값, return 문 또는 `Adjoint` 함수를 지원 하지 않는 다른 작업에 대 한 호출을 포함 하는 작업의 경우 `invert` 또는 다음에 adjoint 특수화를 자동 생성 @no__ t_2_ 지시문은 사용할 수 없습니다.

### <a name="controlled"></a>제어

작업의 제어 된 버전은 퀀텀 제어 버전의 작업을 구현 하는 방법을 지정 합니다. 즉, 조건 화 된 적용 될 때 작업의 작동 방식에는 퀀텀 레지스터가 적용 됩니다.
자세한 내용은 [제어](xref:microsoft.quantum.language.type-model#controlled) 된 섹션에서 제공 됩니다.

제어 된 버전이 없는 작업을 지정 하는 것은 유효 합니다. 예를 들어, 측정 작업은 제어할 수 없으므로 제어 되는 버전이 없습니다.
작업은 해당 선언에 제어 된 특수화의 암시적 또는 명시적 선언이 포함 된 경우에만 `Controlled` 함수를 지원 합니다.
명시적으로 선언 된 제어 된 adjoint 특수화는 제어 된 특수화가 있음을 의미 합니다. 

본문이 `Controlled` 함수를 지원 하지 않는 다른 작업에 대 한 호출을 포함 하는 작업의 경우에는 `distribute` 또는 `auto` 지시문 다음에 제어 된 특수화를 자동으로 생성할 수 없습니다.

### <a name="controlled-adjoint"></a>제어 된 Adjoint

작업의 제어 된 adjoint 버전은 작업의 adjoint의 퀀텀 제어 버전을 구현 하는 방법을 지정 합니다.
제어 된 adjoint 버전이 없는 작업을 지정 하는 것은 유효 합니다. 예를 들어, 측정 작업은 제어 또는 반전할 수 없기 때문에 제어 되는 adjoint 버전이 없습니다.

작업에 대 한 제어 된 adjoint 특수화는 adjoint와 제어 된 특수화가 모두 있는 경우에만 존재 해야 합니다. 이 경우 제어 되는 adjoint 특수화가 유추 되 고 명시적으로 정의 된 구현이 없는 경우 컴파일러에서 적절 한 특수화가 생성 됩니다. 

해당 본문에 제어 된 adjoint 버전이 없는 다른 작업에 대 한 호출이 포함 된 작업의 경우, `invert``distribute` 또는 `auto` 지시문 다음에 adjoint 특수화를 자동으로 생성 하는 것은 불가능 합니다.


### <a name="examples"></a>예시

작업 선언은 다음과 같이 간단할 수 있습니다 .이는 기본 Pauli X 작업을 정의 합니다.

```qsharp
operation X (q : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```

다음은 텔레포트 작업을 정의 합니다.

```qsharp
// Entangle two qubits.
// Assumes that both qubits are in the |0> state.
operation EPR (q1 : Qubit, q2 : Qubit) : Unit 
is Adj + Ctl {
    H(q2);
    CNOT(q2, q1);
}

// Teleport the quantum state of the source to the target.
// Assumes that the target is in the |0> state.
operation Teleport (source : Qubit, target : Qubit) : Unit {

    // Get a temporary for the Bell pair
    using (ancilla = Qubit())
    {
        // Create a Bell pair between the temporary and the target
        EPR(target, ancilla);

        // Do the teleportation
        Adjoint EPR (ancilla, source);

        if (MResetZ(source) == One) {
            X(target);
        }
        if (MResetZ(ancilla) == One) {
            Z(target);
        }
    }
}
```

## <a name="function-declarations"></a>함수 선언

함수는 Q #에서 순수 하 게 사용할 수 있는 루틴입니다.
각 Q # 소스 파일은 원하는 수의 함수를 정의할 수 있습니다.

함수 선언은 `function`키워드와 함수 이름, 형식화 된 식별자 튜플, 함수의 반환 형식을 설명 하는 형식 주석 및의 구현을 설명 하는 문 블록으로 구성 됩니다. 칩셋용으로.

함수를 정의 하는 문 블록은 `{`로 묶어야 하 고 다른 문 블록과 같이 `}` 해야 합니다.

함수 이름은 네임 스페이스 내에서 고유 해야 하며 작업 및 형식 이름과 충돌 하지 않을 수 있습니다.
함수는 이러한 기능을 할당 하거나이 작업을 호출할 수 없습니다. 부분적으로 작업을 적용 하거나 작업의 형식화 된 값을 전달 하는 것은 문제가 되지 않습니다.

예를 들면 다음과 같습니다.

```qsharp
function DotProduct(a : Double[], b : Double[]) : Double {
    if (Length(a) != Length(b)) {
        fail "Arrays are not compatible";
    }

    mutable accum = 0.0;
    for (i in 0..Length(a)-1) {
        set accum += a[i] * b[i];
    }
    return accum;
}
```
