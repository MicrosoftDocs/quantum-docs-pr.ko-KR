---
title: 'Q # 기술-작업 및 함수 | Microsoft Docs'
description: 'Q # 기술-작업 및 함수'
uid: microsoft.quantum.techniques.opsandfunctions
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 06da09dc9c6e0ba0331db6bc0cd3d2ddeb287113
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183457"
---
# <a name="q-operations-and-functions"></a>Q # 작업 및 함수

Q # 프로그램은 퀀텀 작업이 퀀텀 데이터에 대해 가질 수 있는 부작용을 설명 하는 하나 이상의 *작업* 으로 구성 되며, 기존 데이터를 수정할 수 있도록 하는 하나 이상의 *함수* 를 포함 합니다. 연산과 달리 함수는 순수 하 게 모든 동작을 설명 하는 데 사용 되며 클래식 출력 값을 계산 하는 것 외에 영향을 주지 않습니다.

Q #에 정의 된 각 작업은 해당 언어로 정의 된 기본 제공 기본 작업을 포함 하 여 원하는 수의 다른 작업을 호출할 수 있습니다. 이러한 내장 작업이 정의 되는 특정 방법은 대상 컴퓨터에 따라 다릅니다. 컴파일되는 경우 각 작업은 대상 컴퓨터에 제공할 수 있는 .NET 클래스 형식으로 표시 됩니다.

## <a name="defining-new-operations"></a>새 작업 정의

위에서 설명한 것 처럼 Q #으로 작성 된 퀀텀 프로그램의 가장 기본적인 빌딩 블록은 작업입니다 .이는 기존 .NET 응용 프로그램에서 호출할 수 있는 *작업*입니다. 예를 들어 시뮬레이터를 사용 하거나 q # 내의 다른 작업을 수행할 수 있습니다.
각 작업은 입력을 가져오고, 출력을 생성 하 고, 하나 이상의 작업 특수화에 대해 구현을 지정 합니다.
예를 들어, 다음 작업은 기본 본문 특수화만 정의 하 고 단일 비트를 입력으로 사용 하 고 해당 입력에 대해 기본 제공 `X` 작업을 호출 합니다.

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

`operation` 키워드는 작업 정의를 시작 하 고 뒤에 이름이 옵니다. 여기에서 `BitFlip`합니다.
그런 다음 입력의 형식은 새 작업 내의 입력을 참조 하는 이름 `target`와 함께 `Qubit`로 정의 됩니다.
마찬가지로 `Unit`는 작업의 출력이 비어 있음을 정의 합니다.
이는 및 기타 명령적 언어에서 C# `void` 하는 경우와 비슷하게 사용 되며 및 다른 기능 F# 언어의 `unit`와 동일 합니다.

> [!NOTE]
> 이 내용은 아래에 자세히 설명 되어 있지만, Q #의 각 작업은 정확히 하나의 입력을 사용 하 고 정확히 하나의 출력을 반환 합니다.
> 그런 다음 여러 개의 값을 단일 값으로 수집 하는 *튜플을*사용 하 여 여러 입력 및 출력을 나타냅니다.
> 비공식적으로 Q #은 "튜플 인 튜플" 언어 라고 합니다.
> 이 개념에 따라 `()` `Unit`형식이 있는 "빈" 튜플로 읽어야 합니다.

새 작업 내에서 기본 본문 특수화의 구현만 명시적으로 지정 해야 하는 경우 선언 내에서 직접 구현을 지정할 수 있습니다. 또한 아래에서 구체화 된 하나 이상의 `functor` 작업 등의 구현을 정의할 수 있습니다. 위의 예제에서 유일한 문은 <xref:microsoft.quantum.intrinsic.x>기본 제공 Q # 작업을 호출 하는 것입니다.

작업은 `Unit`보다 더 흥미로운 형식을 반환할 수도 있습니다.
예를 들어 <xref:microsoft.quantum.intrinsic.m> 작업은 측정을 수행 하는 것을 나타내는 `Result`형식의 출력을 반환 합니다. 작업의 출력을 다른 작업으로 전달 하거나 `let` 키워드와 함께 사용 하 여 새 변수를 정의할 수 있습니다.
<!-- Link to UID for superdense conceptual and example documentation. -->
이를 통해 슈퍼 조밀한 코딩의 경우와 같이 낮은 수준에서 퀀텀 작업과 상호 작용 하는 기존 계산을 나타낼 수 있습니다.

```qsharp
operation Superdense(here : Qubit, there : Qubit) : (Result, Result) {

    CNOT(there, here);
    H(there);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```
### <a name="functors-adjoint-and-controlled"></a>함수, adjoint 및 제어 됨
작업에서 단일 변환을 구현 하는 경우 *adjointed* 또는 *제어*될 때 작업이 작동 하는 방식을 정의할 수 있습니다. 작업의 adjoint 특수화는 역방향으로 실행 될 때 작동 하는 방식을 지정 하는 반면, 제어 된 특수화는 퀀텀 레지스터의 상태에 조건 화 된 적용 될 때 작업이 작동 하는 방식을 지정 합니다.
이러한 특수화의 존재는 다음 예제에서 `is Adj + Ctl` 작업 시그니처의 일부로 선언할 수 있습니다. 이렇게 암시적으로 선언 된 각 특수화에 해당 하는 구현은 컴파일러에 의해 생성 됩니다. 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit {
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```

> [!NOTE]
> Q #의 많은 작업은 단일 게이트를 나타냅니다.
> $U $가 작업 `U`으로 표시 되는 단일 게이트가 면 `Adjoint U`는 단일 게이트 $U ^ \a와 $를 나타냅니다.

컴파일러가 구현을 생성할 수 없는 경우에는 명시적으로 지정할 수 있습니다. 이러한 명시적 특수화 선언은 적절 한 세대 지시문 또는 사용자 정의 구현으로 구성 될 수 있습니다. 위의 `PrepareEntangledPair` 코드는 다음 코드와 같이 명시적 특수화 선언이 포함 된 코드와 같습니다. 

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
컴파일러가 특정 특수화의 구현을 자동으로 생성할 수 없는 경우 또는 보다 효율적인 구현을 제공할 수 있는 경우에는 구현을 수동으로 정의할 수도 있습니다.

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

이에 대 한 더 많은 예제는 [고차 제어 흐름](xref:microsoft.quantum.concepts.control-flow)에서 볼 수 있습니다.

작업의 특수화를 호출 하려면 `Adjoint` 또는 `Controlled` 키워드를 사용 합니다.
예를 들어, 위의 슈퍼 조밀한 코딩 예는 조밀 `PrepareEntangledPair`의 adjoint를 사용 하 여 entangled 상태를 a비트의 unentangled 쌍으로 다시 변환 하 여 더 많은를 작성할 수 있습니다.

```qsharp
operation Superdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

함수와 함께 사용 하기 위한 작업을 디자인할 때 고려해 야 할 몇 가지 중요 한 제한이 있습니다.
다른 작업의 출력 값을 사용 하는 작업에 대 한 특수화는 컴파일러에서 자동으로 생성할 수 없습니다. 이러한 작업에서 문을 다시 정렬 하 여 동일한 효과를 얻는 방법은 모호 합니다.


## <a name="defining-new-functions"></a>새 함수 정의

Q #에서는 출력 값을 계산 하는 것 보다는 효과를 가질 수 없다는 점에서 작업과는 다른 *함수*를 정의할 수도 있습니다.
특히 함수는 작업을 호출 하거나,이 함수를 호출할 수 없으며, 난수를 샘플링 하거나, 함수에 대 한 입력 값 이상으로 상태에 의존 하지 않습니다.
결과적으로 Q # 함수는 항상 동일한 입력 값을 동일한 출력 값에 매핑하기 때문에 *순수*합니다.
이를 통해 Q # 컴파일러는 작업 특수화를 생성할 때 함수가 호출 되는 방법 및 시기를 안전 하 게 다시 정렬할 수 있습니다.

함수 정의는 함수에 대해 adjoint 또는 제어 된 특수화를 정의할 수 없다는 점을 제외 하 고 작업을 정의 하는 것과 유사 하 게 작동 합니다.
예를 들면 다음과 같습니다.

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```
이러한 작업을 수행할 수 있는 경우 작업 내에서 보다 쉽게 사용할 수 있도록 작업 대신 함수를 기준으로 기존 논리를 작성 하는 것이 좋습니다.
예를 들어 `Square`를 작업으로 작성 한 경우 컴파일러는 동일한 입력을 사용 하 여 호출 하는 것이 일관 되 게 동일한 출력을 생성 하도록 보장할 수 없습니다.

함수 및 작업 간의 차이를 표시 하려면 Q # 작업 내에서 난수를 샘플링 하는 것과 관련 된 문제를 일반적으로.

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

`U`가 호출 될 때마다 `target`에서 다른 작업이 수행 됩니다.
특히 컴파일러는 `U(target); Adjoint U(target);` `U`에 `adjoint auto` 특수화 선언을 추가한 경우 id (즉, op)로 작동 하도록 보장할 수 없습니다.
이는 [벡터 및 행렬](xref:microsoft.quantum.concepts.vectors)에서 보았던 adjoint의 정의를 위반 하 여, 작업 <xref:microsoft.quantum.math.randomreal> 호출한 작업에서 adjoint 특수화를 자동으로 생성할 수 있도록 하 여 컴파일러에서 제공 하는 보증을 중단 합니다. ; <xref:microsoft.quantum.math.randomreal>는 adjoint 또는 제어 된 버전이 존재 하지 않는 작업입니다.

반면에 `Square`와 같은 함수 호출을 안전 하 게 사용할 수 있다는 것은 컴파일러가 출력을 안정적으로 유지 하기 위해 `Square` 입력을 유지 해야 한다는 것을 확신할 수 있다는 것입니다.
따라서 함수에서 최대한 많은 고전 논리를 격리 하면 다른 함수와 작업에서 해당 논리를 쉽게 다시 사용할 수 있습니다.

## <a name="control-flow"></a>제어 흐름

작업 또는 함수 내에서 각 문은 순서 대로 실행 되며 가장 일반적인 명령적 언어와 비슷합니다.
그러나이 제어 흐름은 다음과 같은 세 가지 방법으로 수정할 수 있습니다.

- `if` 문
- `for` 루프
- `repeat`-`until` 루프

[성공 (RUS) 회로까지 반복](xref:microsoft.quantum.techniques.qubits#measurements) 에 대해 논의할 때까지 후자의 토론을 연기 합니다.
그러나 `if` 및 `for` 제어 흐름 구문은 대부분의 일반적인 프로그래밍 언어에 대해 잘 알고 있습니다.
특히 `if` 문은 조건을 사용할 수 있으며 그 뒤에 하나 이상의 `elif` 문이 올 수 있으며 `else`으로 끝날 수 있습니다.

```qsharp
if (pauli == PauliX) {
    X(qubit);
} elif (pauli == PauliY) {
    Y(qubit);
} elif (pauli == PauliZ) {
    Z(qubit);
} else {
    fail "Cannot use PauliI here.";
}
```

마찬가지로 `for` 루프는 정수 범위 또는 배열의 요소에 대 한 반복을 표시 합니다.

```qsharp
for (idxQubit in 0..nQubits - 1) {
    // Do something to idxQubit...
}
```

중요 한 것은 특수화가 자동 생성 되는 작업에도 `for` 루프 및 `if` 문을 사용할 수 있다는 것입니다. 이 경우 `for` 루프의 adjoint는 방향을 바꾸고 각 반복의 adjoint를 사용 합니다.
이는 "신발 및 socks" 원칙을 따릅니다. 즉, socks에 배치를 취소 한 다음 신발로 전환 하려면 축구 전환에 대 한 실행을 취소 하 고 socks에 배치를 실행 취소 해야 합니다.
계속 해 서 신발를 decidedly 하는 동안 시도 하 고 socks를 사용 하지 않는 것이 좋습니다.

## <a name="operations-and-functions-as-first-class-values"></a>작업 및 함수를 첫 번째 클래스 값으로

작업 대신 함수를 사용 하는 제어 흐름과 기존 논리를 추론 하는 한 가지 중요 한 기술은 Q #의 해당 작업 및 함수를 *첫 번째 클래스*에 사용 하는 것입니다.
즉, 해당 언어의 각 값은 고유한 권한입니다.
예를 들어, 약간 간접적인 경우 다음은 완벽 하 게 유효한 Q # 코드입니다.

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

위의 코드 조각에서 `ourH` 된 변수 값은 다른 작업 처럼 해당 값을 호출할 수 있도록 하는 작업이 <xref:microsoft.quantum.intrinsic.h>됩니다.
이렇게 하면 작업을 입력의 일부로 사용 하 여 고차 제어 흐름 개념을 형성 하는 작업을 작성할 수 있습니다.
예를 들어 동일한 대상의 동일한 대상에 두 번 적용 하 여 작업을 "제곱" 하는 것을 생각해 볼 수 있습니다.

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

이 예제에서 `(Qubit => Unit)` 형식에 표시 되는 `=>` 화살표는 입력 `op` 필드가 `Qubit` 형식의 입력으로 사용 하 고 빈 튜플을 출력으로 생성 하는 작업 임을 나타냅니다.
또한 지원 되는 함수에 대 한 정보를 포함 하는 해당 작업 유형의 특성을 지정 합니다.
`(Qubit => Unit)` 형식의 연산은 `Adjoint` 및 `Controlled` 함수를 지원 하지 않습니다. `Adjoint` 함수와 같이 해당 형식의 작업에서를 지원 해야 함을 나타내려면 adjointable로 선언 해야 합니다. 이 작업은 주석 `is Adj`를 형식에 사용 하 여 수행 됩니다. 마찬가지로 `(Qubit => Unit is Ctl)`는 해당 형식의 작업이 `Controlled` 함수를 지원함을 나타냅니다. 이에 대 한 자세한 내용은 [Q #의 형식 (f:) 보다 일반적으로 살펴보겠습니다.

지금은 작업의 형태로 퀀텀 프로그램에 대 한 설명을 반환 하는 클래식 함수로 일부 종류의 클래식 조건부 논리를 격리할 수 있도록 작업을 출력의 일부로 반환할 수도 있음을 강조 합니다.
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

이 새 함수는 실제로는 함수 이며 `hereBit` 및 `thereBit`값이 같은 값을 사용 하 여 호출 하는 경우 항상 동일한 작업을 반환 합니다.
따라서 디코딩 논리가 다른 작업 특수화의 정의와 상호 작용 하는 방법에 대해 설명 하지 않고도 작업 내에서 디코더를 안전 하 게 실행할 수 있습니다.
즉, 함수 내에서 기존 논리를 격리 하 여 입력이 유지 되는 한 함수 호출이  unity를 사용 하 여 다시 정렬할 수 있도록 합니다.

함수를 고급 값으로 취급할 수도 있습니다 .이는 [작업 및 함수 형식](#operations-and-functions-as-first-class-values)에 대해 자세히 설명 합니다.

## <a name="partially-applying-operations-and-functions"></a>작업 및 함수를 부분적으로 적용

*부분 응용 프로그램*을 사용 하 여 작업을 반환 하는 함수를 사용 하 여 작업을 반환 하는 함수를 사용 하 여 훨씬 더 많은 작업을 수행할 수 있습니다. 이러한 함수는 실제로 호출 하지 않고도 함수 또는 작업에 입력 부분 예를 들어 위의 `ApplyTwice` 예제를 회수할 때 입력 작업을 적용 해야 하는 것을 즉시 지정 하지 않을 것을 나타낼 수 있습니다.

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

이 경우 지역 변수 `twiceOp` `ApplyTwice(op, _)`부분적으로 적용 된 작업을 보관 합니다. 여기서 아직 지정 하지 않은 입력 부분은 `_`표시 됩니다.
실제로 다음 줄에서 `twiceOp`를 호출 하는 경우 입력의 나머지 부분을 모두 원래 작업에 대 한 입력으로 전달 합니다.
따라서 위의 코드 조각은 실제로 `ApplyTwice(op, target)`를 직접 호출 하는 것과 동일 합니다. 즉, 입력의 일부를 제공 하는 동안 호출을 지연할 수 있는 새 지역 변수를 도입 했습니다.

부분적으로 적용 된 작업은 전체 입력이 제공 될 때까지 실제로 호출 되지 않으므로 함수 내 에서도 작업을 부분적으로 적용할 수 있습니다.

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

원칙적으로 `SquareOperation` 내의 기존 논리는 훨씬 더 많은 작업을 수행 했을 수 있지만 컴파일러에서 함수에 대해 제공할 수 있도록 보장을 통해 작업의 나머지 부분과 여전히 격리 되어 있습니다.
이 접근 방식은 퀀텀 프로그램 내에서 쉽게 사용할 수 있는 방식으로 클래식 제어 흐름을 표현 하기 위해 Q # 표준 라이브러리 전체에서 사용 됩니다.
