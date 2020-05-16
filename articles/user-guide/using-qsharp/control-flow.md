---
title: 'Q의 제어 흐름 #'
description: 루프, 조건 등
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
ms.openlocfilehash: c534e016fcb8b50e66c11ca29c253ba0512acc6e
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430954"
---
# <a name="control-flow-in-q"></a>Q의 제어 흐름 #

작업 또는 함수 내에서 각 문은 순서 대로 실행 되며 가장 일반적인 명령적 언어와 비슷합니다.
그러나이 제어 흐름은 다음과 같은 세 가지 방법으로 수정할 수 있습니다.

- `if`할당문
- `for`하며
- `repeat`-`until`하며

후자는 [아래](#repeat-until-success-loop)에서 자세히 설명 합니다.
`if`그러나 및 `for` 제어 흐름 구문은 대부분의 일반적인 프로그래밍 언어에 대해 친숙 하 게 진행 됩니다.

중요 한 `for` `if` 것은 특수화가 자동 생성 되는 작업에 루프 및 문을 사용할 수 있다는 것입니다. 이 경우 루프의 adjoint는 `for` 방향을 바꾸고 각 반복의 adjoint를 사용 합니다.
이는 "신발 및 socks" 원칙을 따릅니다. 즉, socks에 배치를 취소 한 다음 신발로 전환 하려면 축구 전환에 대 한 실행을 취소 하 고 socks에 배치를 실행 취소 해야 합니다.
계속 해 서 신발를 decidedly 하는 동안 시도 하 고 socks를 사용 하지 않는 것이 좋습니다.

## <a name="if-else-if-else"></a>If, Else-if, Else

`if`문은 조건부 실행을 지원 합니다.
키워드 `if` , 여는 괄호 `(` , 부울 식, 닫는 괄호 `)` 및 문 블록 ( _then_ 블록)으로 구성 됩니다.
그 다음에는 각각 키워드 `elif` , 여는 괄호 `(` , 부울 식, 닫는 괄호 `)` 및 문 블록 ( _else if_ 블록)으로 구성 된 여러 개의 else if 절이 올 수 있습니다.
마지막으로, `else` 다른 문 블록 ( _else_ 블록) 뒤에 오는 키워드로 구성 된 else 절을 사용 하 여 문을 선택적으로 완료할 수 있습니다.

`if`조건이 평가 되 고 true 이면 then 블록이 실행 됩니다.
조건이 false 이면 첫 번째 else 조건이 평가 됩니다. true 이면 else 블록을 실행 합니다.
그렇지 않으면 두 번째 else if 블록이 테스트 되 고, 세 번째는 조건이 true 인 절이 발생 하거나 else if 절이 더 이상 없을 때까지 테스트 됩니다.
원래 if 조건과 모든 else if 절이 false 이면 else 블록이 제공 된 경우 실행 됩니다.

실행 되는 블록은 자체 범위에서 실행 됩니다.
`if`, 또는 블록 내부에서 만들어진 바인딩은 `elif` `else` 끝 뒤에 표시 되지 않습니다.

예를 들면 다음과 같습니다.

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
또는
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
문은 키워드, `for` 여는 괄호 `(` , 기호 또는 기호 튜플, 키워드 `in` , 형식 `Range` 또는 배열의 식, 닫는 괄호 `)` 및 문 블록으로 구성 됩니다.

문 블록 (루프의 본문)은 범위 또는 배열의 각 값에 바인딩된 정의 된 기호 (루프 변수)를 사용 하 여 반복적으로 실행 됩니다.
범위 식이 빈 범위 또는 배열로 계산 되는 경우 본문은 실행 되지 않습니다.
식은 루프를 시작 하기 전에 완전히 계산 되며 루프가 실행 되는 동안에는 변경 되지 않습니다.

루프 변수는 루프 본문에 대 한 각 입구에 바인딩되고 본문의 끝에서 바인딩되지 않습니다.
특히 for 루프가 완료 된 후 루프 변수가 바인딩되지 않습니다.
선언 된 기호의 바인딩은 변경할 수 없으며 다른 변수 바인딩과 동일한 규칙을 따릅니다. 

몇 가지 예를 들어, 다음은 형식에 대 한 `qubits` 레지스터입니다. `Qubit[]` 

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
끝에는 산술 시프트 왼쪽 이항 연산자를 사용 했습니다 .이에 대 한 `<<<` 세부 정보는 [숫자 식](xref:microsoft.quantum.guide.expressions#numeric-expressions) 에서 찾을 수 있습니다.


## <a name="repeat-until-success-loop"></a>반복-성공 루프

Q # 언어를 사용 하면 기존 제어 흐름을 사용 하 여 다양 한 비트 측정 결과에 따라 달라 집니다.
이 기능을 사용 하면 unitaries을 구현 하기 위한 계산 비용을 줄일 수 있는 강력한 확률 가젯을 구현할 수 있습니다.
예를 들어 Q #에서 쉽게 구현할 수 있습니다 (RUS ( *-성공-성공* ) 패턴 이라고 함).
이러한 RUS 패턴은 기본 게이트 측면에서 비용이 *저렴 한* 확률 프로그램 이지만 실제 실행 및 가능한 여러 가지 branchings의 실제 인터리브에 따라 실질적인 비용이 달라 집니다.

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

반복/until 루프의 세 부분 (본문, 테스트 및 픽스업)은 *각 반복에 대해*단일 범위로 처리 되므로 본문에 바인딩된 기호는 테스트 및 픽스업에서 사용할 수 있습니다.
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

이 페이지의 맨 아래에는 [RUS 루프의 몇 가지 예가 나와](#repeat-until-success-examples)있습니다.

> [!TIP]   
> 함수 내에서-success 루프를 사용 하지 마십시오. 함수에서 루프를 통해 해당 기능을 제공 합니다. 

## <a name="while-loop"></a>While 루프

반복-성공 패턴에는 퀀텀 별 connotation가 있을 수 있습니다. 이러한 클래스는 특정 퀀텀 알고리즘 클래스에서 널리 사용 되므로 Q #에서 전용 언어 구문을 사용 합니다. 그러나 조건에 따라 중단 되 고 해당 실행 길이는 컴파일 시간에 알 수 없는 루프는 퀀텀 런타임에서 특히 주의 해 서 처리 해야 합니다. 반면에 함수 내에서의 사용은 기존 (비 퀀텀) 하드웨어에서 실행 되는 코드만 포함 하기 때문에 문제가 되지 않습니다. 

따라서 Q #은 함수 내 에서만 while 루프를 사용할 수 있도록 지원 합니다. `while`문은 키워드, 여는 `while` 괄호 `(` , 조건 (예: 부울 식), 닫는 괄호 `)` 및 문 블록으로 구성 됩니다.
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

빈 튜플을 반환 하는 호출 가능에는 `()` return 문이 필요 하지 않습니다.
초기 종료를 사용 하는 경우 `return ()` 이 경우를 사용할 수 있습니다.
다른 형식을 반환 하는 callables에는 최종 return 문이 필요 합니다.

작업 내에는 최대 개수의 return 문이 없습니다.
문이 블록 내의 return 문 뒤에 오는 경우 컴파일러는 경고를 생성할 수 있습니다.

예를 들면 다음과 같습니다.
```qsharp
return 1;
```
또는
```qsharp
return ();
```
또는
```qsharp
return (results, qubits);
```

## <a name="fail-statement"></a>Fail 문

Fail 문은 작업 실행을 종료 하 고 호출자에 게 오류 값을 반환 합니다.
키워드 `fail` 와 문자열 및 종료 세미콜론으로 구성 됩니다.
문자열은 오류 메시지로 기존 드라이버에 반환 됩니다.

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

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a>무리 축에 대 한 단일 고 비트 회전에 대 한 RUS 패턴 

일반적인 사용 사례에서 다음 Q # 연산은 Bloch 구의 $ (I + 2i Z)/\sqrt $의 무리 축을 중심으로 회전을 구현 {5} 합니다. 이 작업은 알려진 RUS 패턴을 사용 하 여 수행 됩니다.

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

### <a name="rus-loop-with-mutable-variable-in-scope"></a>범위에서 변경 가능한 변수가 있는 RUS 루프

이 예에서는 `finished` 전체 반복-픽스업 루프의 범위에 있고 루프 전에 초기화 되 고 픽스업 단계에서 업데이트 되는 변경 가능한 변수를 사용 하는 방법을 보여 줍니다.

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

예를 들어 다음 코드는 {5} 및 게이트를 사용 하 여 $V _3 = (\boldone + 2 i Z)/\sqrt $ 중요 한 회전 게이트를 구현 하는 확률 회로입니다 `H` `T` .
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

마지막으로 {1} $ \ket{+} $ 상태에서 시작 하 여 퀀텀 상태 $ \frac {\sqrt {3} } \left (\sqrt {2} \ket {0} + \ket {1} \right) $를 준비 하는 RUS 패턴의 예를 보여 줍니다.
[표준 라이브러리와 함께 제공 되는 단위 테스트 샘플](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs)도 참조 하세요.

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

이 작업에 표시 되는 주목할 만한 프로그래밍 기능은 `fixup` 퀀텀 작업을 포함 하는 루프의 더 복잡 한 부분이 며, `AssertProb` 문을 사용 하 여 프로그램의 지정 된 특정 지점에서 퀀텀 상태를 측정 하는 확률을 확인 합니다.
및 작업에 대 한 자세한 내용은 [테스트 및 디버깅](xref:microsoft.quantum.guide.testingdebugging) 을 참조 하세요 [`Assert`](xref:microsoft.quantum.intrinsic.assert) [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) .


## <a name="whats-next"></a>다음 단계
Q #에서 [테스트 및 디버깅](xref:microsoft.quantum.guide.testingdebugging) 에 대해 알아봅니다.