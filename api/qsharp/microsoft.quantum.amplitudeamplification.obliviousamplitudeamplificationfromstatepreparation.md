---
uid: Microsoft.Quantum.AmplitudeAmplification.ObliviousAmplitudeAmplificationFromStatePreparation
title: ObliviousAmplitudeAmplificationFromStatePreparation 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ObliviousAmplitudeAmplificationFromStatePreparation
qsharp.summary: Oblivious amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 9975d26af8f9beb2b91e409ad78159d6f04936e3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721831"
---
# <a name="obliviousamplitudeamplificationfromstatepreparation-function"></a><span data-ttu-id="ffcf2-102">ObliviousAmplitudeAmplificationFromStatePreparation 함수</span><span class="sxs-lookup"><span data-stu-id="ffcf2-102">ObliviousAmplitudeAmplificationFromStatePreparation function</span></span>

<span data-ttu-id="ffcf2-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="ffcf2-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="ffcf2-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ffcf2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ffcf2-105">부분 반사에 대해 oracles 명확한 진폭 증폭</span><span class="sxs-lookup"><span data-stu-id="ffcf2-105">Oblivious amplitude amplification by oracles for partial reflections.</span></span>

```qsharp
function ObliviousAmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, idxFlagQubit : Int) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="ffcf2-106">입력</span><span class="sxs-lookup"><span data-stu-id="ffcf2-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="ffcf2-107">단계: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="ffcf2-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="ffcf2-108">부분 반사의 단계</span><span class="sxs-lookup"><span data-stu-id="ffcf2-108">Phases of partial reflections</span></span>


### <a name="startstateoracle--deterministicstateoracle"></a><span data-ttu-id="ffcf2-109">startStateOracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="ffcf2-109">startStateOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="ffcf2-110">보조 시작 상태를 준비 하는 단일 oracle $A $</span><span class="sxs-lookup"><span data-stu-id="ffcf2-110">Unitary oracle $A$ that prepares auxiliary start state</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="ffcf2-111">signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="ffcf2-111">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="ffcf2-112">`ObliviousOracle`보조 및 시스템 레지스터에 공동으로 작동 하는 형식의 단일 oracle $O $</span><span class="sxs-lookup"><span data-stu-id="ffcf2-112">Unitary oracle $O$ of type `ObliviousOracle` that acts jointly on the auxiliary and system register</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="ffcf2-113">Idx플래그 [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ffcf2-113">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ffcf2-114">단일 수준 비트 플래그 레지스터의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-114">Index to single-qubit flag register</span></span>



## <a name="output--qubitqubit--unit-adj--ctl"></a><span data-ttu-id="ffcf2-115">출력: (Adj[[]](xref:microsoft.quantum.lang-ref.qubit)[, []](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="ffcf2-115">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="ffcf2-116">부분 반사를 기준으로 명확한 진폭 증폭을 구현 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-116">An operation that implements oblivious amplitude amplification based on partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffcf2-117">설명</span><span class="sxs-lookup"><span data-stu-id="ffcf2-117">Remarks</span></span>

<span data-ttu-id="ffcf2-118">이로 인해의 보조 시작 및 대상 상태 형식에 보다 엄격한 조건이 부과 `AmpAmpObliviousByReflectionPhases` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-118">This imposes stricter conditions on form of the auxiliary start and target states than in `AmpAmpObliviousByReflectionPhases`.</span></span>
<span data-ttu-id="ffcf2-119">$A \ket {0} \_ f\ket {0} \_ A = \ket{\text{start}} \_ {fa} $는 \_ 계산 기준 $ \ket f\ket $에서 보조 시작 상태 $ \ket{\text{start}} {fa} $를 준비 {0} \_ {0} 하는 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-119">It is assumed that $A\ket{0}\_f\ket{0}\_a= \ket{\text{start}}\_{fa}$ prepares the auxiliary start state $\ket{\text{start}}\_{fa}$ from the computational basis $\ket{0}\_f\ket{0}$.</span></span>
<span data-ttu-id="ffcf2-120">대상 상태가 $ \ket f $로 표시 되어 있다고 가정 합니다 {1} \_ .</span><span class="sxs-lookup"><span data-stu-id="ffcf2-120">It is assumed that the target state is marked by $\ket{1}\_f$.</span></span>
<span data-ttu-id="ffcf2-121">\Begin{align} O\ket {\ text {start}} \_ {fa} \ket{\psi} \_ s = \lambda\ket {1} \_ f\ket {\ text {모든}} \_ a\ket {\ text {target}} \_ s U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots,에 대 한 일부 단일 $U $로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-121">It is assumed that \begin{align} O\ket{\text{start}}\_{fa}\ket{\psi}\_s= \lambda\ket{1}\_f\ket{\text{anything}}\_a\ket{\text{target}}\_s U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} for some unitary $U$.</span></span>