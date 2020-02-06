---
title: 'Q # 표준 라이브러리-특징 | Microsoft Docs'
description: 'Q # 표준 라이브러리-특징'
author: QuantumWriter
uid: microsoft.quantum.libraries.characterization
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 0c347113339a77e9eaf63dc0967c320f8b063a0e
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036256"
---
# <a name="quantum-characterization-and-statistics"></a>퀀텀 특성화 및 통계 #

유용한 퀀텀 알고리즘을 개발 하기 위해 작업 효과의 특징을 지정할 수 있어야 합니다.
이는 퀀텀 시스템의 모든 측정값이 최대 1 비트 정보를 생성 하기 때문입니다.
사용자가 이러한 개념을 나타내는 데 필요한 많은 양의 정보를 공개할 수 있도록 eigenvalue를 학습 하 고,이를 사용 하 여 여러 측정값의 결과를 함께 연결 되어 해야 합니다.
퀀텀 상태는 특히 상태를 복사 하는 것이 가능 하기 때문에 [정리](xref:microsoft.quantum.concepts.pauli#the-no-cloning-theorem) 의 단일 복사본에서 임의의 퀀텀 상태를 학습할 방법이 없다는 것을 vexing 때문입니다.
사용자의 퀀텀 상태 난독 처리는 Q #에서 퀀텀 프로그램에 대 *한 상태를* 노출 하거나 정의 하지 않는다는 사실에 반영 됩니다.
따라서 작업 및 상태를 블랙 박스로 처리 하 여 퀀텀 특징을 접근 합니다. 이 접근 방식은 퀀텀, 확인 및 유효성 검사 (QCVV)의 실험적 사례와 공통적으로 많이 공유 됩니다.

용어는 앞에서 설명한 대부분의 다른 라이브러리와는 다릅니다.
여기서는 상태 벡터에서 단일 변환을 수행 하는 대신 시스템에 대 한 기존 정보를 배우는 것이 더 낮습니다.
따라서 이러한 라이브러리는 기존 및 퀀텀 정보 처리를 모두 혼합 해야 합니다.


## <a name="iterative-phase-estimation"></a>반복 단계 예측 ##

퀀텀 용어를 기준으로 퀀텀 프로그래밍을 보면 퀀텀 단계 추정에 대 한 유용한 대안이 될 수 있습니다.
즉, 퀀텀 단계 추정에서와 같이 단계의 이진 표현을 포함 하도록 $-hbit 레지스터 $n을 준비 하는 대신, *기존* 에이전트가 측정값을 통해 퀀텀 시스템의 속성을 학습 하는 프로세스로 단계 예측을 볼 수 있습니다.
Kickback 단계를 사용 하 여 블랙 박스 작업의 응용 프로그램을 알 수 없는 각도 만큼 회전으로 전환 하는 퀀텀 사례에서 작업을 진행 하면서 각 단계에서 회전 직후 회전 하는 ancilla를 측정 합니다.
이는 퀀텀 사례에 설명 된 단계를 수행 하는 데 하나의 추가 kickback 필요 하지만 반복적인 방식으로 각 단계의 측정 결과에서 단계를 알아보는 것입니다.  
아래에서 제안 하는 각 방법은 실험을 설계 하 고 다양 한 데이터 처리 방법을 사용 하 여 단계를 학습할 수 있는 다른 전략을 사용 합니다.  각 사용자에 게는 엄격한 오류 범위를 포함 하는 것부터 이전 정보를 포함 하는 기능, 오류를 허용 하거나 메모리 limitted 클래식 컴퓨터에서 실행 하는 기능에 이르기까지 고유한 이점이 있습니다.

반복 단계 예측에 대해 논의 하는 경우 블랙 박스 작업으로 제공 되는 단일 $U $을 고려 합니다.
Oracles의 [데이터 구조](xref:microsoft.quantum.libraries.data-structures)에 대 한 섹션에 설명 된 대로 튜플 형식으로 정의 된 <xref:microsoft.quantum.oracles.discreteoracle> 사용자 정의 형식에의 한 Q # 라고 모델은 `((Int, Qubit[]) => Unit : Adjoint, Controlled)`합니다.
구체적으로 인 `U : DiscreteOracle`경우에는 `m : Int`에 대 한 $U ^ m $을 구현 `U(m)`.

이 정의를 사용 하 여 반복 단계 예측의 각 단계는 초기 상태 $ \ket{\phi} $와 함께 $ \ket{+} $ 상태에서 보조 비트를 준비 하 여 진행 됩니다 .이는 $U [eigenvector](xref:microsoft.quantum.concepts.matrix-advanced) (m) $, 즉 $U (m) \ket{\phi} = e ^ {im\eml\ k {\ l o} $입니다.  
그런 다음 `U(m)`의 제어 된 응용 프로그램을 사용 하 여 $ \left (R\_1 (m \left) \ket{+} \left) $ 상태를 준비 합니다.
퀀텀 사례에서와 같이 oracle `U(m)` 제어 되는 응용 프로그램의 영향은 $ \ket{+} $에서 알 수 없는 단계에 대해 $R _1 $을 적용 하는 것과 정확 하 게 동일 합니다 .이에 따라 $U $의 효과를 보다 간단한 방식으로 설명할 수 있습니다.
필요에 따라이 알고리즘은 \ket{\psi} (-m\theta) $을 $R 적용 하 여 상태 $ = \left (R\_1 (m [\phi-\theta]) \ket{+} \right) \ket{\phi} $ $를 가져와 컨트롤을 회전 합니다.
그런 다음 `U(m)`에 대 한 컨트롤로 사용 되는 보조 비트를 $X $ 기준으로 측정 하 여 단일 클래식 `Result`을 가져옵니다.

이 시점에서 반복 단계 예측을 통해 얻은 `Result` 값에서 단계를 다시 생성 하는 것은 기존 통계 유추 문제입니다.
고정 유추 방법이 제공 되는 경우 얻은 정보를 최대화 하는 $m $ 값을 찾는 것은 단순히 통계의 문제입니다.
이 기존 유추 문제를 해결 하기 위해 Q # 라고에서 제공 된 통계 알고리즘을 설명 하기 전에 Bayesian 매개 변수 추정 정해진 이론적 수준에서 반복적 단계 예측을 간략하게 설명 하 여이를 강조 합니다.

### <a name="iterative-phase-estimation-without-eigenstates"></a>Eigenstates 없이 반복 단계 예측 ###

Eigenstate가 아닌 입력 상태를 제공 하는 경우 ($U (m) \ket{\phi\_j} = e ^ {im\emname\_j} $ 인 경우 단계 추정 프로세스는 단일 에너지 eigenstate에 대 한 퀀텀 상태를 명확 하 게 안내 합니다.  궁극적으로 수렴 하는 eigenstate는 관찰 된 `Result`를 생성할 가능성이 가장 높은 eigenstate입니다.

특히, PE의 단일 단계는 상태 \begin{align} \ sum_j \sqrt{\Pr (\a\_j)} \ket{\phi\_j} \maps\\a\a\_j\frac {\ sqrt {\ Pr (\_\\aaj)}에 대해 다음과 같은 비 단일 변환을 수행 합니다. \sqrt{\Pr (\text{Result} | \a\_j)} \ket{\phi\_j}} {\sqrt{\Pr (\\a\_j) \sum\_j \Pr (\text{Result} | \\a\_j)}}.
이 프로세스가 여러 `Result` 값에 대해 반복 되는 것으로 \end{align}, 최대 값이 $ \ prod_k \Pr (\text{Result}\_k | \\a\_j) $ 인 eigenstates는 계속 해 서 표시 되지 않습니다.
따라서 실험을 제대로 선택 하면 유추 프로세스는 단일 eigenvalue를 사용 하 여 상태로 수렴 하는 경향이 있습니다.

Bayes ' 정리 \begin{align} \frac{\sqrt{\Pr (\a\_j)} \sqrt{\Pr (\text{Result} | \a\_j)} \ket{\phi\_j}} {\sqrt{s로 생성 되는 상태를 추가로 제안 합니다. \Phi (\a\_j) \phi\_j \Phi (\text{Result} | \a\_j)}} = \ sum_j \sqrt{\Pr (\aa\_j | \text{Result})} \ket{\phi\_j}.
\end{align} 여기 $ \Pr (\a\_j | \text{Result}) $는 지정 된 eigenstates에 대 한 각 가설에 ascribe 확률로 interpretted 수 있습니다.

1. 측정 전의 퀀텀 상태에 대 한 지식
2. $U $ 및의 eigenstates에 대 한 지식
3. $U $의 고유 값에 대 한 정보입니다.

이러한 세 가지 작업을 수행 하는 것은 일반적으로 기존 컴퓨터에서 매우 하드 디스크입니다.
단계 예측의 유틸리티는 이러한 작업을 알지 못해도 이러한 퀀텀 학습 작업을 수행할 수 있다는 사실에서 작은 익스텐트가 발생 하지 않습니다.
이러한 이유에 대 한 단계 예측은 지 수 속도를 제공 하는 여러 퀀텀 알고리즘 내에 표시 됩니다.

### <a name="bayesian-phase-estimation"></a>Bayesian 단계 예측 ###

> [!TIP]
> Bayesian 단계 예측에 대 한 자세한 내용은 [**PhaseEstimation**](https://github.com/microsoft/Quantum/tree/master/samples/characterization/phase-estimation) 샘플을 참조 하세요.

Bayesian 단계 추정의 개념은 간단 합니다.
단계 추정 프로토콜에서 측정 통계를 수집한 다음 Bayesian 유추를 사용 하 여 결과를 처리 하 고 예상 된 매개 변수를 제공 합니다.
이러한 처리를 통해 예상 값을 예측할 수 있을 뿐만 아니라 예상 값을 예측할 수 있습니다.
또한 적응 실험을 수행 하 고 이전 정보를 활용할 수 있습니다.
메서드의 원칙에 대 한 단점은 계산을 요구 하는 것입니다.

이 Bayesian 유추 프로세스가 작동 하는 방식을 이해 하려면 단일 `Zero` 결과를 처리 하는 경우를 고려 합니다.
$X = \ket{+} \bra{+}-\ket{-}\bra{-}$와 같이 $ \ket{+} $는 `Zero`에 해당 하는 $X $의 유일한 긍정 eigenstate입니다.
입력 상태 $ \ket{\psi}\ket{\phi} $로 지정 된 첫 번째 [값에서`PauliX` 측정](xref:microsoft.quantum.concepts.pauli) 에 대 한 `Zero`를 관찰 하는 확률에 대 한 확률 \braket{+ | \psi} \right | ^ 2.
\end{equation} 반복적인 단계 예측의 경우 $ \ket{\psi} = R_1 (m [\phi-\theta]) \ket{+} $ (\begin{align} \Pr (\texttt{Zero} | \\asa; m, \테타) & = \left | \braket{+ | R_1 (m [\phi-\theta]) | +} \right | ^ 2 \\\\ & = \right | \frac12 \left (\bra{0} + \bra{1} \left) \left (\ket{0} + e ^ {i m [\phi-\theta]} \ket{1} \left) \left | ^ 2 \\\\ & = \left | \frac{1 + e ^ {i m [\phi-\theta]}{2} \right | ^ 2 \\\\ & = \right ^ 2 (m [\phi-\theta]/2) \tag{★} \label{eq:}.
\end{align} 반복 단계 추정은 해당 sinusoid로 지정 된 바이어스로 동전을 대칭 이동 하는 기능을 제공 하 여 사인 곡선 함수의 진동 범위가 빈도를 학습 하는 것으로 구성 됩니다.
기존의 기존 용어에 따라 $ \eqref{eq:} $는 반복적인 단계 예측에 대 한 *가능성 함수* 를 호출 합니다.

반복 단계 예측 가능성 함수에서 `Result`를 관찰 한 후에는 Bayes ' 규칙을 사용 하 여 이러한 관찰을 수행 해야 하는 단계를 규정 하 고 있습니다.
구체적으로, \begin{equation} \A\\\\\\\\frac{\Pr (d | \) \Pr (\aa>} {\int \Pr (d | \\a) \Pr (\aa) {\mathrm d} \phi} \Aa> \begin{equation} 여기서 $d \cin \\{\texttt{Zero}, \texttt{One}\\} $는 `Result`이 고 $ \Pr (\aa) $은 이전 신념 about $ \\as$를 설명 합니다.
그러면 사후 배포 $ \Pr (\\ax) $가 다음 `Result`의 관찰 바로 앞에 신념을 설명 하므로 반복적인 단계 예측의 반복적인 특성을 명시적으로 만듭니다.

이 절차를 수행 하는 동안 언제 든 지 클래식 컨트롤러에서 유추 된 $ \hat{\phi} $ 단계를 \begin{equation} \hat{\phi} \mathrel{로 보고할 수 있습니다. =} \ [\\a| \text{data}] = \int \Las\pr (\laa| \text{data}) {\mathrm d} \\a\ariation} where $ \text{data} $는 가져온 모든 `Result` 값의 전체 레코드를 나타냅니다.

정확한 Bayesian 유추는 실제로 intractable입니다.
이에 대 한 자세한 내용은 $ 비트 변수 $x $를 $n 합니다.
이전 배포 $ \Pr (x) $는 $2 ^ n $ $x $의 가상 값을 지원 합니다.
즉, $x를 매우 정확 하 게 예측 해야 하는 경우에는 Bayesian 단계 예측에 필요한 메모리 및 처리 시간이 너무 늘어날 수 있습니다.
퀀텀 시뮬레이션 같은 일부 응용 프로그램의 경우에는 limitted 정확도가 Shor의 알고리즘과 같은 다른 응용 프로그램에서 해당 단계 예측 단계 내에 정확한 Bayesian 유추를 사용할 수 없습니다.  이러한 이유로 [RWPE (임의 워크 단계 예측)](xref:microsoft.quantum.research.randomwalkphaseestimation.randomwalkphaseestimation) 와 같은 대략적인 Bayesian 메서드 및 [강력한 단계 추정치](xref:microsoft.quantum.characterization.robustphaseestimation)와 같은 Bayesian 없는 방법에 대 한 구현도 제공 합니다.

### <a name="robust-phase-estimation"></a>강력한 단계 예측 ###

측정 결과에서 단계 추정치의 최대 *posteriori* Bayesian 재구성은 최악의 경우에는 매우 어렵습니다. 따라서 대부분의 실용적인 단계 예측 알고리즘은 구성의 몇 가지 품질을 저하 시킬 수 있습니다 .이 알고리즘은 측정 횟수로 polynomially를 확장 하는 일반적인 사후 처리의 양에 대 한 것입니다.

효율적인 기존 사후 처리 단계를 사용 하는 예 중 하나는 위에 언급 된 시그니처와 입력이 있는 [강력한 단계 추정 알고리즘](https://arxiv.org/abs/1502.02677)입니다. 입력 된 단일 블랙 박스 $U $가 `DiscreteOracle` 형식으로 패키지 되는 것으로 가정 합니다. 따라서 정수는 제어 된 $U $로만 쿼리 합니다. `Qubit[]` 레지스터의 입력 상태가 eigenstate $U \ket{\psi} = e ^ {i\em} \ k {\ psi} $ 인 경우, 강력한 단계 추정 알고리즘은 $ \eml$의 예상 $ \hat{\phi}\in [-\pi, \pi) $를 `Double`로 반환 합니다.

가장 많이 사용 되는 다른 변형에서 공유 되는 강력한 단계 추정의 가장 중요 한 기능은 $ \hat{\phi} $의 재구성 품질이 Heisenberg 제한 되어 있다는 것입니다. 즉, 값이 $ \sigma $ 인 $ \hat{\phi} $의 편차가 $ \sigma $ 인 경우 $ \sigma $는 $U $ (예: $ \sigma = \mathcal{O} (1/Q) $로 만든 $Q 총 쿼리 수에 반비례 하 게 비례 합니다. 이제 편차에 대 한 정의는 예측 알고리즘 마다 다릅니다. 경우에 따라 $ \mathcal{O} (1) $ probability를 사용 하는 경우 예상 오류 $ | \hat{\phi}-\phi |를 의미할 수 있습니다. \circ\le \sigma $를 일부 순환 측정값 $ \sigma $에\_합니다. 강력한 단계 예측의 경우 편차는 일정 한 간격으로 \mathbb{E}을 정확 하 게 분산 하는 것은 $ \sigma ^ 2 =\_\hat{\phi} [(\sigma\_{2 \ pi} (\hat{\phi}-\phi + \sigma)-\sigma) ^ 2] $입니다. 좀 더 정확 하 게 말하자면, 강력한 단계 추정의 표준 편차는 같지 $ $ \begin{align} 2.0 \pi/Q \pi \pi \pi 2 \ pi/2 ^ {n} \pi 10.7 \ pi/Q, \end{align} $ $를 충족 합니다. 여기서 하한값은 asymptotically large $Q $로 제한 되며, 상한값은 작은 샘플 크기에 대해서도 보장 됩니다.  $N $는 `bitsPrecision` 입력으로 선택 되며, $Q $를 암시적으로 정의 합니다.

그 밖의 관련 세부 정보에는 $1 $ ancilla?의 작은 공간 오버 헤드 또는 프로시저가 비 적응 (예를 들어, 퀀텀 실험의 필수 시퀀스는 중간 측정 결과와 무관)이 있습니다. 단계 추정 알고리즘의 선택이 중요 한이 예제와 향후 예제에서는 @"microsoft.quantum.characterization.robustphaseestimation"와 같은 설명서를 참조 하 고 해당 구현에 대 한 참조 된 게시를 참조 해야 합니다.

> [!TIP]
> 강력한 단계 예측을 사용 하는 많은 샘플이 있습니다. 다양 한 물리적 시스템의 그라운드 상태 에너지를 추출 하는 단계를 예측 하려면 [ **H2 시뮬레이션** 샘플](https://github.com/microsoft/Quantum/tree/master/samples/simulation/h2/command-line), [ **simpleising** 샘플](https://github.com/microsoft/Quantum/tree/master/samples/simulation/ising/simple)및 [ **model** 샘플](https://github.com/microsoft/Quantum/tree/master/samples/simulation/hubbard)을 참조 하세요.


### <a name="continuous-oracles"></a>연속 Oracles ###

또한 oracles를 사용 하 여 라고 <xref:microsoft.quantum.oracles.continuousoracle>유형에 의해 모델링 된 연속 시간을 허용 하기 위해 위에서 사용 하는 oracle 모델을 일반화할 수 있습니다.
단일 단일 연산자 대신 $ $U 하는 것이 아니라 (t) $ = $U (t + s) $와 $U 같은 $t \in \mathbb{R} $에 대 한 단일 연산자 $U (t) $를 포함 합니다.
일부 fixed $ \delta t $에 대해 $t = m\,\delta t $를 제한 하 여 <xref:microsoft.quantum.oracles.discreteoracle>를 생성할 수 있기 때문에이는 불연속 사례에서 보다 약한 문입니다.
일부 $H 연산자의 경우 [석재의 정리](https://en.wikipedia.org/wiki/Stone%27s_theorem_on_one-parameter_unitary_groups)(t) = \exp (i H t) $를 $U 합니다. 여기서 $ \exp $는 [고급 행렬](xref:microsoft.quantum.concepts.matrix-advanced)에 설명 된 대로 행렬 지 수입니다.
$H $의 eigenstate $ \ket{\phi} $는 $H \ket{\phi} = \em\ket{\phi} $이 고 모든 $t $, \begin{station} U (t) \ket{\phi} = e ^ {\\emt} \ket{\phi}.에 대 한 $U (t) $의 eigenstate 이기도 합니다.
\end{equation}

[Bayesian 단계 예측](#bayesian-phase-estimation) 에 대해 설명한 것과 정확히 동일한 분석을 적용할 수 있으며,이 함수는 보다 일반적인 oracle 모델인 $ $ \Pr (\texttt{Zero} | \\; t, \pr) = \pr ^ 2 \ left (\frac{t [\\an\테타]}{2}\pr)와 정확히 동일 합니다.
$ $ 또한 [Hamiltonian 시뮬레이션](xref:microsoft.quantum.libraries.applications#hamiltonian-simulation)의 경우와 마찬가지로 $ 동적 생성기의 시뮬레이션 인 $U 경우 $ \aa$를 에너지로 해석 합니다.
따라서 연속 쿼리를 사용 하 여 단계 예측을 사용 하면 $t $를 정수로 요구 하 여 선택한 [실험을 손상](https://arxiv.org/abs/1510.03859) [시 키 지](https://arxiv.org/abs/1111.3633v2) 않고 시뮬레이션 된 [에너지 스펙트럼의](https://arxiv.org/abs/quant-ph/0604193)시뮬레이션을 molecules 수 있습니다.

### <a name="random-walk-phase-estimation"></a>무작위 워크 단계 예측 ###

Q #에서는 반복 단계 추정에서 얻은 데이터 레코드에 대 한 임의 워크를 조절 하 여 작동 하는 퀀텀 장치에 가까운 사용을 위해 설계 된 Bayesian 단계 추정의 유용한 근사값을 제공 합니다.
이 메서드는 적응 및 완전히 결정적 이며, 예상 되는 단계 $ \hat{\phi} $에서 메모리 오버 헤드가 매우 낮으므로 거의 최적의 오류 확장을 허용 합니다.

프로토콜이 이전 분포를 가우스로 가정 하는 대략적인 Bayesian 유추 메서드를 사용 합니다.
이러한 가우시안 가정을 통해 사후 분산을 최소화 하는 실험에 대 한 분석 수식을 사용할 수 있습니다.
그런 다음 해당 실험의 결과에 따라 $ \a? $의 추정치를 미리 결정 된 양만큼 이동 하 고 미리 결정 된 양만큼 분산을 축소 합니다.
이 평균 및 가변성은 다음 실험을 위해 $ \\a$의 이전에 가우스을 지정 하는 데 필요한 모든 정보를 제공 합니다.
예기치 않은 측정 오류 이거나 초기 이전 앞부분과 뒷부분에 대 한 실제 결과가 발생 하면이 메서드가 실패할 수 있습니다.
실험을 수행 하 여 현재 평균과 표준 편차가 시스템에 적합 한지 테스트 하 여 오류 로부터 복구 합니다.
그렇지 않은 경우 알고리즘은 워크의 반대 단계를 수행 하 고 프로세스가 계속 진행 됩니다.
또한 뒤로 이동 하는 기능을 통해 초기 이전 표준 편차가 inapropriately 작은 경우에도 알고리즘을 배울 수 있습니다.

## <a name="calling-phase-estimation-algorithms"></a>단계 추정 알고리즘 호출 ##

Q # 라고과 함께 제공 되는 각 단계 예측 작업은 다른 입력 집합을 사용 하 여 최종 추정 $ \hat{\phi} $에서 요구 하는 품질을 매개 변수화 합니다.
그러나 이러한 다양 한 입력은 모두 공통 된 여러 입력을 공유 합니다. 예를 들어, 품질 매개 변수를 통해 부분 응용 프로그램에서 일반적인 서명이 발생 합니다.
예를 들어 다음 섹션에서 설명 하는 <xref:microsoft.quantum.characterization.robustphaseestimation> 작업에는 다음 서명이 있습니다.

```qsharp
operation RobustPhaseEstimation(bitsPrecision : Int, oracle : DiscreteOracle, eigenstate : Qubit[])  : Double
```

`bitsPrecision` 입력은 `RobustPhaseEstimation`에 고유 하며 `oracle` 및 `eigenstate`은 일반적입니다.
따라서 **H2Sample**에 표시 된 것 처럼 작업은 사용자가 임의 단계 추정 알고리즘을 지정할 수 있도록 `(DiscreteOracle, Qubit[]) => Unit` 폼의 입력을 사용 하 여 반복 단계 추정 알고리즘을 수락할 수 있습니다.

```qsharp
operation H2EstimateEnergy(
    idxBondLength : Int,
    trotterStepSize : Double,
    phaseEstAlgorithm : ((DiscreteOracle, Qubit[]) => Double))
: Double
```

이러한 방대한 단계 추정 알고리즘은 대상 응용 프로그램에 가장 적합 한 항목을 선택 하기 위해 이해 해야 하는 다양 한 속성 및 입력 매개 변수에 대해 최적화 됩니다. 예를 들어 일부 단계 추정 알고리즘은 적응입니다. 즉, 이후 단계는 이전 단계의 측정 결과에 의해 일반적으로 제어 됩니다. 일부 경우에는 임의 실수에 의해 블랙 박스 단일 oracle을 exponentiate 하는 기능이 필요 하 고, 다른 사용자에 게는 정수 거듭제곱이 필요 하지만 단계 추정 모듈로 $2 \ pi $를 해결할 수 있습니다. 일부는 많은 보조 비트 비트가 필요 하며, 다른 일부는 하나만 필요 합니다.

마찬가지로 임의의 워크 단계 예측을 사용 하는 것은 canon과 함께 제공 되는 다른 알고리즘과 거의 동일한 방식으로 진행 됩니다.

```qsharp
operation ApplyExampleOracle(
    eigenphase : Double,
    time : Double,
    register : Qubit[])
: Unit is Adj + Ctl {
    Rz(2.0 * eigenphase * time, register[0]);
}

operation EstimateBayesianPhase(eigenphase : Double) : Double {
    let oracle = ContinuousOracle(ApplyExampleOracle(eigenphase, _, _));
    using (eigenstate = Qubit()) {
        X(eigenstate);
        // The additional inputs here specify the mean and variance of the prior, the number of
        // iterations to perform, how many iterations to perform as a maximum, and how many
        // steps to roll back on an approximation failure.
        let est = RandomWalkPhaseEstimation(0.0, 1.0, 61, 100000, 1, oracle, [eigenstate]);
        Reset(eigenstate);
        return est;
    }
}
```
