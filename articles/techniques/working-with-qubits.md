---
title: 이상 비트 사용 | Microsoft Docs
description: 이상 비트 작업
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.qubits
ms.openlocfilehash: 477b358c3eba58b62926b4e9094770c9741cac92
ms.sourcegitcommit: 27c9bf1aae923527aa5adeaee073cb27d35c0ca1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/05/2019
ms.locfileid: "74864256"
---
# <a name="working-with-qubits"></a>이상 비트 작업 #

이제는 Q # 언어의 다양 한 부분을 살펴보았습니다 .이를 통해 더 많은 부분을 소개 하 고,이를 사용 하는 방법을 확인할 수 있습니다.

## <a name="allocating-qubits"></a>비트 할당 ##

첫째, Q #에서 사용할 수 있는 이상 비트를 얻기 위해 `using` 블록 내에서 다음과 같은 작업을 *할당* 합니다.

```qsharp
using (register = Qubit[5]) {
    // Do stuff...
}
```

이 방법으로 할당 된 모든 모든 비트는 $ \ket{0}$ state;에서 시작 됩니다. 위의 예에서는 `register`가 $ \ket{00000} = \ket{0} \otimes \ket{0} \otimes \cst\otimes \ket{0}$ 상태에 있습니다.
`using` 블록의 끝에서 해당 블록에 의해 할당 된 모든 요소는 즉시 할당 취소 되며 더 이상 사용할 수 없습니다.

> [!WARNING]
> 대상 컴퓨터는 할당을 위해 다른 `using` 블록으로 다시 사용 하 고 제공할 수 있도록 \ket가 할당 취소 바로 앞에 ${0}$ 상태에 있을 것으로 간주 합니다.
> 가능 하면 항상 단일 작업을 사용 하 여 할당 된 모든 비트를 $ \ket{0}$로 반환 합니다.
> 이 필요한 경우에는 @"microsoft.quantum.intrinsic.reset" 작업을 사용 하 여 대신 원하는 비트를 측정 하 고 해당 측정 결과를 사용 하 여 측정 된 값이 $ \ket{0}$로 반환 되도록 할 수 있습니다. 이러한 측정값을 사용 하면 잔여 비트를 사용 하 여 되거나 얽 히를 소멸 시킬 수 있으므로 계산에 영향을 줄 수 있습니다. 

## <a name="intrinsic-operations"></a>내장 작업 ##

할당 된 후에는 함수 및 작업에 이상 비트를 전달할 수 있습니다.
어떤 경우에는이 작업을 수행할 수 있는 작업은 모두 작업으로 정의 되므로 Q # 프로그램은이 작업을 수행할 수 있습니다.
이러한 작업은 [내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude)에서 더 자세히 볼 수 있지만 지금은이 작업에 대 한 몇 가지 유용한 작업을 소개 합니다.

첫째, 단일 기능 비트 Pauli 연산자 $X $, $Y $ 및 $Z $는 Q #에서 각각 `Y`형식의 내장 작업 `X`, `Z`및 `(Qubit => Unit is Adj + Ctl)`로 표시 됩니다.
[내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude)에 설명 된 대로 $X $ 등의 `X`를 비트 대칭 작업으로 생각할 수 있습니다.
이를 통해 일부 기존 비트 문자열 $s $에 대해 $ \ket{s_0 s_1 \dots . s_n} $ 형식의 상태를 준비할 수 있습니다.

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

operation Example() : Unit {

    using (register = Qubit[8]) {
        PrepareBitString(
            [true, true, false, false, true, false, false, true],
            register
        );
        // At this point, register now has the state |11001001〉.
    }
}
```

> [!TIP]
> 나중에이 작업을 작성 하는 보다 간단한 방법으로 수동 흐름 제어를 요구 하지 않습니다.

\Ket transform{0} $를 사용 하 여 $ \ket{+} = \left (\ket{0} + \ket{1}\left)/\left{2}$ 및 $ \ket{-} = \left (\ket{1}-Hadamard{2}\left)/\left $H $와 같은 상태를 준비할 수도 있습니다.

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

## <a name="measurements"></a>측정값 ##

기본 제공 되는 내장 형식이 아닌 작업 인 `Measure` 작업을 사용 하 여 `Qubit` 형식의 개체에서 클래식 정보를 추출 하 고 `Result`예약 된 형식이 포함 된 기존 값을 할당 하 여 결과가 더 이상 퀀텀 상태가 아님을 나타냅니다. `Measure`에 대 한 입력은 `Pauli` 형식의 개체 (예: `PauliX`) 및 `Qubit`형식의 개체에 의해 표현 되는 Bloch 구의 Pauli 축입니다. 

간단한 예는 $ \ket{0}$ 상태에서 하나 비트를 만든 다음 Hadamard gate ``H``를 적용 한 다음 `PauliZ` 기준으로 결과를 측정 하는 다음 작업입니다. 

```qsharp
operation MeasurementOneQubit () : Result {

    // The following using block creates a fresh qubit and initializes it 
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby creating the 
        // state 1/sqrt(2)(|0〉+|1〉). 
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

약간 더 복잡 한 예는 다음 연산에 의해 지정 됩니다 .이는 지정 된 형식으로 측정 될 때 `Qubit[]` 형식 레지스터의 모든 값이 0 인 경우 `true` 부울 값을 반환 하 고 그렇지 않으면 `false` 하는 부울 값을 반환 합니다. 

```qsharp
operation AllMeasurementsZero (qs : Qubit[], pauli : Pauli) : Bool {

    mutable value = true;
    for (q in qs) {
        if ( Measure([pauli], [q]) == One ) {
            set value = false;
        }
    }
    return value;
}
```

Q # 언어를 사용 하면 기존 제어 흐름에 대 한 종속성을 사용 하 여 값을 측정할 수 있습니다. 이를 통해에서는 unitaries 구현을 위한 계산 비용을 줄일 수 있는 강력한 확률 가젯을 구현할 수 있습니다. 예를 들어, Q #의 *반복* 을 구현 하는 것은 간단 합니다. Q #의 경우에는 기본 게이트를 기준으로 낮은 비용을 *예상* 하는 확률 회로 이지만 실제 실행 및 가능한 여러 가지 branchings의 실제 인터리브에 따라 실질적인 비용이 달라 집니다. 

반복-성공 (RUS) 패턴을 용이 하 게 하기 위해 Q #에서 구문을 지원 합니다.
```qsharp
repeat {
    statementBlock1 
}
until (expression)
fixup {
    statementBlock2
}
```
여기서 `statementBlock1` 및 `statementBlock2`은 0 개 이상의 Q # 문이 고 `Bool`형식의 값으로 계산 되는 유효한 식을 `expression` 합니다. 일반적인 사용 사례에서 다음 회로는 Bloch 구의 $ (I + 2i Z)/\sqrt{5}$의 무리 축을 중심으로 회전을 구현 합니다. 이 작업은 알려진 RUS 패턴을 사용 하 여 수행 됩니다. 

```qsharp
operation RUScircuit (qubit : Qubit) : Unit {

    using(ancillas = Qubit[2]) {
        ApplyToEachA(H, ancillas);
        mutable finished = false;
        repeat {
            Controlled X(ancillas, qubit);
            S(qubit);
            Controlled X(ancillas, qubit);
            Z(qubit);
        }
        until(finished)
        fixup {
            if AllMeasurementsZero(ancillas, Xpauli) {
                set finished = true;
            }
        }
    }
}
```

이 예에서는 전체 반복 전-픽스업 루프의 범위에 있고 루프에서 초기화 되 고 픽스업 단계에서 업데이트 되는 변경 가능한 변수 `finished`를 사용 하는 방법을 보여 줍니다.

마지막으로, $ \ket{+} $ 상태에서 시작 하 여 퀀텀 상태 $ \frac{1}{\sqrt{3}} \left (\sqrt{2}\ket{0}+ \ket{1}\right) $를 준비 하는 RUS 패턴의 예를 보여 줍니다. [표준 라이브러리와 함께 제공 되는 단위 테스트 샘플](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs)도 참조 하세요. 

```qsharp
operation RepeatUntilSuccessStatePreparation( target : Qubit ) : Unit {

    using( ancilla = Qubit() ) {
        H(ancilla);
        repeat {
            // We expect target and ancilla qubit to be in |+⟩ state.
            AssertProb( 
                [PauliX], [target], Zero, 1.0, 
                "target qubit should be in the |+⟩ state", 1e-10 );
            AssertProb( 
                [PauliX], [ancilla], Zero, 1.0,
                "ancilla qubit should be in the |+⟩ state", 1e-10 );
                
            Adjoint T(ancilla);
            CNOT(target, ancilla);
            T(ancilla);

            // The probability of measuring |+⟩ state on ancilla is 3/4.
            AssertProb( 
                [PauliX], [ancilla], Zero, 3. / 4., 
                "Error: the probability to measure |+⟩ in the first 
                ancilla must be 3/4",
                1e-10);

            // If we get measurement outcome Zero, we prepare the required state 
            let outcome = Measure([PauliX], [ancilla]);
        }
        until( outcome == Zero )
        fixup {
            // Bring ancilla and target back to |+⟩ state
            if( outcome == One ) {
                Z(ancilla);
                X(target);
                H(target);
            }
        }
        // Return ancilla back to Zero state
        H(ancilla);
    }
}
```
 
이 작업에 표시 되는 주목할 만한 프로그래밍 기능은 퀀텀 작업과 관련 된 루프의 더 복잡 한 `fixup` 부분으로, `AssertProb` 문을 사용 하 여 프로그램의 특정 지점에서 퀀텀 상태를 측정 하는 확률을 확인 합니다. `Assert` 및 `AssertProb` 문에 대 한 자세한 내용은 [테스트 및 디버깅](xref:microsoft.quantum.techniques.testing-and-debugging) 을 참조 하세요. 
