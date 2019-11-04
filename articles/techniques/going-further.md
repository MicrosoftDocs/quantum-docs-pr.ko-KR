---
title: 'Q # 기술-자세히 살펴보기 | Microsoft Docs'
description: 'Q # 기술-자세히 살펴보기'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4677b0f9c4f64a9c1bc46d34e8a883dc006ba8f0
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183304"
---
# <a name="going-further"></a>자세히 살펴보기 #

이제 Q #에서 흥미로운 퀀텀 프로그램을 작성 하는 방법에 대해 알아보았습니다 .이 섹션에서는 앞으로 살펴보겠습니다.

<!-- Moved Debugging and Testing Quantum Programs section to a separate article -->

## <a name="generic-operations-and-functions"></a>제네릭 작업 및 함수 ##

> [!TIP]
> 이 섹션에서는 [의 C#제네릭 ](https://docs.microsoft.com/dotnet/csharp/programming-guide/generics/introduction-to-generics), [제네릭의 F# ](https://docs.microsoft.com/dotnet/fsharp/language-reference/generics/)제네릭, [ C++ 템플릿](https://docs.microsoft.com/cpp/cpp/templates-cpp)또는 다른 언어의 메타 프로그래밍에 대 한 유사한 접근 방법에 대 한 몇 가지 기본적인 지식이 있다고 가정 합니다.

정의할 수 있는 많은 함수와 연산은 실제로 해당 입력의 형식에 의존 하지 않고 다른 함수 또는 작업을 통해서만 암시적으로 해당 형식을 사용 합니다.
예를 들어 많은 기능 언어에 공통적인 *map* 개념을 살펴보겠습니다. 함수 $f (x) $ 및 값 $\{x_1, x_2, \dots, x_n\}$, map은 새 컬렉션 $\{f (x_1), f (x_2), \dots, f ()\}$를 반환 합니다.
Q #에서이를 구현 하려면 먼저 해당 함수를 사용할 수 있습니다.
필요한 형식을 확인 하는 동안 ★를 자리 표시자로 사용 하 여 `Map`에 대 한 간단한 예제를 작성해 보겠습니다.

```qsharp
function Map(fn : ★ -> ★, values : ★[]) : ★[] {
    mutable mappedValues = new ★[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

참고이 함수는에서 대체 하는 실제 형식에 관계 없이 거의 동일 하 게 보입니다.
예를 들어 정수에서 Paulis의 맵은 부동 소수점 숫자에서 문자열로의 맵과 거의 같습니다.

```qsharp
function MapIntsToPaulis(fn : Int -> Pauli, values : Int[]) : Pauli[] {
    mutable mappedValues = new Pauli[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}

function MapDoublesToStrings(fn : Double -> String, values : Double[]) : String[] {
    mutable mappedValues = new String[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

원칙적으로는 발생 하는 모든 형식 쌍에 대 한 `Map` 버전을 작성할 수 있지만이로 인해 많은 어려움이 발생 합니다.
예를 들어 `Map`에서 버그를 발견 한 경우에는 모든 버전의 `Map`에 대해 수정이 균일 하 게 적용 되도록 해야 합니다.
또한 새 튜플 또는 UDT를 생성 하는 경우 새 형식과 함께 이동할 새 `Map`를 구성 해야 합니다.
이러한 함수는 `Map`와 동일한 폼의 더 많은 함수를 수집 하기 때문에 이러한 함수에는 다루기가 하지만 새 형식을 도입 하는 비용은 매우 짧은 순서로 지나치게 길면 커집니다.

그러나이 문제는 대부분 다른 버전의 `Map` 관련 된 방법을 인식 하는 데 필요한 정보를 컴파일러에 제공 하지 않았기 때문에 발생 합니다.
실제로 컴파일러는 Q # *형식* 에서 q # 함수로 `Map`를 일종의 수학적 함수로 처리 하려고 합니다.
이 개념은 함수 및 작업에 *형식 매개 변수*를 포함 하 고 일반적인 튜플 매개 변수를 허용 하 여 공식화 됩니다.
위의 예제에서는 첫 번째 경우에 `Int, Pauli` 형식 매개 변수를 포함 하 고 두 번째 경우에 `Double, String` `Map`를 생각해 보겠습니다.
대부분의 경우 이러한 형식 매개 변수는 일반 형식인 것 처럼 사용할 수 있습니다. 즉, 형식 매개 변수 값을 사용 하 여 배열 및 튜플을 만들고, 함수 및 작업을 호출 하 고, 일반 변수 또는 변경 가능한 변수에 할당 합니다.

> [!NOTE]
> 간접적 종속성의 가장 극단적인 경우는 Q # 프로그램이 `Qubit` 형식의 구조에 직접 의존할 수 없지만 이러한 형식을 다른 작업 및 함수에 전달 **해야** 하는 것입니다.

위의 예제로 돌아가면 형식 매개 변수를 포함 하는 `Map` 필요 합니다. 하나는 `fn` 입력을 나타내고 다른 하나는 `fn`의 출력을 나타내는 것입니다.
Q #에서는 해당 선언에서 함수 또는 작업 이름 뒤에 꺾쇠 괄호를 추가 하 고 각 형식 매개 변수를 나열 하 여이를 작성 합니다 `<>`(brakets $ \braket{}$!).
각 형식 매개 변수의 이름은 일반 형식 ( *구체적* 형식이 라고도 함)이 아니라 형식 매개 변수 임을 나타내는 틱 `'`으로 시작 해야 합니다.
`Map`의 경우 다음을 작성 합니다.

```qsharp
function Map<'Input, 'Output>(fn : 'Input -> 'Output, values : 'Input[]) : 'Output {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

`Map<'Input, 'Output>` 정의는 이전에 작성 한 버전과 매우 유사 하 게 보입니다.
유일한 차이점은 `Map` `'Input` 및 `'Output`에 직접적으로 종속 되지 않지만 `fn`를 통해 간접적으로이를 사용 하 여 두 가지 형식에 대해 작동 한다는 것입니다.
이러한 방식으로 `Map<'Input, 'Output>`를 정의 하 고 나면 일반적인 함수 처럼 호출할 수 있습니다.

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, we assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> 제네릭 함수 및 작업 작성은 Q # 함수 및 작업에 대해 생각 하는 데 매우 유용 하 게 사용할 수 있는 방법 중 하나입니다.
> 모든 함수는 정확히 하나의 입력을 사용 하 고 정확히 하나의 출력을 반환 하므로 형식의 입력 `'T -> 'U` *모든* Q # 함수와 일치 합니다.
> 마찬가지로 모든 작업을 `'T => 'U`형식의 입력에 전달할 수 있습니다.

두 번째 예는 다른 두 함수의 컴퍼지션을 반환 하는 함수를 작성 하는 것입니다.

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

여기서는 `A`, `B`및 `C`를 정확 하 게 지정 해야 하므로 새로운 `Compose` 함수의 유틸리티를 심각 하 게 제한 합니다.
모든 `Compose` `A`, `B`및 `innerFn` 및 `outerFn`를 *통해* `C`에만 의존 합니다.
또는 `A`, `B`및 `C`에 대해 작동 함을 나타내는 *`Compose`에 형식* 매개 변수를 추가할 수 있습니다. 이러한 매개 변수는 `innerFn` 및 `outerFn`에서 예상한 것과 일치 합니다. :

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

Q # 표준 라이브러리는 이러한 형식의 매개 변수가 있는 작업 및 함수를 제공 하 여 더 높은 순서 제어 흐름을 보다 쉽게 표현할 수 있도록 합니다.
이러한 내용은 [Q # 표준 라이브러리 가이드](xref:microsoft.quantum.libraries.standard.intro)에 자세히 설명 되어 있습니다.

## <a name="borrowing-qubits"></a>Borrowing ##

Borrowing 메커니즘을 사용 하면 계산 중에 스크래치 공간으로 사용할 수 있는 원하는 비트를 할당할 수 있습니다. 이러한 기능은 일반적으로 깨끗 한 상태가 아닙니다. 즉, $ \ket{0}$와 같은 알려진 상태로 반드시 초기화 되는 것은 아닙니다. 그 중 하나는 상태를 알 수 없기 때문에 "더티"의 상태를 말하는 것 이며,이는 퀀텀 컴퓨터의 메모리에 있는 다른 부분과 함께 사용 될 수도 있습니다. 더티 비트의 알려진 사용 사례 중에는 incrementers의 구현이 매우 거의 필요 하지 않은 다중 제어 CNOT 게이트의 구현입니다.

`borrowing` 키워드를 사용 하는 예제는 다음과 같습니다. 예를 들어 함수는 아래 정의 `MultiControlledXBorrow` 합니다.
`controls` `X` 작업에 추가 해야 하는 컨트롤의 비트를 표시 하는 경우이 구현에 따라 `Length(controls)-2` 많은 더티 ancillas이 추가 됩니다.

```qsharp
operation MultiControlledXBorrow ( controls : Qubit[] , target : Qubit ) : Unit
is Adj + Ctl {

    body (...) {
        ... // skipping some case handling here
        let numberOfDirtyQubits = numberOfControls - 2;
        borrowing( dirtyQubits = Qubit[ numberOfDirtyQubits ] ) {

            let allQubits = [ target ] + dirtyQubits + controls;
            let lastDirtyQubit = numberOfDirtyQubits;
            let totalNumberOfQubits = Length(allQubits);

            let outerOperation1 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 1, 1, 0, numberOfDirtyQubits , _ );
            
            let innerOperation = 
                CCNOTByIndex(
                    totalNumberOfQubits - 1, totalNumberOfQubits - 2, lastDirtyQubit, _ );
            
            WithA(outerOperation1, innerOperation, allQubits);
            
            let outerOperation2 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 2, 2, 1, numberOfDirtyQubits - 1 , _ );
            
            WithA(outerOperation2, innerOperation, allQubits);
        }
    }

    controlled(extraControls, ...) {
        MultiControlledXBorrow( extraControls + controls, target );
    }
}
```

`With` 조합 기---는 adjoint를 지 원하는 작업 (예: `WithA`---에 적용 되는 형식으로 사용 됩니다. 즉, `With`만 포함 하는 구조에 대 한 제어를 추가 하는 것과 같은 좋은 프로그래밍 스타일입니다. 내부 작업에 제어를 전파 합니다. 작업의 `body` 외에도, 작업의 `controlled` 본문에 대 한 구현이 `controlled auto` 문으로의 구현이 아닌 명시적으로 제공 되었습니다. 그 이유는 회로 구조에서 각 및 `body`의 모든 개별 게이트에 컨트롤을 추가 하는 것과 비교 하 여 유용한 컨트롤을 쉽게 추가 하는 방법입니다. 

그러나이 코드는 곱하기 제어 `X` 작업을 구현 하는 것과 동일한 목표를 달성 하는 다른 함수 `MultiControlledXClean`와 비교 하는 것이 좋습니다. 그러나 `using` 메커니즘을 사용 하 여 여러 가지 깨끗 한 비트를 사용 합니다. 
