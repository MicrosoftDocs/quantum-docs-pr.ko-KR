---
title: 의 작업 및 함수 Q#
description: 작업 및 함수를 정의 하 고 호출 하는 방법 뿐만 아니라 제어 된 및 adjoint 작업 특수화입니다.
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.operationsfunctions
no-loc:
- Q#
- $$v
ms.openlocfilehash: 55e6d3e1a242386c46213083692377520df83a80
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92692129"
---
# <a name="operations-and-functions-in-no-locq"></a>의 작업 및 함수 Q#

## <a name="defining-new-operations"></a>새 작업 정의

작업은의 핵심입니다 Q# .
선언 되 면 기존 .NET 응용 프로그램에서 호출할 수 있습니다. 예를 들어 시뮬레이터를 사용 하거나 내에서 다른 작업을 수행할 수 있습니다 Q# .
에 정의 된 각 작업은 Q# 언어로 정의 된 기본 제공 기본 작업을 포함 하 여 원하는 수의 다른 작업을 호출할 수 있습니다. 이러한 내장 작업을 정의 하는 특정 방법은 Q# 대상 컴퓨터에 따라 다릅니다.
컴파일되는 경우 각 작업은 대상 컴퓨터에 제공할 수 있는 .NET 클래스 형식으로 표시 됩니다.

각 Q# 소스 파일은 원하는 수의 작업을 정의할 수 있습니다.
작업 이름은 네임 스페이스 내에서 고유 해야 하며 형식 또는 함수 이름과 충돌 하지 않을 수 있습니다.

작업 선언은 키워드, 작업의 `operation` 인수를 정의 하는 형식화 된 식별자 튜플, 작업에 대 한 인수를 정의 하는 형식화 된 식별자 튜플, 작업의 결과 형식에 대 한 인수를 정의 하는 형식화 된 식별자 튜플, `:` 선택적으로 작업 특성을 포함 하는 주석, 여는 중괄호, 작업 선언의 본문 (중괄호로 묶)으로 구성 됩니다 `{ }` .

각 작업은 입력을 가져오고, 출력을 생성 하 고, 하나 이상의 작업 특수화에 대해 구현을 지정 합니다.
가능한 특수화와이를 정의 하 고 호출 하는 방법은이 문서의 다른 섹션에 자세히 설명 되어 있습니다.
지금은 기본 본문 특수화만 정의 하 고 단일 비트를 입력으로 사용 하 고 <xref:Microsoft.Quantum.Intrinsic.X> 해당 입력에 대 한 기본 제공 작업을 호출 하는 다음 작업을 고려 합니다.

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

키워드는 `operation` 작업 정의를 시작 하 고 그 뒤에 이름을 입력 `BitFlip` 합니다. 여기서는입니다.
그런 다음 입력의 형식이 `Qubit` `target` 새 작업 내의 입력을 참조 하는 이름과 함께 정의 됩니다 ().
마지막으로,는 `Unit` 작업의 출력이 비어 있음을 정의 합니다.
`Unit` 는 `void` c # 및 기타 명령형 언어에서와 유사 하 게 사용 되며 `unit` F # 및 다른 기능 언어에서와 동일 합니다.

작업은 보다 더 흥미로운 형식을 반환할 수도 있습니다 `Unit` .
예를 들어 <xref:Microsoft.Quantum.Intrinsic.m> 작업은 측정을 수행 하는 `Result` 것을 나타내는 형식의 출력을 반환 합니다.  작업에서 다른 작업으로 전달 하거나 키워드와 함께 사용 하 여 `let` 새 변수를 정의할 수 있습니다.

이 접근 방식을 사용 하면 [슈퍼 조밀한 코딩](https://github.com/microsoft/QuantumKatas/tree/main/SuperdenseCoding)의 경우와 같이 낮은 수준에서 퀀텀 작업과 상호 작용 하는 기존 계산을 나타낼 수 있습니다.

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {

    CNOT(there, here);
    H(there);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

> [!NOTE]
> 의 각 작업 Q# 은 정확히 하나의 입력을 받아 정확히 하나의 출력을 반환 합니다.
> 여러 값을 단일 값으로 수집 하는 *튜플을* 사용 하 여 여러 입력 및 출력이 표시 됩니다.
> 이와 관련 하 Q# 여은 "튜플 인 튜플" 언어입니다.
> 이 개념에 따라 빈 괄호 집합은 `()` 형식을 가진 "empty" 튜플로 읽어야 합니다 `Unit` .

## <a name="controlled-and-adjoint-operations"></a>제어 된 및 Adjoint 작업

에서 많은 작업을 수행 하는 경우 처럼 작업에서 단일 변환을 구현 하는 경우 Q# *adjointed* 또는 *제어* 될 때 작업의 작동 방식을 정의할 수 있습니다. 작업의 *adjoint* 특수화는 작업의 "역"이 작동 하는 방식을 지정 하는 반면, *제어* 되는 특수화는 응용 프로그램이 특정 퀀텀 레지스터의 상태에서 조건 화 된 때 작업이 작동 하는 방식을 지정 합니다.

퀀텀 작업의 adjoints는 퀀텀 컴퓨팅의 많은 측면에서 매우 중요 합니다. 유용한 프로그래밍 기술을 함께 설명 하는 이러한 상황에 대 한 예는 Q# [제어 흐름: 변화](xref:microsoft.quantum.guide.controlflow#conjugations)을 참조 하세요. 제어 되는 작업 버전은 모든 컨트롤이 지정 된 상태에 있는 경우에만 기본 작업을 효과적으로 적용 하는 새 작업입니다.
컨트롤의 superposition에 있는 경우 기본 작업은 superposition의 해당 부분에 coherently 적용 됩니다.
따라서 제어 된 작업은 종종 되거나 얽 히을 생성 하는 데 사용 됩니다.

물론, *제어 된 adjoint* 특수화도 존재할 수 있으며, 작업의 adjoint의 제어 된 응용 프로그램을 지정 합니다.

> [!NOTE]
> $U $가 연산에 의해 구현 되는 단일 변환 인 경우는 `U` `Adjoint U` 복소수 (복소수)가 복소수 인 단일 변환을 $U 나타냅니다.
> 작업을 연속적으로 적용 한 다음, 해당 adjoint를 상태에 적용 하면 ^ \a턴 = U ^ \A턴 U = \dagger $, id 매트릭스를 $UU 하는 것 처럼 상태가 변경 되지 않습니다.
> 제어 된 작업에 대 한 단일 표현은 약간 더 미묘한 [퀀텀 컴퓨팅 개념: 여러 가지](xref:microsoft.quantum.concepts.multiple-qubits)추가 정보를 찾을 수 있습니다.

다음 섹션에서는 코드에서 이러한 다양 한 특수화를 호출 하는 방법과 이러한 특수화를 지 원하는 작업을 정의 하는 방법을 설명 합니다 Q# .

### <a name="calling-operation-specializations"></a>작업 특수화 호출

의 *함수* 는 Q# 다른 작업에서 새 작업을 정의 하는 팩터리입니다.
의 두 표준 함수 Q# 는 `Adjoint` 및 `Controlled` 입니다.

함수는 새 작업의 구현을 정의할 때 기본 작업의 구현에 액세스할 수 있습니다.
따라서 함수는 기존의 상위 수준 함수 보다 더 복잡 한 함수를 수행할 수 있습니다. 함수에 형식 시스템에 대 한 표현이 없습니다 Q# . 따라서 현재 변수를 변수에 바인딩하거나 인수로 전달할 수 없습니다. 

새 작업을 반환 하는 작업에 적용 하 여 함수를 사용 합니다.
예를 들어 `Adjoint` 작업에 함수를 적용 하면 `Y` 새 작업이 반환 `Adjoint Y` 됩니다. 다른 작업과 마찬가지로 새 작업을 호출할 수 있습니다.
또는 함수의 응용 프로그램을 지 원하는 작업의 경우 `Adjoint` `Controlled` 반환 형식은 여야 `Unit` 합니다. 

#### <a name="adjoint-functor"></a>`Adjoint` 함수

따라서에서는 `Adjoint Y(q1)` 작업에 함수를 적용 하 여 `Adjoint` `Y` 새 작업을 생성 하 고 새 작업을에 적용 `q1` 합니다.
새 작업의 시그니처와 형식이 기본 작업과 동일 합니다 `Y` .
특히, 새 작업은를 지원 하 `Adjoint` 고, `Controlled` 기본 작업이 수행한 경우에만를 지원 합니다.
`Adjoint`함수는 자체적으로 반전 됩니다. 즉, `Adjoint Adjoint Op` 는 항상와 동일 합니다 `Op` .

#### <a name="controlled-functor"></a>`Controlled` 함수

마찬가지로에서는 `Controlled X(controls, target)` 작업에 함수를 적용 하 여 `Controlled` `X` 새 작업을 생성 하 고 해당 새 작업을 및에 적용 합니다 `controls` `target` .

> [!NOTE]
> 에서 Q# 제어 되는 버전은 항상 컨트롤의 배열을 사용 하며, 제어는 항상 계산 ( `PauliZ` ) `One` 상태 ($ \ket $)에 있는 모든 컨트롤을 기반으로 합니다 {1} .
> 제어 된 작업 이전에 적절 한 단일 작업을 제어 된 작업 이전에 적용 한 다음 제어 된 작업 후에 단일 작업의 반대을 적용 하 여 다른 상태를 기반으로 제어 합니다.
> 예를 들면 제어 된 `X` 작업 전후에 컨트롤에 작업을 적용 하면 작업에서 `Zero` 해당 기능에 대해 상태 ($ \ket $)를 제어 하 {0} 고, 상태에서 컨트롤 전후에 작업을 적용 합니다. `H` `PauliX` `One` 즉,-1 Eigenvalue는 pauli X, $ \ket {-} \mathrel{: =} (\ket {0} -\ket {1} )/\sqrt $ (상태 아님)입니다 {2} `PauliZ` `One` .

작업 식이 지정 된 경우 함수를 사용 하 여 새 작업 식을 만들 수 있습니다 `Controlled` .
새 작업의 서명은 원래 작업의 서명을 기반으로 합니다.
결과 형식은 동일 하지만 입력 형식은 두 번째 요소로 서, 컨트롤의 요소를 첫 번째 요소로 사용 하 고 원래 작업의 인수를 두 번째 요소로 보유 하 고 있는 두 번째 튜플입니다.
새 작업은 `Controlled` 를 지원 하 고, `Adjoint` 원래 작업이 수행한 경우에만를 지원 합니다.

원래 작업에 단일 인수만 사용한 경우 단일 [튜플 동등성](xref:microsoft.quantum.guide.types) 은 여기에서 재생 됩니다.
예를 들어 `Controlled X` 는 작업의 제어 된 버전입니다 `X` . 
`X` 에는 형식이 `(Qubit => Unit is Adj + Ctl)` 있으므로 `Controlled X` 형식이 있습니다 `((Qubit[], (Qubit)) => Unit is Adj + Ctl)` . 단일 튜플 동치로 인해와 동일 합니다 `((Qubit[], Qubit) => Unit is Adj + Ctl)` .

기본 작업에서 여러 인수를 사용한 경우에는 작업의 제어 되는 버전에 대 한 해당 인수를 괄호로 묶어 튜플로 변환 해야 합니다.
예를 들어 `Controlled Rz` 는 작업의 제어 된 버전입니다 `Rz` . 
`Rz` 형식에는 `((Double, Qubit) => Unit is Adj + Ctl)` `Controlled Rz` 형식이 `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)` 있습니다.
따라서는 `Controlled Rz(controls, (0.1, target))` 의 유효한 호출입니다 `Controlled Rz` (괄호로 묶인 괄호 `0.1, target` ).

또 다른 예로는를 `CNOT(control, target)` 로 구현할 수 있습니다 `Controlled X([control], target)` . 대상이 CCNOT (두 제어 비트)로 제어 되어야 하는 경우 `Controlled X([control1, control2], target)` 문을 사용 합니다.

#### `Controlled Adjoint` 

`Controlled`및 `Adjoint` 함수 commute을 적용 하는 경우에는 또는를 적용 하는 것에 차이가 없습니다 `Controlled Adjoint Op` `Adjoint Controlled Op` .


## <a name="defining-controlled-and-adjoint-implementations"></a>제어 된 및 Adjoint 구현 정의

앞의 예제에서 첫 번째 작업 선언에서 작업 및는 `BitFlip` `DecodeSuperdense` 각각 시그니처와로 정의 되었습니다 `(Qubit => Unit)` `((Qubit, Qubit) => (Result, Result))` .
`DecodeSuperdense`에는 측정값이 포함 되어 있으므로 단일 연산이 아니므로 adjoint 특수화를 제어 하지 않습니다 (해당 작업이 반환 하는 관련 요구 사항 회수 `Unit` ).
그러나는 `BitFlip` 단순히 단일 <xref:Microsoft.Quantum.Intrinsic.X> 작업을 수행 하므로 두 가지 특수화를 모두 사용 하 여 정의 했을 수 있습니다.

이 섹션에서는 작업 선언에 특수화의 존재를 포함 하 여 Q# 또는 함수와 함께 호출할 수 있는 기능을 제공 하는 방법에 대해 자세히 설명 합니다 `Adjoint` `Controlled` .
특정 특수화를 선언 하는 데 유효 하거나 유효 하지 않은 상황에 대 한 자세한 내용은이 문서에서 특수화를 올바르게 정의 하는 [상황](#circumstances-for-validly-defining-specializations) 을 참조 하세요.

작업 특성은 선언 된 작업에 적용할 수 있는 함수의 종류와 표시 되는 결과를 정의 합니다. 이러한 특수화의 존재는 작업 시그니처의 일부로 선언 될 수 있으며, 특히 작업 특성이 포함 된 주석 (, 또는)을 통해 선언할 수 있습니다 `is Adj` `is Ctl` `is Adj + Ctl` .
각 특수화의 실제 구현은 *암시적* 또는 *명시적으로* 정의 될 수 있습니다.

### <a name="implicitly-specifying-implementations"></a>암시적으로 구현 지정

이 경우 작업 선언의 본문은 기본 구현 으로만 구성 됩니다. 예를 들면 다음과 같습니다.

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```
여기에서 암시적으로 선언 된 각 특수화에 해당 하는 구현은 `Adjoint` 또는 함수 사용 될 경우 컴파일러에 의해 자동으로 생성 됩니다 `Controlled` .

따라서를 호출 하면의 `Adjoint PrepareEntangledPair` adjoint와 adjoint의를 구현 하는 컴파일러가 생성 됩니다 `CNOT` `H` .
이러한 개별 작업은 둘 다 자체 작업 이므로 결과 `Adjoint PrepareEntangledPair` 작업은 단순히 적용 되 고 그 다음으로 구성 됩니다 `CNOT(here, there)` `H(here)` .
따라서이를 사용 하면 `DecodeSuperdense` adjoint의를 사용 하 여 `PrepareEntangledPair` entangled 상태를 조밀로 다시 변환 하는 방법으로 앞의 예제에서를 작성할 수 있습니다.

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

선언에서 작업 특성이 포함 된 주석은 컴파일러가 기본 구현을 기반으로 하 여 다른 특수화를 자동으로 생성 하는지 확인 하는 데 유용 합니다. 

함수와 함께 사용 하기 위한 작업을 디자인할 때 고려해 야 할 몇 가지 중요 한 제한이 있습니다.
다른 작업의 출력 값을 사용 하는 작업에 대 한 특수화는 컴파일러에서 자동으로 생성할 수 *없습니다* . 이러한 작업에서 문을 다시 정렬 하 여 동일한 효과를 얻는 방법은 모호 합니다.

따라서 다양 한 구현을 명시적으로 지정 하는 것이 유용한 경우가 많습니다.

### <a name="explicitly-specifying-implementations"></a>명시적으로 구현 지정

컴파일러가 구현을 생성할 수 없는 경우 명시적으로 지정할 수 있습니다. 이러한 명시적 특수화 선언은 적절 한 *세대 지시문* 또는 사용자 정의 구현으로 구성 될 수 있습니다.
다음은 명시적 특수화의 몇 가지 예를 포함 한 모든 범위의 전체 범위입니다. 


#### <a name="explicit-specialization-declarations"></a>명시적 특수화 선언

Q# 작업에는 다음과 같은 명시적 특수화 선언이 포함 될 수 있습니다.

- `body`특수화는 함수 적용 되지 않은 작업의 구현을 지정 합니다.
- `adjoint`특수화는 적용 된 함수를 사용 하 여 작업의 구현을 지정 합니다 `Adjoint` .
- `controlled`특수화는 적용 된 함수를 사용 하 여 작업의 구현을 지정 합니다 `Controlled` .
- `controlled adjoint`특수화는 `Adjoint` 및 함수 적용 된 작업의 구현을 지정 합니다 `Controlled` .
  두 함수 commute 이므로이 특수화의 이름을 지정할 수도 있습니다 `adjoint controlled` .


작업 특수화는 특수화 태그 (예 `body` `adjoint` : 또는)와 다음 중 하나가 됩니다.

- 다음에 설명 된 명시적 선언입니다.
- 다음 중 하나에 해당 하는 특수화를 생성 하는 *방법을* 컴파일러에 지시 하는 *지시문* 입니다.
  - `intrinsic`-대상 컴퓨터가 특수화를 제공 함을 나타냅니다.
  - `distribute`및 특수화와 함께 `controlled` 사용 `controlled adjoint` 됩니다.
    에서 사용 하는 경우 `controlled` 컴파일러는의 `Controlled` 모든 작업에를 적용 하 여 특수화를 계산 해야 함을 나타냅니다 `body` .
    과 함께 사용 하는 경우 `controlled adjoint` `Controlled` 특수화의 모든 작업에를 적용 하 여 컴파일러가 특수화를 계산 해야 함을 나타냅니다 `adjoint` .
  - `invert`. 예를 들어 `adjoint` `body` 작업 순서를 반대로 하 고 각각에 adjoint를 적용 하 여 컴파일러가 특수화를 계산 해야 함을 나타냅니다.
    이는와 함께 사용 될 때 `adjoint controlled` 컴파일러가 특수화를 반전 하 여 특수화를 계산 해야 함을 나타냅니다 `controlled` .
  - `self`-adjoint 특수화가 특수화와 동일 함을 표시 `body` 합니다.
    `self`및 특수화에는를 사용할 수 `adjoint` `adjoint controlled` 있습니다.
    의 `adjoint controlled` 경우 `self` `adjoint controlled` 특수화가 특수화와 동일 함을 의미 합니다 `controlled` .
  - `auto`-컴파일러가 적용할 적절 한 지시문을 선택 하도록 지정 합니다.
    특수화에는를 사용할 수 없습니다 `auto` `body` .

지시문과 모두에는 `auto` 닫는 세미콜론이 필요 `;` 합니다.
`auto`의 명시적 선언이 제공 되는 경우 지시문은 다음과 같이 생성 된 지시문으로 확인 `body` 됩니다.

- `adjoint`특수화는 지시문에 따라 생성 `invert` 됩니다.
- `controlled`특수화는 지시문에 따라 생성 `distribute` 됩니다.
- `adjoint controlled`특수화는 `invert` 에 대 한 명시적 선언이 `controlled` 지정 되었지만에 대해 지정 되지 않은 경우 지시문에 따라 생성 되 `adjoint` 고 그렇지 않은 경우에는 `distribute` 입니다.

> [!TIP]   
> 작업이 자체 adjoint 인 경우 생성 지시문을 통해 adjoint 또는 제어 된 adjoint 특수화를 명시적으로 지정 `self` 하 여 컴파일러가 최적화를 위해 해당 정보를 사용할 수 있도록 합니다.

사용자 정의 구현을 포함 하는 특수화 선언은 인수 튜플 및 Q# 특수화를 구현 하는 코드를 포함 하는 문 블록으로 구성 됩니다.
인수 목록에서 `...` 은 작업에 대해 전체적으로 선언 된 인수를 나타내는 데 사용 됩니다.
및의 경우 `body` `adjoint` 인수 목록은 항상 이어야 합니다 `(...)` . 및의 `controlled` 경우 `adjoint controlled` 인수 목록은 컨트롤의 배열을 나타내는 기호 여야 합니다 ( `...` 예:) `(controls,...)` .

### <a name="examples"></a>예

작업 선언은 다음과 같이 간단할 수 있습니다 .이는 기본 Pauli X 작업을 정의 합니다.

```qsharp
operation X (qubit : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```
Pauli X 작업의 adjoint는 `self` 정의에 따라 고유한 역함수 이기 때문에 지시문을 사용 하 여 정의 됩니다 `X` .

이전 예제에서 `PrepareEntangledPair` 코드는 명시적 특수화 선언이 포함 된 다음 코드와 동일 합니다. 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    adjoint auto; // auto-generate adjoint specialization
    controlled auto; // auto-generate controlled specialization
    controlled adjoint auto; // auto-generate controlled adjoint specialization
}
```
키워드는 `auto` 컴파일러가 특수화 구현을 생성 하는 방법을 결정 해야 함을 나타냅니다.

#### <a name="user-defined-specialization-implementation"></a>사용자 정의 특수화 구현

컴파일러가 특정 특수화에 대 한 구현을 자동으로 생성할 수 없거나 보다 효율적인 구현을 제공할 수 있는 경우에는 구현을 수동으로 정의할 수 있습니다.

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user-defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```
이전 예제에서는 `adjoint invert;` 본문 구현을 반전 하 여 adjoint 특수화를 생성 하 고, 제어 된 `controlled adjoint invert;` 특수화의 지정 된 구현을 반전 하 여 제어 된 adjoint 특수화가 생성 됨을 나타냅니다.

기본 본문 외에도 하나 이상의 특수화를 명시적으로 선언 해야 하는 경우 기본 본문의 구현은 적절 한 특수화 선언에도 래핑해야 합니다.

```qsharp
operation CountOnes(qubits: Qubit[]) : Int {

    body (...) // default body specialization
    {
        mutable n = 0;
        for (qubit in qubits) {
            set n += M(q) == One ? 1 | 0;
        }
        return n;
    }

    ...
```

### <a name="circumstances-for-validly-defining-specializations"></a>특수화를 유효 하 게 정의 하는 상황

#### <a name="operation-declarations-with-adjointcontrolled"></a>Adjoint/제어를 사용 하는 작업 선언

Adjoint 또는 제어 된 버전이 없는 작업을 지정 하는 것은 유효 합니다. 예를 들어, 측정 작업은 역 변환할 수 없거나 제어할 수 없기 때문에 없습니다.

작업은 선언에 `Adjoint` `Controlled` 각 특수화의 암시적 또는 명시적 선언이 포함 된 경우 및 함수을 지원 합니다.

명시적으로 선언 된 adjoint/제어 된 특수화는 adjoint/제어 된 특수화의 존재를 의미 합니다. 

본문이-success 루프, set 문, 측정값, return 문 또는 함수를 지원 하지 않는 다른 작업에 대 한 호출을 포함 하는 작업의 경우 `Adjoint` 또는 지시문 다음에 adjoint 특수화 자동 생성을 `invert` `auto` 수행할 수 없습니다.

해당 본문에서 함수를 지원 하지 않는 다른 작업에 대 한 호출을 포함 하는 작업의 경우 `Controlled` 또는 지시문 다음에 제어 된 특수화를 자동으로 생성할 `distribute` `auto` 수 없습니다.

#### <a name="controlled-adjoint"></a>제어 된 Adjoint

작업의 제어 된 adjoint 버전은 작업의 adjoint의 퀀텀 제어 버전을 구현 하는 방법을 지정 합니다.
제어 된 adjoint 버전이 없는 작업을 지정 하는 것은 유효 합니다. 예를 들어, 측정 작업은 제어 또는 반전할 수 없기 때문에 제어 되는 adjoint 버전이 없습니다.

작업에 대 한 제어 된 adjoint 특수화는 adjoint와 제어 된 특수화가 모두 있는 경우에만 존재 해야 합니다. 이 경우 제어 된 adjoint 특수화의 존재 여부가 유추 됩니다. 명시적으로 정의 된 구현이 없는 경우 컴파일 시 적절 한 특수화가 생성 됩니다.

해당 본문에 제어 된 adjoint 버전이 없는 다른 작업에 대 한 호출이 포함 된 작업의 경우, 또는 지시문 다음에 나오는 adjoint 특수화를 자동으로 생성할 `invert` `distribute` `auto` 수 없습니다.


### <a name="type-compatibility"></a>형식 호환성

모든 위치에서 지원 되는 추가 함수와 함께 작업을 사용 합니다 .이 작업은 함수 더 적거나 동일한 서명을 사용 합니다. 예를 들어 형식의 작업을 사용 하는 모든 위치에서 형식의 작업을 사용 `(Qubit => Unit is Adj)` `(Qubit => Unit)` 합니다.

Q#는 호출 가능 반환 형식과 관련 하 여 *공변 (covariant* )이 있습니다. 형식을 반환 하는 호출 가능은 `'A` 동일한 입력 형식 및와 호환 되는 결과 형식으로 호출할 수 있는와 호환 됩니다. `'A`

Q# 입력 형식과 관련 하 여 *반공 변 (contravariant* ): 형식을 입력으로 사용 하는 호출할 수 있는는 `'A` 동일한 결과 형식 및와 호환 되는 입력 형식으로 호출할 수 있는와 호환 됩니다 `'A` .

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

당신은 할 수 있어요

- `ConjugateInvertWith`또는의 인수를 사용 하 여 함수를 호출 합니다 `inner` `Invert` `ApplyUnitary` .
- `ConjugateUnitaryWith`의 인수를 사용 하 여 함수를 호출 `inner` `ApplyUnitary` `Invert` 합니다.
- 에서 형식의 값을 반환 `(Qubit[] => Unit is Adj + Ctl)` `ConjugateInvertWith` 합니다.

> [!IMPORTANT]
> Q# 0.3에서는 사용자 정의 형식의 동작에 상당한 차이점이 도입 되었습니다.

사용자 정의 형식은 하위 형식이 아니라 기본 형식의 래핑된 버전으로 취급 됩니다.
이는 기본 형식의 값이 인 것으로 간주 되는 사용자 정의 형식의 값을 사용할 수 없음을 의미 합니다.


## <a name="defining-new-functions"></a>새 함수 정의

함수는 순수 하 게 결정적 이며,이 루틴은 Q# 출력 값을 계산 하는 것 이상의 효과를 허용 하지 않는 작업과는 다릅니다.
특히 함수는 작업을 호출할 수 없습니다. 작업 수행, 할당 또는 적용 샘플 난수 또는 함수에 대 한 입력 값 이상의 상태에 종속 됩니다.
결과적으로 함수는 Q# 항상 동일한 입력 값을 동일한 출력 값에 매핑하기 때문에 *순수* 합니다.
이 동작을 통해 Q# 컴파일러는 작업 특수화를 생성할 때 함수를 호출 하는 방법 및 시기를 안전 하 게 다시 정렬할 수 있습니다.

각 Q# 소스 파일은 원하는 수의 함수를 정의할 수 있습니다.
함수 이름은 네임 스페이스 내에서 고유 해야 하며 작업 또는 형식 이름과 충돌할 수 없습니다.

함수 정의는 함수에 대해 adjoint 또는 제어 된 특수화를 정의할 수 없다는 점을 제외 하 고 작업을 정의 하는 것과 유사 하 게 작동 합니다.
예:

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```

또는 

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

### <a name="classical-logic-in-functions--good"></a>함수의 기존 논리 = = 양호

이렇게 할 수 있는 경우에는 작업 보다 더 쉽게 사용할 수 있도록 함수 대신 함수를 사용 하 여 기존 논리를 작성 하는 것이 유용 합니다. 예를 들어 이전 `Square` 선언을 *작업* 으로 작성 한 경우 컴파일러는 동일한 입력을 사용 하 여 호출 하는 것이 일관 되 게 동일한 출력을 생성 하도록 보장할 수 없습니다.

함수와 작업 사이의 차이를 표시 하려면 작업 내에서 난수를 샘플링 하 여 일반적으로 문제를 고려해 야 합니다 Q# .

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

`U`가 호출 될 때마다에 대해 다른 작업을 수행 `target` 합니다.
특히 특수화 선언을에 추가 하는 경우 컴파일러는 `adjoint auto` `U` `U(target); Adjoint U(target);` id (즉, op)로 작동 하도록 보장할 수 없습니다.
이는 [벡터 및 행렬](xref:microsoft.quantum.concepts.vectors)에 정의 된 adjoint의 정의를 위반 합니다. 즉, 컴파일러가 작업을 호출 하는 작업에서 adjoint 특수화를 자동으로 생성 하 여 <xref:Microsoft.Quantum.Math.RandomReal> 컴파일러에서 제공 하는 보증을 중단 하는 것과 같이 <xref:Microsoft.Quantum.Math.RandomReal> adjoint 또는 제어 된 버전이 없는 작업입니다.

반면,와 같은 함수 호출을 안전 하 게 허용 하 `Square` 고 `Square` 출력을 안정적으로 유지 하기 위해 입력을 유지 해야 한다는 것을 컴파일러에 게 보장 합니다.
따라서 함수에서 최대한 많은 고전 논리를 격리 하면 다른 함수와 작업에서 해당 논리를 쉽게 다시 사용할 수 있습니다.


## <a name="generic-type-parameterized-callables"></a>제네릭 (형식 매개 변수화 된) Callables

정의할 수 있는 많은 함수와 연산은 실제로 해당 입력의 형식에 의존 하지 않고 다른 함수 또는 작업을 통해서만 암시적으로 해당 형식을 사용 합니다.
예를 들어 많은 기능 언어에 공통적인 *map* 개념을 살펴보겠습니다. 함수 $f (x) $ 및 값 $ \{ x_1, x_2, \dots, x_n \} $, map이 지정 된 경우 새 컬렉션 $ \{ f (x_1), f (x_2), \ 점, f (x_n) $를 반환 합니다 \} .
에서이를 구현 하려면 Q# 함수가 첫 번째 클래스 라는 사실을 활용 합니다.
`Map` `T` 필요한 형식을 확인 하는 동안를 자리 표시자로 사용 하는 간단한 예제는 다음과 같습니다.

```qsharp
function Map(fn : (T -> T), values : T[]) : T[] {
    mutable mappedValues = new T[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

이 함수는에서 대체 하는 실제 형식에 관계 없이 거의 동일 하 게 보입니다.
예를 들어 정수에서 Paulis의 맵은 부동 소수점 숫자에서 문자열로의 맵과 거의 같습니다.

```qsharp
function MapIntsToPaulis(fn : (Int -> Pauli), values : Int[]) : Pauli[] {
    mutable mappedValues = new Pauli[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}

function MapDoublesToStrings(fn : (Double -> String), values : Double[]) : String[] {
    mutable mappedValues = new String[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

원칙적으로는 `Map` 발생 하는 모든 형식 쌍에 대해의 버전을 작성할 수 있지만이 경우 여러 가지 문제가 발생 합니다.
예를 들어에서 버그를 발견 한 경우에는 `Map` 모든 버전의에서 일관 되 게 수정 사항을 적용 해야 합니다 `Map` .
또한 새 튜플 또는 UDT를 생성 하는 경우 새 형식과 함께 새를 구성 해야 합니다 `Map` .
이러한 함수는 약간의 이러한 기능을 다루기가 하지만,와 동일한 폼의 더 많은 함수를 수집 하는 경우 `Map` 새 형식을 도입 하는 비용은 매우 짧은 순서로 지나치게 길면 커집니다.

그러나 이러한 어려움의 대부분은 서로 다른 버전의와 관련 된 방법을 인식 하는 데 필요한 정보를 컴파일러에 제공 하지 않았기 때문에 발생 `Map` 합니다.
효과적으로 컴파일러에서 `Map` Q# *형식* 에서 함수로 함수를 일종의 수학적 함수로 처리 하려고 합니다 Q# .

Q# 는 함수 및 작업에 *형식 매개 변수와* 일반적인 튜플 매개 변수를 포함 하도록 허용 하 여이 개념을 공식화 합니다.
앞의 예제에서는 `Map` `Int, Pauli` 첫 번째 경우와 두 번째 경우에 형식 매개 변수를 포함 한다고 생각 합니다 `Double, String` .
대부분의 경우 이러한 형식 매개 변수를 일반적인 형식인 것 처럼 사용 합니다. 형식 매개 변수 값을 사용 하 여 배열 및 튜플을 만들고, 함수 및 작업을 호출 하 고, 일반 변수 또는 변경 가능한 변수에 할당 합니다.

> [!NOTE]
> 간접적 종속성의 가장 극단적인 경우는 Q# 프로그램에서 형식의 구조를 직접 사용할 수 `Qubit` 없지만 이러한 형식을 다른 작업 및 함수에 전달 **해야** 하는 것입니다.

이전 예제로 돌아가면에서 입력을 `Map` 나타내는 형식 매개 변수와 출력을 나타내는 하나를 표시 하는 형식 매개 변수가 있어야 합니다 `fn` `fn` .
에서는 Q# `<>` {} 선언에서 함수 또는 작업 이름 뒤에 꺾쇠 괄호 (brakets $ \braket $!)를 추가 하 고 각 형식 매개 변수를 나열 하 여이를 작성 합니다.
각 형식 매개 변수의 이름은 틱으로 시작 해야 `'` 하며 일반 형식 ( *구체적* 형식이 라고도 함)이 아니라 형식 매개 변수 임을 나타냅니다.
따라서 `Map` 는 다음과 같이 작성 됩니다.

```qsharp
function Map<'Input, 'Output>(fn : ('Input -> 'Output), values : 'Input[]) : 'Output[] {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

의 정의는 `Map<'Input, 'Output>` previoius 버전과 매우 유사 하 게 보입니다.
유일한 차이점은 컴파일러에 직접 의존 하지 않는 컴파일러에 명시적으로 알리는 것이 `Map` `'Input` 고 `'Output` ,이를 간접적으로 사용 하 여 두 가지 형식에 대해 작동 `fn` 한다는 것입니다.
이러한 방식으로를 정의한 후 `Map<'Input, 'Output>` 에는 일반적인 함수 처럼 호출할 수 있습니다.

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> 제네릭 함수 및 작업을 작성 하는 것은 함수 및 작업에 대해 생각 하는 데 매우 유용한 방법입니다 Q# .
> 모든 함수는 정확히 하나의 입력을 사용 하 고 정확히 하나의 출력을 반환 하므로 형식의 입력은 `'T -> 'U` *모든* Q# 함수와 일치 합니다.
> 마찬가지로 형식의 입력에 작업을 전달할 수 있습니다 `'T => 'U` .

두 번째 예는 다른 두 함수의 컴퍼지션을 반환 하는 함수를 작성 하는 것입니다.

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

여기에서, 및가 무엇 인지 정확 하 게 지정 해야 `A` `B` `C` 하므로 새 함수의 유틸리티를 심각 하 게 제한 합니다 `Compose` .
그 후에는 `Compose` 및를 `A` 통해, 및에만 의존 `B` `C` *via* `innerFn` `outerFn` 합니다.
또는 `Compose` *any* `A` `B` `C` 이러한 매개 변수가 및에서 예상한 것과 일치 하는 경우, 및에 대해 작동 함을 나타내는 `innerFn` 형식 매개 변수를에 추가할 수 있습니다 `outerFn` .

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

Q#표준 라이브러리는 이러한 형식의 매개 변수가 있는 작업 및 함수를 제공 하 여 더 높은 순서 제어 흐름을 보다 쉽게 표현할 수 있도록 합니다.
이러한 내용은 [ Q# 표준 라이브러리 가이드](xref:microsoft.quantum.libraries.standard.intro)에 자세히 설명 되어 있습니다.


## <a name="callables-as-first-class-values"></a>First-Class 값으로 callables

작업 대신 함수를 사용 하는 제어 흐름과 기존 논리를 추론 하는 한 가지 중요 한 기술은의 작업 및 함수를 활용 하는 것입니다 Q# . *first-class*
즉, 해당 언어의 각 값은 고유한 권한입니다.
예를 들어, 약간의 간접적인 경우 다음과 같은 코드는 완벽 하 게 유효 합니다 Q# .

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

`ourH`이전 코드 조각의 변수 값은 <xref:Microsoft.Quantum.Intrinsic.H> 다른 작업 처럼 해당 값을 호출할 수 있도록 하는 작업입니다.
이 기능을 사용 하면 작업을 수행 하는 작업을 작성 하 여 고차 제어 흐름 개념을 형성할 수 있습니다.
예를 들어 동일한 대상의 동일한 대상에 두 번 적용 하 여 작업을 "제곱" 하는 것을 생각해 볼 수 있습니다.

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

### <a name="returning-operations-from-a-function"></a>함수에서 작업 반환

작업을 출력의 일부로 반환 하는 것이 중요 합니다. 예를 들어 작업 형식으로 퀀텀 프로그램에 대 한 설명을 반환 하는 클래식 함수로 일부 종류의 클래식 조건부 논리를 격리할 수 있습니다.
간단한 예로, 2 비트 클래식 메시지를 수신 하는 파티가 메시지를 사용 하 여 해당 teleportation를 적절 한 teleported 상태로 디코딩하는 경우를 예로 들어 보겠습니다.
이러한 두 개의 기존 비트를 사용 하 고 적절 한 디코딩 작업을 반환 하는 함수를 기준으로이를 작성할 수 있습니다.

```qsharp
function TeleporationDecoderForMessage(hereBit : Result, thereBit : Result)
: (Qubit => Unit is Adj + Ctl) {

    if (hereBit == Zero && thereBit == Zero) {
        return I;
    } elif (hereBit == One && thereBit == Zero) {
        return X;
    } elif (hereBit == Zero && thereBit == One) {
        return Z;
    } else {
        return Y;
    }
}
```

이 새로운 함수는 실제로 함수 이며, 같은 값을 사용 하 여이 함수를 호출 하는 경우 `hereBit` `thereBit` 항상 동일한 작업을 반환 합니다.
따라서 디코딩 논리가 다른 작업 특수화의 정의와 상호 작용 하는 방법에 대해 설명 하지 않고도 디코더를 작업 내에서 안전 하 게 실행할 수 있습니다.
즉, 함수 내의 기존 논리가 격리 되므로 입력이 유지 되는 한, 함수 호출을 사용 하 여 함수 호출을 사용할 수 있습니다.


## <a name="partial-application"></a>부분 응용 프로그램

*부분 응용 프로그램* 을 사용 하 여 작업을 반환 하는 함수를 사용 하 여 작업을 반환 하는 함수를 사용 하 여 더 많은 작업을 수행할 수 있습니다. 이러한 함수는 실제로 호출 하지 않고 함수 또는 작업에 입력의 앞의 예제에서 입력 작업을 적용 해야 하는 것을 즉시 지정 하지 않으려는 경우를 `ApplyTwice` 나타낼 수 있습니다.

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

이 경우 지역 변수는 `twiceOp` 부분적으로 적용 된 작업을 보유 합니다 `ApplyTwice(op, _)` . 여기서는 `_` 아직 지정 되지 않은 입력 부분을 나타냅니다.
`twiceOp`다음 줄에서를 호출 하는 경우 입력의 나머지 부분을 모두 원래 작업에 적용 하 여 부분적으로 적용 된 작업에 입력으로 전달 합니다.
따라서 이전 코드 조각은 실제로 직접 호출 하는 것과 동일 합니다 `ApplyTwice(op, target)` . 새 지역 변수를 도입 하 여 입력의 일부를 제공 하는 동안 호출을 지연할 수 있도록 저장 합니다.

부분적으로 적용 된 작업은 전체 입력이 제공 될 때까지 실제로 호출 되지 않으므로 함수 내 에서도 작업을 부분적으로 적용할 수 있습니다.

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

원칙적으로 내에서의 기존 논리는 `SquareOperation` 훨씬 더 많은 관련이 있었지만 컴파일러가 함수에 대해 제공할 수 있는 보증을 통해 작업의 나머지 부분과 여전히 격리 되어 있습니다. Q#표준 라이브러리는 퀀텀 프로그램에서 쉽게 사용할 수 있는 방식으로 클래식 제어 흐름을 표현 하는 데이 접근 방식을 사용 합니다.


## <a name="recursion"></a>재귀

Q# callables은 직접 또는 간접적으로 재귀적으로 사용할 수 있습니다.
즉, 작업 또는 함수가 자신을 호출 하거나 호출 가능 작업을 직접 또는 간접적으로 호출 하는 다른 호출 가능 함수를 호출할 수 있습니다.

그러나 재귀 사용에 대 한 두 가지 중요 한 설명은 다음과 같습니다.

- 작업에서 재귀를 사용 하면 특정 최적화에 방해가 될 수 있습니다.
  이 간섭을 통해 알고리즘의 런타임에 상당한 영향을 줄 수 있습니다.
- 실제 퀀텀 장치에서 실행 되는 경우 스택 공간이 제한 될 수 있으므로 심층 재귀가 런타임 오류가 발생할 수 있습니다.
  특히 Q# 컴파일러와 런타임에서는 마무리 재귀를 식별 하 고 최적화 하지 않습니다.

## <a name="next-steps"></a>다음 단계

에서 [변수에](xref:microsoft.quantum.guide.variables) 대해 알아보세요 Q# .