---
uid: Microsoft.Quantum.Research.Characterization.RandomWalkPhaseEstimation
title: RandomWalkPhaseEstimation 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Characterization
qsharp.name: RandomWalkPhaseEstimation
qsharp.summary: Performs iterative phase estimation using a random walk to approximate Bayesian inference on the classical measurement results from a given oracle and eigenstate.
ms.openlocfilehash: f9edafcce62c8b30a6bd52b7dbaa2df2c50c920d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846012"
---
# <a name="randomwalkphaseestimation-operation"></a><span data-ttu-id="e3c9c-102">RandomWalkPhaseEstimation 작업</span><span class="sxs-lookup"><span data-stu-id="e3c9c-102">RandomWalkPhaseEstimation operation</span></span>

<span data-ttu-id="e3c9c-103">네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Characterization) .</span><span class="sxs-lookup"><span data-stu-id="e3c9c-103">Namespace: [Microsoft.Quantum.Research.Characterization](xref:Microsoft.Quantum.Research.Characterization)</span></span>

<span data-ttu-id="e3c9c-104">패키지: [Microsoft](https://nuget.org/packages/Microsoft.Quantum.Research.Characterization) .</span><span class="sxs-lookup"><span data-stu-id="e3c9c-104">Package: [Microsoft.Quantum.Research.Characterization](https://nuget.org/packages/Microsoft.Quantum.Research.Characterization)</span></span>


<span data-ttu-id="e3c9c-105">임의 워크를 사용 하 여 반복 단계 예측을 수행 하 여 지정 된 oracle 및 eigenstate에서 얻은 기존 측정 결과에 대 한 Bayesian 유추를 대략적으로 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-105">Performs iterative phase estimation using a random walk to approximate Bayesian inference on the classical measurement results from a given oracle and eigenstate.</span></span>

```qsharp
operation RandomWalkPhaseEstimation (initialMean : Double, initialStdDev : Double, nMeasurements : Int, maxMeasurements : Int, unwind : Int, oracle : Microsoft.Quantum.Oracles.ContinuousOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a><span data-ttu-id="e3c9c-106">입력</span><span class="sxs-lookup"><span data-stu-id="e3c9c-106">Input</span></span>

### <a name="initialmean--double"></a><span data-ttu-id="e3c9c-107">initialMean: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e3c9c-107">initialMean : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e3c9c-108">$ \\A$를 통한 초기 정규 이전 배포의 평균입니다.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-108">Mean of the initial normal prior distribution over $\phi$.</span></span>


### <a name="initialstddev--double"></a><span data-ttu-id="e3c9c-109">initialStdDev: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e3c9c-109">initialStdDev : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e3c9c-110">$ \Phi $를 통한 초기 표준 이전 배포의 표준 편차입니다.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-110">Standard deviation of the initial normal prior distribution over $\phi$.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="e3c9c-111">n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e3c9c-111">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e3c9c-112">최종 사후 예상치에 허용할 측정 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-112">Number of measurements to be accepted into the final posterior estimate.</span></span>


### <a name="maxmeasurements--int"></a><span data-ttu-id="e3c9c-113">maxMeasurements: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e3c9c-113">maxMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e3c9c-114">작업을 실패 한 것으로 간주 하기 전에 수행할 수 있는 총 측정 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-114">Total number of measurements than can be taken before the operation is considered to have failed.</span></span>


### <a name="unwind--int"></a><span data-ttu-id="e3c9c-115">해제: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e3c9c-115">unwind : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e3c9c-116">일관성 확인에 실패할 경우 잊어버릴 결과의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-116">Number of results to forget when consistency checks fail.</span></span>


### <a name="oracle--continuousoracle"></a><span data-ttu-id="e3c9c-117">oracle: [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span><span class="sxs-lookup"><span data-stu-id="e3c9c-117">oracle : [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span></span>

<span data-ttu-id="e3c9c-118">\Ket{\phi} (t) \ket{\phi} = e ^ {i t \phi}\ket{\phi} $ for eigenstates $ $ (\mathbb{R} ^ + $에서 알 수 없는 단계 $ \emin) 인 단일 $U $를 나타내는 작업 $U입니다.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-118">An operation representing a unitary $U$ such that $U(t)\ket{\phi} = e^{i t \phi}\ket{\phi}$ for eigenstates $\ket{\phi}$ with unknown phase $\phi \in \mathbb{R}^+$.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="e3c9c-119">targetState: [[](xref:microsoft.quantum.lang-ref.qubit)]</span><span class="sxs-lookup"><span data-stu-id="e3c9c-119">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e3c9c-120">$U $가 작동 하는 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-120">A register that $U$ acts on.</span></span>



## <a name="output--double"></a><span data-ttu-id="e3c9c-121">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e3c9c-121">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e3c9c-122">최종 예상 $ \hat{\phi} \mathrel{: =} \은 (는) 허용 되는 모든 데이터를 제공 하는 사후에 대 한 기대를 예상 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-122">The final estimate $\hat{\phi} \mathrel{:=} \expect[\phi]$ , where the expectation is over the posterior given all accepted data.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3c9c-123">설명</span><span class="sxs-lookup"><span data-stu-id="e3c9c-123">Remarks</span></span>

### <a name="iterative-phase-estimation-and-eigenstates"></a><span data-ttu-id="e3c9c-124">반복 단계 예측 및 Eigenstates</span><span class="sxs-lookup"><span data-stu-id="e3c9c-124">Iterative Phase Estimation and Eigenstates</span></span>

<span data-ttu-id="e3c9c-125">일반적으로 입력 레지스터는 `eigenstate` $U $의 eigenstate $ \ket{\phi} $ 일 필요가 없지만 eigenstate에 superposition 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-125">In general, the input register `eigenstate` need not be an eigenstate $\ket{\phi}$ of $U$, but can be a superposition over eigenstates.</span></span> <span data-ttu-id="e3c9c-126">입력 상태가 \begin{align} \ket{\psi} & = \sum \_ {j} \sum \_ j \ket{\phi j}에서 제공 된다고 가정 합니다 \_ . 여기서 $ \{ \sum \_ j \} $는 $ \sum \_ j | \sum \_ j | ^ 2 = $1 및 where $U \ket{\phi \_ j} = \aj\ket \_ {\ l \_ j} $와 같이 복잡 한 계수입니다.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-126">Suppose that the input state is given by \begin{align} \ket{\psi} & = \sum\_{j} \alpha\_j \ket{\phi\_j}, \end{align} where $\{\alpha\_j\}$ are complex coefficients such that $\sum\_j |\alpha\_j|^2 = 1$ and where $U\ket{\phi\_j} = \phi\_j\ket{\phi\_j}$.</span></span>

<span data-ttu-id="e3c9c-127">그런 다음 [개발 가이드](xref:microsoft.quantum.libraries.characterization#iterative-phase-estimation-without-eigenstates)에 설명 된 대로 반복적인 단계 예측을 수행 하면 궁극적으로 단일 eigenstate로 수렴 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-127">Then, performing iterative phase estimation will eventually converge to a single eigenstate, as described in the [development guide](xref:microsoft.quantum.libraries.characterization#iterative-phase-estimation-without-eigenstates).</span></span>

### <a name="experiment-design"></a><span data-ttu-id="e3c9c-128">실험 디자인</span><span class="sxs-lookup"><span data-stu-id="e3c9c-128">Experiment Design</span></span>

<span data-ttu-id="e3c9c-129">에 전달 되는 $t $ 및 역 각도 $ \theta $의 측정 시간은 `oracle` *파티클 추측 추론*, \begin{align} \stc\\\ac\\\\variance{\phi}}., \aa\ca\a\a\ca\ca\ {1}</span><span class="sxs-lookup"><span data-stu-id="e3c9c-129">The measurement times $t$ and inversion angles $\theta$ passed to `oracle` are chosen according to the *particle guess heuristic*, \begin{align} \theta \sim \Pr(\phi),\quad t \approx \frac{1}{\variance{\phi}}.</span></span>
<span data-ttu-id="e3c9c-130">\end{align}이 추론은 이전의 표준에 대 한 가정 하에 반복 단계 추정에서 예상 되는 사후 분산을 줄이는 데 가장 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-130">\end{align} This heuristic is optimal for reducing the expected posterior variance in iterative phase estimation under the assumption of a normal prior.</span></span>

### <a name="optimality"></a><span data-ttu-id="e3c9c-131">Optimality</span><span class="sxs-lookup"><span data-stu-id="e3c9c-131">Optimality</span></span>

<span data-ttu-id="e3c9c-132">이 작업은 평가기 (\phi,) \mathrel{: =} (\a\hat{\phi}) ^ 2 $를 사용 $L 하 여 계산한 $ \\a$ 단계에 대 한 최적의 근사치를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-132">This operation approximates the optimal estimator for the phase $\phi$, as evaluated using the quadratic loss $L(\phi, \hat{\phi}) \mathrel{:=} (\phi - \hat{\phi})^2$.</span></span>

<span data-ttu-id="e3c9c-133">반복 단계 예측의 통계에 대 한 자세한 내용은 [Bayesian 단계 예측](xref:microsoft.quantum.libraries.characterization#bayesian-phase-estimation) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-133">See [Bayesian Phase Estimation](xref:microsoft.quantum.libraries.characterization#bayesian-phase-estimation) for more details on the statistics of iterative phase estimation.</span></span>

## <a name="references"></a><span data-ttu-id="e3c9c-134">참조</span><span class="sxs-lookup"><span data-stu-id="e3c9c-134">References</span></span>

- <span data-ttu-id="e3c9c-135">Ferrie *et al.* 2011 [doi: 10/tfx](https://doi.org/10.1007/s11128-012-0407-6), [arxiv: 1110.3067](https://arxiv.org/abs/1110.3067).</span><span class="sxs-lookup"><span data-stu-id="e3c9c-135">Ferrie *et al.* 2011 [doi:10/tfx](https://doi.org/10.1007/s11128-012-0407-6), [arXiv:1110.3067](https://arxiv.org/abs/1110.3067).</span></span>
- <span data-ttu-id="e3c9c-136">Wiebe *et al.* 2013 [doi: 10/tf3](https://doi.org/10.1103/PhysRevLett.112.190501), [arxiv: 1309.0876](https://arxiv.org/abs/1309.0876)</span><span class="sxs-lookup"><span data-stu-id="e3c9c-136">Wiebe *et al.* 2013 [doi:10/tf3](https://doi.org/10.1103/PhysRevLett.112.190501), [arXiv:1309.0876](https://arxiv.org/abs/1309.0876)</span></span>
- <span data-ttu-id="e3c9c-137">Wiebe 및 Granade 2018 *(준비)*.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-137">Wiebe and Granade 2018 *(in preparation)*.</span></span>