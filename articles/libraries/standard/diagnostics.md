---
title: 'Q # 표준 라이브러리-진단 | Microsoft Docs'
description: 'Q # 표준 라이브러리-진단'
author: cgranade
uid: microsoft.quantum.libraries.diagnostics
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: d5889b8d5a92801b0ada65f7a17c655c959fc57f
ms.sourcegitcommit: 27c9bf1aae923527aa5adeaee073cb27d35c0ca1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/05/2019
ms.locfileid: "74864341"
---
# <a name="diagnostics"></a>진단 #

기존 개발과 마찬가지로 퀀텀 프로그램에서 실수 및 오류를 진단할 수 있는 것이 중요 합니다.
Q # 표준 라이브러리는 <xref:microsoft.quantum.techniques.testing-and-debugging>에 설명 된 대로 퀀텀 프로그램의 정확성을 보장 하는 다양 한 방법을 제공 합니다.
이러한 지원은 대부분 호스트 프로그램 또는 개발자에 게 추가 진단 정보를 제공 하도록 대상 컴퓨터에 지시 하거나 조건 및 고정의 정확성을 강제 적용 하는 함수 및 작업 형식으로 제공 됩니다. 함수 또는 작업 호출을 기준으로 합니다.

## <a name="machine-diagnostics"></a>컴퓨터 진단 ##

<xref:microsoft.quantum.intrinsic.message> 함수를 사용 하 여 컴퓨터 종속 방식으로 메시지를 기록 하 여 기존 값에 대 한 진단 정보를 얻을 수 있습니다.
기본적으로이 문자열은 콘솔에 기록 됩니다.
<xref:microsoft.quantum.intrinsic.message> 보간된 문자열과 함께 사용 하 여 기존 값에 대 한 진단 정보를 쉽게 보고할 수 있습니다.

```Q#
let angle = Microsoft.Quantum.Math.PI() * 2.0 / 3.0;
Message($"About to rotate by an angle of {angle}...");
```

> [!NOTE]
> `Message`에는 시그니처 `(String -> Unit)`있으며,이는 디버그 로그 메시지 내보내기가 Q # 내에서 관찰 될 수 없음을 나타냅니다.

<xref:microsoft.quantum.diagnostics.dumpmachine> 및 <xref:microsoft.quantum.diagnostics.dumpregister> callables은 대상 컴퓨터에 현재 할당 된 모든 기능에 대 한 진단 정보를 제공 하거나 각각의 특정 기능에 대 한 진단 정보를 제공 합니다.
각 대상 컴퓨터는 덤프 명령에 대 한 응답으로 제공 되는 진단 정보에 따라 달라 집니다.
예를 들어 [전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator) 대상 컴퓨터는 내부에서 사용 하는 상태 vector를 호스트 프로그램에 제공 하 여 해당 기능을 내부적으로 사용 합니다.
비교 하 여 [Toffoli 시뮬레이터](xref:microsoft.quantum.machines.toffoli-simulator) 대상 컴퓨터는 각 고 비트에 대해 단일 고전 비트를 제공 합니다.

 [전체 상태 시뮬레이터의](xref:microsoft.quantum.machines.full-state-simulator) `DumpMachine` 출력에 대해 자세히 알아보려면 [테스트 및 디버깅 문서의](xref:microsoft.quantum.techniques.testing-and-debugging#dump-functions)덤프 함수 섹션을 살펴보세요.


## <a name="facts-and-assertions"></a>팩트 및 어설션 ##

[테스트 및 디버깅](xref:microsoft.quantum.techniques.testing-and-debugging)에 설명 된 대로 시그니처 `Unit -> Unit` 또는 `Unit => Unit`를 사용 하는 함수 또는 작업은 각각 *단위 테스트*로 표시 될 수 있습니다.
각 단위 테스트는 일반적으로 해당 프로그램의 정확성을 확인 하는 하나 이상의 조건과 함께 작은 퀀텀 프로그램으로 구성 됩니다.
이러한 조건은 입력 값을 확인 하는 _팩트_형식 또는 입력으로 전달 된 하나 이상의 이상 상태를 확인 하는 _어설션_형식으로 제공 될 수 있습니다.

예를 들어 `EqualityFactI(1 + 1, 2, "1 + 1 != 2")`은 $1 + 1 = $2 이라는 수학적 팩트를 나타내며 `AssertQubit(One, qubit)`는 `qubit` 측정 하는 조건을 명확 하 게 `One` 반환 하는 조건을 나타냅니다.
이전 경우에는 해당 값만 제공 된 조건의 정확성을 확인할 수 있습니다. 후자의 경우에는 어설션을 평가 하기 위해 해당 값에 대 한 정보를 알고 있어야 합니다.

Q # 표준 라이브러리는 다음과 같은 여러 가지 기능을 제공 합니다.

- <xref:microsoft.quantum.diagnostics.fact>
- <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact>
- <xref:microsoft.quantum.diagnostics.nearequalityfact>
- <xref:microsoft.quantum.diagnostics.equalityfacti>


### <a name="testing-qubit-states"></a>비트율 비트 상태 테스트 ###

실제로 어설션은 퀀텀 메커니즘의 클래식 시뮬레이션이 [복제 안 함 정리](https://arxiv.org/abs/quant-ph/9607018)을 준수 하지 않아도 된다는 사실에 의존 합니다 .이를 위해 대상 컴퓨터에 시뮬레이터를 사용 하는 경우 비 물리적 측정과 어설션을 수행할 수 있습니다.
따라서 하드웨어에를 배포 하기 전에 기존 시뮬레이터에서 개별 작업을 테스트할 수 있습니다.
어설션 평가를 허용 하지 않는 대상 컴퓨터에서는 <xref:microsoft.quantum.intrinsic.assert>에 대 한 호출을 안전 하 게 무시할 수 있습니다.

보다 일반적으로 지정 된의 지정 된 비트를 측정 하는 <xref:microsoft.quantum.intrinsic.assert> 작업에는 항상 지정 된 결과가 포함 됩니다.
어설션이 실패 하면 지정 된 메시지와 함께 `fail`를 호출 하 여 실행이 종료 됩니다.
기본적으로이 작업은 구현 되지 않습니다. 이를 지원할 수 있는 시뮬레이터는 런타임 검사를 수행 하는 구현을 제공 해야 합니다.
`Assert`에 `((Pauli[], Qubit[], Result, String) -> ())`시그니처가 있습니다.
`Assert`는 빈 튜플을 출력 형식으로 사용 하는 함수 이므로 `Assert`를 호출한 결과는 Q # 프로그램 내에서 관찰 가능 하지 않습니다.

<xref:microsoft.quantum.intrinsic.assertprob> 작업 함수는 지정 된 Pauli의 지정 된 된 비트 수를 측정 하는 assert를 사용 하 여 지정 된 확률을 사용 하는 특정 결과를 허용 합니다.
허용 오차는 덧셈입니다 (예: `abs(expected-actual) < tol`).
어설션이 실패 하면 지정 된 메시지와 함께 `fail`를 호출 하 여 실행이 종료 됩니다.
기본적으로이 작업은 구현 되지 않습니다. 이를 지원할 수 있는 시뮬레이터는 런타임 검사를 수행 하는 구현을 제공 해야 합니다.
`AssertProb`에 `((Pauli[], Qubit[], Result, Double, String, Double) -> Unit)`시그니처가 있습니다. 첫 번째 `Double` 매개 변수는 원하는 결과의 확률을 제공 하 고 두 번째 매개 변수는 허용 오차를 제공 합니다.

단일 측정을 어설션하는 것 보다 더 많은 작업을 수행할 수 있습니다. 시뮬레이터에서 사용 되는 기존 정보를 복사 하는 것이 적합할,이를 통해 실제로 어설션을 테스트할 수 있습니다.
특히,이를 통해 실제 하드웨어에서 사용할 수 없는 *호환 되지* 않는 측정에 대해 설명할 수 있습니다.

\Ket{\psi}가 $ \ket{0}$ 상태에 있을 때 $ $ 상태를 준비 하기 위한 작업 이라고 `P : Qubit => Unit` 가정 합니다.
$ \Ket{\psi '} $는 `P`에서 준비한 실제 상태가 되도록 합니다.
$ \Ket{\psi} $에서 설명 하는 축에서 $ \ket{\psi '} $를 측정 하는 경우에만 $ \ket{\psi} = \ket{\psi '} $가 항상 `Zero`을 반환 합니다.
즉, \begin{align} \ket{\psi} = \ket{\psi '} \text{} \braket{\psi | \psi '} = 1 인 경우에만 해당 합니다.
prelude에 정의 된 기본 작업을 사용 하 여 \end{align} $ \ket{\psi} $가 Pauli 연산자 중 하나의 eigenstate 인 경우 `Zero`를 반환 하는 측정값을 직접 수행할 수 있습니다.


작업 <xref:microsoft.quantum.diagnostics.assertqubit>에서는 어설션을 $ \ket{\psi} = \ket{0}$로 테스트 하려는 경우에 특히 유용한 약어를 제공 합니다.
예를 들어이를 해제 하기 전에 ancilla를 $ \ket{0}$로 반환 하기 위해 계산 되지 않은 경우에 일반적입니다.
$ \Ket{0}$에 대 한 어설션은 두 상태 준비 `P` 및 `Q` 작업이 모두 동일한 상태를 준비 하 고 `Q` `Adjoint`를 지 원하는 경우에도 유용 합니다.
특히,

```qsharp
using (register = Qubit()) {
    P(register);
    Adjoint Q(register);

    AssertQubit(Zero, register);
}
```

그러나 일반적으로 Pauli 연산자의 eigenstates와 일치 하지 않는 상태에 대 한 어설션을 액세스할 수 없습니다.
예를 들어 $ \ket{\psi} = (\ket{0} + e ^ {i \pi/8} \ket{1})/\pi{2}$는 <xref:microsoft.quantum.intrinsic.assertprob>를 사용 하 여 $ \ket{\psi '} $ 상태가 $ \ket{\psi} $와 같은지를 고유 하 게 확인할 수 없는 경우와 같이 Pauli 연산자의 eigenstate가 아닙니다.
대신, 시뮬레이터에서 지 원하는 기본 형식을 사용 하 여 직접 테스트할 수 있는 가정으로 assertion $ \ket{\psi '} = \ket{\psi} $를 분해 해야 합니다.
이렇게 하려면 $ \ket{\psi} = \alpha \ket{0} + \alpha \ket{1}$ 복소수에 대해 $ \alpha = a\_r + a\_i i $ 및 $ \alpha $를 사용 합니다.
이 식에는 각 복소수를 실수와 허수부의 합계로 표현할 수 있으므로 $\{\_r, a\_i, b\_r, b\_i\}$ 네 개의 실수 숫자가 필요 합니다.
그러나 글로벌 단계 때문에 $a\_i = $0를 선택할 수 있습니다. 예를 들어, 단일가 나 비트 상태를 고유 하 게 지정 하기 위해 세 가지 실수만 필요 합니다.

따라서 필요한 상태를 어설션할 수 있도록 서로 독립적인 세 가지 어설션을 지정 해야 합니다.
이를 위해 $ \alpha $ 및 $ \alpha $를 지정 하 고 각각을 독립적으로 어설션하는 각 Pauli에 대 한 `Zero` 관찰 확률을 찾습니다.
$X $, $y $ 및 $z $를 각각 Pauli $X $, $Y $ 및 $Z $ 측정값에 대 한 `Result` 값으로 사용 합니다.
그런 다음 퀀텀 측정값에 대 한 유사도 함수를 사용 하 여 \begin{align} \Pr (x = \texttt{Zero} | \pr, \pr) & = \frac12 + a\_r b\_r + a\_i b\_\\\\ \Pr (y = \texttt{Zero} | \pr, \pr) & = \frac12 + a\_r b\_i-a\_i b\_r \\\\ \Pr (z = \texttt{Zero} | \pr, \pr) & = \frac12\left (1 + a\_r ^ 2 + a\_i ^ 2 + b\_r ^ 2 + b\_i ^ 2 \right).
\end{align}

<xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> 작업에서는 $ \alpha $ 및 $ \alpha $의 지정 된 표현이 <xref:microsoft.quantum.math.complex>형식의 값으로 지정 된 이러한 어설션을 구현 합니다.
이는 예상 상태를 수학적으로 계산할 수 있는 경우에 유용 합니다.

### <a name="asserting-equality-of-quantum-operations"></a>퀀텀 작업의 같음 어설션 ###

지금까지 특정 상태를 준비 하기 위한 테스트 작업과 관련 하 여 노력 했습니다.
그러나 종종 단일 고정 입력이 아닌 임의의 입력에 대해 작업을 수행 하는 방법에 관심이 있습니다.
예를 들어 일련의 단일 연산자 $U (t) $에 해당 하는 작업 `U : ((Double, Qubit[]) => () : Adjoint)`를 구현 했으며 `adjoint auto`를 사용 하는 대신 명시적인 `adjoint` 블록을 제공 했다고 가정 합니다.
$T $가 진화 시간을 나타내는 경우 예상 대로 ^ \aa&gt (t) = U (-t) $ $U를 어설션하는 데 관심이 있을 수 있습니다.

두 가지 작업을 `U` 하 고 `V` 동일 하 게 작동 하는 어설션을 만들기 위해 수행할 수 있는 두 가지 전략이 있습니다.
첫째, `U(target); (Adjoint V)(target);`이 지정 된 기준으로 각 상태를 유지 하는지 확인할 수 있습니다.
둘째, entangled의 절반에 대해 작동 하는 `U(target); (Adjoint V)(target);`이 해당을 유지 하는지 확인할 수 있습니다.
이러한 전략은 각각 라고 작업 <xref:microsoft.quantum.diagnostics.assertoperationsequalinplace> 및 <xref:microsoft.quantum.diagnostics.assertoperationsequalreferenced>에 의해 구현 됩니다.

> [!NOTE]
> 위에 설명 된 참조 어설션은 $2n $ Choi – $ Jamiłkowski isomorphism에 대 한 $n 작업을 연결 하는 수학적 프레임 워크인 [–](https://en.wikipedia.org/wiki/Channel-state_duality)을 기반으로 작동 합니다.
> 특히 $ \ket{\ beta_의 ${00}} \mathrel{: =} (\ket{00} + \ket{11})/\sqrt{2}$를 $n $에 $n 대 한 id 작업을 나타냅니다.
> 작업 <xref:microsoft.quantum.preparation.preparechoistate>이 isomorphism를 구현 하 여 지정 된 작업을 나타내는 상태를 준비 합니다.

대략 이러한 전략은 시간 공간 균형에 따라 구분 됩니다.
각 입력 상태를 반복 하는 데는 추가 시간이 소요 되지만 되거나 얽 히를 참조로 사용 하는 경우 추가 추가 비트를 저장 해야 합니다.
작업에서 해독 가능한 클래식 작업을 구현 하는 경우 (계산 기준 상태에만 관심이 있음)이 제한 된 입력 집합에 대 한 같음 테스트를 <xref:microsoft.quantum.diagnostics.assertoperationsequalinplacecompbasis> 합니다.

> [!TIP]
> 입력 상태 반복은 열거형 작업 <xref:microsoft.quantum.canon.iteratethroughcartesianproduct> 및 <xref:microsoft.quantum.canon.iteratethroughcartesianpower>에 의해 처리 됩니다.
> 이러한 작업은 일반적으로 두 개 이상의 집합 사이에 있는 카티션 product의 각 요소에 작업을 적용 하는 데 유용 합니다.

그러나 두 가지 접근 방식은 검사 중인 작업의 다른 속성을 테스트 하는 것입니다.
내부 어설션은 각 작업을 여러 번 호출 하므로 입력 상태 마다 한 번씩 임의의 선택 및 측정 결과가 호출 사이에서 변경 될 수 있습니다.
이와 대조적으로 참조 된 어설션은 각 작업을 정확히 한 번 호출 하 여 *단일 샷에*작업이 동일한 지 확인 합니다.
이러한 테스트는 모두 퀀텀 프로그램의 정확성을 보장 하는 데 유용 합니다.


## <a name="further-reading"></a>추가 참고 자료 ##

- <xref:microsoft.quantum.techniques.testing-and-debugging>
- <xref:microsoft.quantum.diagnostics>
