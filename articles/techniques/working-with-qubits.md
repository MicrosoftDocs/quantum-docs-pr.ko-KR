---
title: 이상 비트 작업
description: '엔터프라이즈급 비트 작업-Q # 기술'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.qubits
ms.openlocfilehash: dc6db93dadc37534aece9624fe516125d919f8cd
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76819997"
---
# <a name="working-with-qubits"></a>이상 비트 작업

이제는 Q # 언어의 다양 한 부분을 살펴보았습니다 .이를 통해 더 많은 부분을 소개 하 고,이를 사용 하는 방법을 확인할 수 있습니다.

## <a name="allocating-qubits"></a>비트 할당

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

## <a name="intrinsic-operations"></a>내장 작업

할당 된 후에는 함수 및 작업에 이상 비트를 전달할 수 있습니다.
어떤 경우에는이 작업을 수행할 수 있는 작업은 모두 작업으로 정의 되므로 Q # 프로그램은이 작업을 수행할 수 있습니다.
이러한 작업은 [내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude)에서 더 자세히 볼 수 있지만 지금은이 작업에 대 한 몇 가지 유용한 작업을 소개 합니다.

첫째, 단일 기능 비트 Pauli 연산자 $X $, $Y $ 및 $Z $는 Q #에서 각각 `Y`형식의 내장 작업 `X`, `Z`및 `(Qubit => Unit is Adj + Ctl)`로 표시 됩니다.
[내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude)에 설명 된 대로 $X $ 등의 `X`를 비트 대칭 작업으로 생각할 수 있습니다.
`X` 작업을 사용 하면 일부 클래식 비트 문자열 $s $에 대해 $ \ket{s_0 s_1 \dots . s_n} $ 형식의 상태를 준비할 수 있습니다.

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

## <a name="measurements"></a>측정값

기본 제공 되는 기본 제공 비 작업 인 `Measure` 작업을 사용 하 여 `Qubit` 형식의 개체에서 기존 정보를 추출 하 고, 예약 된 형식 `Result`를 포함 하는 기존 값을 결과에 할당할 수 있습니다 .이는 결과가 더 이상 퀀텀 상태가 아님을 나타냅니다.
`Measure`에 대 한 입력은 `Pauli` 형식의 값 (예 `PauliX`) 및 `Qubit`형식의 값으로 표현 되는 Bloch 구의 Pauli 축입니다.

간단한 예는 $ \ket{0}$ 상태에서 하나 비트를 할당 한 다음 Hadamard 연산을 `H` 적용 하 고 결과를 `PauliZ` 기준으로 측정 하는 다음 작업입니다.

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

약간 더 복잡 한 예는 다음 연산에서 제공 됩니다 .이 경우에는 `Qubit[]` 형식의 레지스터에 있는 모든 값이 지정 된 Pain으로 측정 될 때 `true` 상태이 고, 그렇지 않은 경우 `false`를 반환 하는 경우 부울 값을 반환 합니다.

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

Q # 언어를 사용 하면 기존 제어 흐름을 사용 하 여 다양 한 비트 측정 결과에 따라 달라 집니다.
이 기능을 사용 하면 unitaries을 구현 하기 위한 계산 비용을 줄일 수 있는 강력한 확률 가젯을 구현할 수 있습니다.
예를 들어 Q #에서 쉽게 구현할 수 있습니다 (RUS ( *-성공-성공* ) 패턴 이라고 함).
이러한 RUS 패턴은 기본 게이트 측면에서 비용이 *저렴 한* 확률 프로그램 이지만 실제 실행 및 가능한 여러 가지 branchings의 실제 인터리브에 따라 실질적인 비용이 달라 집니다.

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

여기서 `statementBlock1` 및 `statementBlock2`은 0 개 이상의 Q # 문이 고 `Bool`형식의 값으로 계산 되는 유효한 식을 `expression` 합니다.
일반적인 사용 사례에서 다음 Q # 연산은 Bloch 구의 $ (I + 2i Z)/\sqrt{5}$ 인 무리 축을 중심으로 회전을 구현 합니다. 이 작업은 알려진 RUS 패턴을 사용 하 여 수행 됩니다.

```qsharp
operation ApplyVRotationUsingRUS(qubit : Qubit) : Unit {
    using (controls = Qubit[2]) {
        ApplyToEachA(H, controls);
        mutable finished = false;
        repeat {
            Controlled X(controls, qubit);
            S(qubit);
            Controlled X(controls, qubit);
            Z(qubit);
        }
        until (finished)
        fixup {
            if (MeasureIfAllQubitsAreZero(controls, PauliX)) {
                set finished = true;
            }
        }
    }
}
```

이 예에서는 전체 반복 전-픽스업 루프의 범위에 있고 루프에서 초기화 되 고 픽스업 단계에서 업데이트 되는 변경 가능한 변수 `finished`를 사용 하는 방법을 보여 줍니다.

마지막으로, $ \ket{+} $ 상태에서 시작 하 여 퀀텀 상태 $ \frac{1}{\sqrt{3}} \left (\sqrt{2}\ket{0}+ \ket{1}\right) $를 준비 하는 RUS 패턴의 예를 보여 줍니다.
[표준 라이브러리와 함께 제공 되는 단위 테스트 샘플](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs)도 참조 하세요.

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+⟩ state.
            AssertProb(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+⟩ state", 1e-10 );
            AssertProb(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+⟩ state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+⟩ state on the auxiliary qubit
            // is 3/4.
            AssertProb(
                [PauliX], [auxiliary], Zero, 3. / 4.,
                "Error: the probability to measure |+⟩ in the first
                auxiliary must be 3/4",
                1e-10);

            // If we get the measurement outcome Zero, we prepare the
            // required state.
            let outcome = Measure([PauliX], [auxiliary]);
        }
        until (outcome == Zero)
        fixup {
            // Bring the auxiliary and target qubits back to |+⟩ state.
            if (outcome == One) {
                Z(auxiliary);
                X(target);
                H(target);
            }
        }
        // Return the auxiliary qubit back to the Zero state.
        H(auxiliary);
    }
}
```

이 작업에 표시 되는 주목할 만한 프로그래밍 기능은 퀀텀 작업을 포함 하는 루프의 좀 더 복잡 한 `fixup` 부분으로, `AssertProb` 문을 사용 하 여 프로그램의 지정 된 특정 지점에서 퀀텀 상태를 측정 하는 확률을 확인 합니다.
또한 [`Assert`](xref:microsoft.quantum.intrinsic.assert) 및 [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) 작업에 대 한 자세한 내용은 [테스트 및 디버깅](xref:microsoft.quantum.techniques.testing-and-debugging) 을 참조 하세요.
