---
title: 'Q의 제어 흐름 #'
description: 루프, 조건 등
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
ms.openlocfilehash: 0cf62a128170bd0c28ff77f00fc23414567b1ea4
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415306"
---
# <a name="control-flow-in-q"></a>Q의 제어 흐름 #

작업 또는 함수 내에서 각 문은 다른 일반적인 명령적 언어와 비슷하게 순서 대로 실행 됩니다.
그러나 다음과 같은 세 가지 방법으로 제어 흐름을 수정할 수 있습니다.

* `if`할당문
* `for`하며
* `repeat-until-success`하며

`if`및 `for` 제어 흐름 구성은 대부분의 일반적인 프로그래밍 언어에 대해 친숙 하 게 진행 됩니다. [`Repeat-until-success`](#repeat-until-success-loop)루프는이 문서의 뒷부분에서 설명 합니다.

중요 한 `for` `if` 것은 [특수화](xref:microsoft.quantum.guide.operationsfunctions) 가 자동 생성 되는 작업에 루프 및 문을 사용할 수 있다는 것입니다. 이 시나리오에서 루프의 adjoint는 `for` 방향을 바꾸고 각 반복의 adjoint를 사용 합니다.
이 작업은 "신발 및 socks" 원칙을 따릅니다. 즉, socks에 배치를 취소 한 다음 신발로 전환 하려면 축구 전환에 대 한 실행을 취소 하 고 socks에 배치를 실행 취소 해야 합니다. 

## <a name="if-else-if-else"></a>If, Else-if, Else

`if`문은 조건부 실행을 지원 합니다.
키워드 `if` , 괄호 안의 부울 식, 문 블록 ( _then_ 블록)으로 구성 됩니다.
필요에 따라, 각각 키워드 `elif` , 괄호 안의 부울 식 및 문 블록 ( _else-if_ 블록)으로 구성 된 else 절을 사용할 수 있습니다.
마지막으로, `else` 다른 문 블록 ( _else_ 블록) 뒤에 오는 키워드로 구성 된 else 절을 사용 하 여 문을 선택적으로 완료할 수 있습니다.

`if`조건이 평가 되 고 *true*인 경우 *에는* 블록이 실행 됩니다.
조건이 *false*이면 첫 번째 else 조건이 평가 됩니다. 해당 하는 경우 *else* 블록을 실행 합니다.
그렇지 않은 경우 두 번째 else if 블록은를 계산 하 고, 세 번째는 true 조건이 있는 절이 발견 되거나 else if 절이 없을 때까지 계산 됩니다.
원래 *if* 조건과 모든 else if 절이 *false*이면 *else* 블록이 실행 됩니다 (제공 된 경우).

실행 되는 블록이 무엇이 든 해당 범위 내에서 실행 됩니다.
`if`, 또는 블록 내부에서 만들어진 바인딩은 `elif` `else` 블록이 끝난 후에는 표시 되지 않습니다.

예를 들면 다음과 같습니다.

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
or
```qsharp
if (i == 1) {
    X(target);
    let n = 1;
} elif (i == 2) {
    Y(target);
    let m = n + 1; // would cause an error, because n is no longer bound
} else {
    Z(target);
}
```

## <a name="for-loop"></a>For 루프

`for`문은 정수 범위 또는 배열에 대 한 반복을 지원 합니다.
문은 키워드로 구성 된 `for` 다음 기호 또는 기호 튜플, 키워드 `in` , 형식 `Range` 또는 배열의 식, 괄호 안에 있는 식 및 문 블록으로 구성 됩니다.

문 블록 (루프의 본문)은 범위 또는 배열의 각 값에 바인딩된 정의 된 기호 (루프 변수)를 사용 하 여 반복적으로 실행 됩니다.
범위 식이 빈 범위 또는 배열로 계산 되는 경우 본문은 전혀 실행 되지 않습니다.
루프를 시작 하기 전에 식이 완전히 계산 되며 루프가 실행 되는 동안에는 변경 되지 않습니다.

루프 변수는 루프 본문에 대 한 각 입구에 바인딩되고 본문의 끝에서 바인딩되지 않습니다.
For 루프가 완료 된 후 루프 변수가 바인딩되지 않습니다.
루프 변수의 바인딩은 변경할 수 없으며 다른 변수 바인딩과 동일한 규칙을 따릅니다. 

이 예제에서 `qubits` 는의 레지스터 (즉, 형식)입니다. `Qubit[]` 

```qsharp
// ...
for (qubit in qubits) {  // iterate over each qubit value in the array qubits
    H(qubit);
}
// 'qubit' is no longer bound

mutable results = new (Int, Results)[Length(qubits)];
for (index in 0 .. Length(qubits) - 1) {  // iterates over the integers in the Range 0 .. (Length(qubits) - 1)
    set results w/= index <- (index, M(qubits[index])); // measure each qubit, updates the tuple value in the results array that at index 
}

mutable accumulated = 0;
for ((index, measured) in results) { // iterates over the tuple values in results
    if (measured == One) {
        set accumulated += 1 <<< index;
    }
}
```

끝에는 산술 시프트 왼쪽 이항 연산자를 사용 했습니다 `<<<` . 자세한 내용은 [숫자 식](xref:microsoft.quantum.guide.expressions#numeric-expressions)을 참조 하세요.

## <a name="repeat-until-success-loop"></a>반복-성공 루프

Q # 언어를 사용 하면 기존 제어 흐름을 사용 하 여 다양 한 비트 측정 결과에 따라 달라 집니다.
이 기능을 사용 하면 unitaries를 구현 하기 위한 계산 비용을 줄일 수 있는 강력한 확률 가젯을 구현할 수 있습니다.
이에 대 한 예는 Q #의 *반복-성공* (RUS) 패턴입니다.
이러한 RUS 패턴은 기본 게이트 측면에서 저렴 한 비용으로 *예상* 되는 확률 프로그램입니다. 발생 한 비용은 실제 실행 및 가능한 여러 branchings의 인터리빙에 따라 다릅니다.

반복-성공 (RUS) 패턴을 용이 하 게 하기 위해 Q #에서 구문을 지원 합니다.

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

여기서 `expression` 는 형식의 값으로 계산 되는 유효한 식입니다 `Bool` .
루프 본문이 실행 된 후 조건이 평가 됩니다.
조건이 true 이면 문이 완료 된 것입니다. 그렇지 않으면 픽스업이 실행 되 고 문이 루프 본문부터 다시 실행 됩니다.

RUS 루프의 세 부분 (본문, 테스트 및 수정)은 *각 반복에 대해*단일 범위로 처리 되므로 본문에 바인딩된 기호는 테스트와 픽스업에서 모두 사용할 수 있습니다.
그러나 픽스업 실행을 완료 하면 문 범위가 끝나기 때문에 본문 또는 픽스업 중에 만든 기호 바인딩을 후속 반복에서 사용할 수 없습니다.

또한 `fixup` 문은 종종 유용 하지만 항상 필요한 것은 아닙니다.
필요 하지 않은 경우 구문은

```qsharp
repeat {
    // do stuff
}
until (expression);
```

유효한 RUS 패턴 이기도 합니다.

더 많은 예제 및 세부 정보는이 문서의 [반복-성공 예](#repeat-until-success-examples) 를 참조 하세요.

> [!TIP]   
> 함수 내에서-success 루프를 사용 하지 마십시오. *While* 루프를 사용 하 여 함수 내에 해당 기능을 제공 합니다. 

## <a name="while-loop"></a>While 루프

반복-성공 패턴에는 퀀텀 별 connotation가 있을 수 있습니다. 이러한 클래스는 특정 퀀텀 알고리즘 클래스에서 널리 사용 되므로 Q #의 전용 언어 구문입니다. 그러나 조건에 따라 중단 되 고 해당 실행 길이는 컴파일 시간에 알 수 없는 루프는 퀀텀 런타임에서 특히 주의 해 서 처리 됩니다. 그러나 이러한 루프는 기존 (비 퀀텀) 하드웨어에서 실행 되는 코드만 포함 하므로 함수 내에서 사용 하는 것은 문제가 되지 않습니다. 

따라서 Q #은 함수 내 에서만 루프를 사용할 수 있도록 지원 합니다. `while`문은 키워드 `while` , 괄호 안의 부울 식 및 문 블록으로 구성 됩니다.
문 블록 (루프의 본문)은 조건이로 확인 되 면 실행 됩니다 `true` .

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

## <a name="return-statement"></a>Return 문

Return 문은 작업 또는 함수의 실행을 종료 하 고 호출자에 게 값을 반환 합니다.
키워드와 `return` 해당 형식의 식, 종료 세미콜론으로 구성 됩니다.

예를 들면 다음과 같습니다.
```qsharp
return 1;
```
or
```qsharp
return (results, qubits);
```

* 빈 튜플을 반환 하는 호출 가능에는 `()` return 문이 필요 하지 않습니다.
* 작업 또는 함수에서 조기 종료를 지정 하려면를 사용 `return ();` 합니다.
다른 형식을 반환 하는 callables에는 최종 return 문이 필요 합니다.
* 작업 내에는 최대 개수의 return 문이 없습니다.
문이 블록 내의 return 문 뒤에 오는 경우 컴파일러는 경고를 생성할 수 있습니다.

   
## <a name="fail-statement"></a>Fail 문

Fail 문은 작업 실행을 종료 하 고 호출자에 게 오류 값을 반환 합니다.
키워드 `fail` 와 문자열 및 종료 세미콜론으로 구성 됩니다.
문은 오류 메시지로 기존 드라이버에 문자열을 반환 합니다.

작업 내의 실패 문 수에 대 한 제한은 없습니다.
문이 블록 내의 fail 문 뒤에 오는 경우 컴파일러는 경고를 생성할 수 있습니다.

예를 들면 다음과 같습니다.

```qsharp
fail $"Impossible state reached";
```
또는 [보간된 문자열](xref:microsoft.quantum.guide.expressions#interpolated-strings)을 사용 하 여
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a>반복-성공-성공 예

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a>무리 축에 대 한 단일 비트 회전에 대 한 RUS 패턴 

일반적인 사용 사례에서 다음 Q # 연산은 Bloch 구의 $ (I + 2i Z)/\sqrt $의 무리 축을 중심으로 회전을 구현 {5} 합니다. 구현에서는 알려진 RUS 패턴을 사용 합니다.

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

### <a name="rus-loop-with-a-mutable-variable-in-scope"></a>범위에 변경 가능한 변수가 있는 RUS 루프

이 예에서는 `finished` 전체 반복-픽스업 루프의 범위 내에 있고 루프 앞에서 초기화 되 고 픽스업 단계에서 업데이트 되는 변경 가능한 변수를 사용 하는 방법을 보여 줍니다.

```qsharp
mutable iter = 1;
repeat {
    ProbabilisticCircuit(qubits);
    let success = ComputeSuccessIndicator(qubits);
}
until (success || iter > maxIter)
fixup {
    iter += 1;
    ComputeCorrection(qubits);
}
```

### <a name="rus-without-fixup"></a>RUS (없음)`fixup`

이 예제에서는 픽스업 단계가 없는 RUS 루프를 보여 줍니다. 이 코드는 {5} 및 게이트를 사용 하 여 $V _3 = (\boldone + 2 i Z)/\sqrt $ 중요 한 회전 게이트를 구현 하는 확률 회로입니다 `H` `T` .
루프는 평균에서 $ \frac {8} {5} $ 반복을 종료 합니다.
자세한 내용은 [*반복-성공--성공: 단일 기능 비트 unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick 및 svore, 2014)의 비결 정적 분해를 참조 하세요.

```qsharp
using (qubit = Qubit()) {
    repeat {
        H(qubit);
        T(qubit);
        CNOT(target, qubit);
        H(qubit);
        Adjoint T(qubit);
        H(qubit);
        T(qubit);
        H(qubit);
        CNOT(target, qubit);
        T(qubit);
        Z(target);
        H(qubit);
        let result = M(qubit);
    } until (result == Zero);
}
```

### <a name="rus-to-prepare-a-quantum-state"></a>퀀텀 상태를 준비 하기 위한 RUS

마지막으로, 다음은 {1} $ \ket{+} $ 상태에서 시작 하 여 퀀텀 상태 $ \frac {\sqrt {3} } \left (\sqrt {2} \ket {0} + \ket {1} \right) $를 준비 하는 RUS 패턴의 예입니다.

이 작업에 표시 되는 주목할 만한 프로그래밍 기능은 다음과 같습니다.

* `fixup`퀀텀 작업과 관련 된 루프의 더 복잡 한 부분입니다. 
* `AssertProb`문을 사용 하 여 프로그램의 지정 된 특정 지점에서 퀀텀 상태를 측정 하는 확률을 확인 합니다.

및 작업에 대 한 자세한 내용은 [`Assert`](xref:microsoft.quantum.intrinsic.assert) [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) [테스트 및 디버깅](xref:microsoft.quantum.guide.testingdebugging)을 참조 하세요.

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+> state.
            AssertProb(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+> state", 1e-10 );
            AssertProb(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+> state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+> state on the auxiliary qubit
            // is 3/4.
            AssertProb(
                [PauliX], [auxiliary], Zero, 3. / 4.,
                "Error: the probability to measure |+> in the first
                auxiliary must be 3/4",
                1e-10);

            // If we get the measurement outcome Zero, we prepare the
            // required state.
            let outcome = Measure([PauliX], [auxiliary]);
        }
        until (outcome == Zero)
        fixup {
            // Bring the auxiliary and target qubits back to |+> state.
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

자세한 내용은 [표준 라이브러리와 함께 제공 되는 단위 테스트 샘플](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs)을 참조 하세요.

## <a name="next-steps"></a>다음 단계

Q #에서 [테스트 및 디버깅](xref:microsoft.quantum.guide.testingdebugging) 에 대해 알아봅니다.
