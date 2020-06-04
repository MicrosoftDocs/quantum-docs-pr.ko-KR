---
title: 큐비트 사용
description: 채우기 설명
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
ms.openlocfilehash: 0deb0729a88c49798f32a22a943b935d383c570b
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327546"
---
# <a name="working-with-qubits"></a>큐비트 사용

이제는 Q # 언어의 다양 한 부분을 살펴보았습니다 .이를 통해 더 많은 부분을 소개 하 고,이를 사용 하는 방법을 확인할 수 있습니다.

이러한 문은 함수 본문 내에서 허용 되지 않습니다.
작업 내 에서만 유효 합니다.

## <a name="allocating-qubits"></a>비트 할당

### <a name="clean-qubits"></a>정리 비트

`using`문은 문 블록 중에 사용할 새 요소를 *할당* 하는 데 사용 됩니다.

문은 키워드로 구성 되 고, 여는 `using` 괄호 `(` , 바인딩, 닫는 괄호 `)` 및 계산 된 문 블록으로 구성 됩니다.
바인딩은 문과 동일한 패턴을 따릅니다 `let` . 단일 기호 또는 기호 튜플, 등호 `=` , 단일 값 또는 *이니셜라이저의*일치 하는 튜플 중 하나를 수행 합니다.

이니셜라이저는로 표시 된 단일의 비트 또는의 배열 ( `Qubit()` `Qubit[n]` 여기서 `n` 는 `Int` 식)으로 사용할 수 있습니다.
예제:

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

위의 예에서 $ \ket $ state;에 할당 된 것 처럼이 방법으로 할당 된 모든 {0} `register` 것은 $ \ket {00000} = \ket {0} \otimes \ket {0} \otimes \cst\otimes \ket $ 상태에 {0} 있습니다.
블록의 끝에서 `using` 해당 블록에 의해 할당 된 모든 요소는 즉시 할당 취소 되며 더 이상 사용할 수 없습니다.

> [!WARNING]
> 대상 컴퓨터는 {0} 할당을 위해 다른 블록으로 다시 사용 하 고 제공할 수 있도록 해당 사용자가 할당 취소 직전에 $ \ket $ 상태에 있는 것으로 간주 `using` 합니다.
> 가능 하면 항상 단일 작업을 사용 하 여 할당 된 모든 비트를 $ \ket $로 반환 {0} 합니다.
> 필요한 경우 작업을 사용 하 여 @"microsoft.quantum.intrinsic.reset" 대신 원하는 비트를 측정 하 고 해당 측정 결과를 사용 하 여 측정 된 값이 $ \ket $로 반환 되도록 할 수 있습니다 {0} . 이러한 측정값을 사용 하면 잔여 비트를 사용 하 여 되거나 얽 히를 소멸 시킬 수 있으므로 계산에 영향을 줄 수 있습니다.


### <a name="borrowed-qubits"></a>빌려의 비트

`borrowing`문을 사용 하 여 특정 상태에 있지 않아도 되는 임시 사용에 대 한 작업을 수행할 수 있습니다.

Borrowing 메커니즘을 사용 하면 계산 중에 스크래치 공간으로 사용할 수 있는 원하는 비트를 할당할 수 있습니다.
이러한 기능은 일반적으로 깨끗 한 상태가 아닙니다. 즉, $ \ket $와 같은 알려진 상태로 반드시 초기화 되는 것은 아닙니다. {0}
이러한 경우는 상태를 알 수 없으며 퀀텀 컴퓨터 메모리의 다른 부분과 함께 사용할 수 있기 때문에이를 "더티" 이상으로 지칭 하기도 합니다.

바인딩은 문에 있는 것과 동일한 패턴 및 규칙을 따릅니다 `using` .
예제:
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
인 중 한 비트는 알 수 없는 상태 이며 문 블록의 끝에 있는 범위를 벗어났습니다.
대출자는가 중에 있던 상태와 동일한 상태를 유지 하도록 커밋 합니다. 즉, 문 블록의 시작과 끝에 있는 상태는 동일 해야 합니다.
특히 borrowing 범위에는 측정값이 포함 되지 않아야 하는 일반적인 상태가 아닐 수도 있습니다. 

Borrowing를 사용 하는 경우 시스템은 먼저 사용 중이 고 문의 본문 중에는 액세스 하지 않는 대신에 요청을 채우려고 시도 `borrowing` 합니다.
이러한 것이 충분 하지 않은 경우 요청을 완료 하기 위해 새 비트를 할당 합니다.


더티 비트의 알려진 사용 사례 중에는 incrementers의 구현이 매우 거의 필요 하지 않은 다중 제어 CNOT 게이트의 구현입니다.
Q #에서의 사용 [예를 확인](#borrowing-qubits-example) 하거나, [*2n + 2를 사용 하 여 Toffoli 기반 모듈식 곱하기*](https://arxiv.org/abs/1611.07995) (Haner, RoetBorrowing er 및 svs2017)를 사용 하는 백서를 참조 하십시오.


## <a name="intrinsic-operations"></a>내장 작업

할당 된 후에는 함수 및 작업에 이상 비트를 전달할 수 있습니다.
어떤 경우에는이 작업을 수행할 수 있는 작업은 모두 작업으로 정의 되므로 Q # 프로그램은이 작업을 수행할 수 있습니다.
이러한 작업은 [내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude)에서 더 자세히 볼 수 있지만 지금은이 작업에 대 한 몇 가지 유용한 작업을 소개 합니다.

첫째, 단일 기능 비트 Pauli 연산자 $X $, $Y $ 및 $Z $는 Q #에서 `X` `Y` `Z` 각각 형식이 있는 내장 작업, 및로 표시 됩니다 `(Qubit => Unit is Adj + Ctl)` .
[내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude)에 설명 된 것 처럼, $X $ 등의 작업을 수행 하는 것으로 간주할 수 있습니다 `X` .
`X`작업을 사용 하면 몇 가지 기존 비트 문자열 $s $에 대해 $ \ket{s_0 s_1 \dots .. s_n} $ 형식의 상태를 준비할 수 있습니다.

```qsharp
operation PrepareBitString(bitstring : Bool[], register : Qubit[]) : Unit
is Adj + Ctl {
    let nQubits = Length(register);
    for (idxQubit in 0..nQubits - 1) {
        if (bitstring[idxQubit]) {
            X(register[idxQubit]);
        }
    }
}

operation RunExample() : Unit {
    using (register = Qubit[8]) {
        PrepareBitString(
            [true, true, false, false, true, false, false, true],
            register
        );
        // At this point, register now has the state |11001001〉.
        // Resetting the qubits will allow us to deallocate them properly.
        ResetAll(register);
    }
}
```

> [!TIP]
> 나중에이 작업을 작성 하는 보다 간단한 방법으로 수동 흐름 제어를 요구 하지 않습니다.

\Ket transform $H $를 사용 하 여 $ \ket{+} = \left (\ket {0} + \ket {1} \left)/\left $ {2} 및 $ \ket {-} = \left (\ket-Hadamard \left)/\left $와 같은 상태를 준비할 수도 있습니다 {0} {1} {2} .이는 내장 작업으로 Q #에서 표시 됩니다 `H : (Qubit => Unit is Adj + Ctl)` .

```qsharp
operation PreparePlusMinusState(bitstring : Bool[], register : Qubit[]) : Unit {
    // First, get a computational basis state of the form
    // |s_0 s_1 ... s_n〉 by using PrepareBitString, above.
    PrepareBitString(bitstring, register);
    // Next, we use that |+〉 = H|0〉 and |-〉 = H|1〉 to
    // prepare the state we want.
    for (idxQubit in IndexRange(register)) {
        H(register[idxQubit]);
    }
}
```

## <a name="measurements"></a>측정

`Measure`기본 제공 되는 기본이 아닌 작업 인 작업을 사용 하 여 형식의 개체에서 기존 정보를 추출 하 고, 결과는 `Qubit` `Result` 더 이상 퀀텀 상태가 아님을 나타내는 예약 된 형식을 포함 하는 기존 값을 할당할 수 있습니다.
에 대 한 입력은 `Measure` 형식 `Pauli` (예의 경우 `PauliX` ) 및 형식의 값으로 표현 되는 Bloch 구의 pauli 축입니다 `Qubit` .

간단한 예는 $ \ket $ 상태에서 1 개의 한 비트를 할당 하 {0} 고, Hadamard 작업을 적용 하 고, 결과를 측정 하는 다음 작업입니다 `H` `PauliZ` .

```qsharp
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now we measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // we reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, we return the result of the measurement.
        return result;
    }
}
```

조금 더 복잡 한 예는 다음 연산에서 제공 됩니다 .이 경우에는 `true` 레지스터의 모든 모든 비트가 `Qubit[]` 지정 된 pai로 측정 될 때 0 상태에 있는 경우 부울 값을 반환 하 고, 그렇지 않으면를 반환 `false` 합니다.

```qsharp
operation MeasureIfAllQubitsAreZero(qubits : Qubit[], pauli : Pauli) : Bool {
    mutable value = true;
    for (qubit in qubits) {
        if (Measure([pauli], [qubit]) == One) {
            set value = false;
        }
    }
    return value;
}
```

## <a name="borrowing-qubits-example"></a>Borrowing  Bits 예제

에는 아래 정의 된 함수와 같이 키워드를 사용 하는 예제가 있습니다 `borrowing` `MultiControlledXBorrow` .
가 `controls` 작업에 추가 해야 하는 컨트롤의 비트를 나타내는 경우 `X` `Length(controls)-2` 이 구현에서 많은 더티 ancillas의 전체를 추가 합니다.

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

`With`조합 기---는 adjoint를 지 원하는 작업 (예:---)에 적용할 수 있는 형식으로 되어 있습니다. `WithA`
이는를 포함 하는 구조에 컨트롤을 추가 하 `With` 는 작업을 내부 작업에만 전파 하므로 좋은 프로그래밍 스타일입니다.
또한 여기에서는 작업의에 대 한 추가 작업을 수행 하는 `body` `controlled` 대신 작업 본문의 구현이 명시적으로 제공 되었습니다 `controlled auto` .
이에 대 한 이유는의 각 및 모든 개별 게이트에 컨트롤을 추가 하는 것과 비교 하 여 유용한 추가 컨트롤을 쉽게 추가 하는 방법에 대 한 것입니다 `body` . 

그러나이 코드는 곱하기 제어 작업을 구현 하는 것과 동일한 목표를 달성 하는 다른 라고 함수와 비교 하는 것이 좋습니다 .이는 `MultiControlledXClean` `X` 메커니즘을 사용 하 여 여러 가지 깨끗 한 비트를 사용 합니다 `using` . 

## <a name="next-steps"></a>다음 단계

Q #의 [제어 흐름](xref:microsoft.quantum.guide.controlflow) 에 대해 알아봅니다.