---
uid: Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates
title: EstimateRealOverlapBetweenStates 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateRealOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the real part of the overlap between the states prepared by each operation.
ms.openlocfilehash: 01631bcbff2bff26ddc1db4e42d90ac4f8380bd4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714974"
---
# <a name="estimaterealoverlapbetweenstates-operation"></a><span data-ttu-id="86a69-102">EstimateRealOverlapBetweenStates 작업</span><span class="sxs-lookup"><span data-stu-id="86a69-102">EstimateRealOverlapBetweenStates operation</span></span>

<span data-ttu-id="86a69-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="86a69-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="86a69-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="86a69-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="86a69-105">각각 상태의 복사본을 준비 하는 두 개의 작업이 지정 된 경우 각 작업에서 준비 된 상태 간에 겹치는 부분을 예상 합니다.</span><span class="sxs-lookup"><span data-stu-id="86a69-105">Given two operations which each prepare copies of a state, estimates the real part of the overlap between the states prepared by each operation.</span></span>

```qsharp
operation EstimateRealOverlapBetweenStates (commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="86a69-106">입력</span><span class="sxs-lookup"><span data-stu-id="86a69-106">Input</span></span>

### <a name="commonpreparation--qubit--unit-adj"></a><span data-ttu-id="86a69-107">commonPreparation: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="86a69-107">commonPreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="86a69-108">고정 된 입력 상태를 준비 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="86a69-108">An operation that prepares a fixed input state.</span></span>


### <a name="preparation1--qubit--unit-adj--ctl"></a><span data-ttu-id="86a69-109">preparation1: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="86a69-109">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="86a69-110">비교할 두 개의 상태 준비 작업 중 첫 번째 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="86a69-110">The first of the two state preparation operations to be compared.</span></span>


### <a name="preparation2--qubit--unit-adj--ctl"></a><span data-ttu-id="86a69-111">preparation2: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="86a69-111">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="86a69-112">비교할 두 개의 상태 준비 작업 중 두 번째입니다.</span><span class="sxs-lookup"><span data-stu-id="86a69-112">The second of the two state preparation operations to be compared.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="86a69-113">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="86a69-113">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="86a69-114">`commonPreparation`, `preparation1` 및가 모두 작동 하는 데 사용할 수 있는 값입니다 `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="86a69-114">The number of qubits on which `commonPreparation`, `preparation1`, and `preparation2` all act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="86a69-115">n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="86a69-115">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="86a69-116">겹치기를 추정 하는 데 사용할 측정 수입니다.</span><span class="sxs-lookup"><span data-stu-id="86a69-116">The number of measurements to use in estimating the overlap.</span></span>



## <a name="output--double"></a><span data-ttu-id="86a69-117">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="86a69-117">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="86a69-118">설명</span><span class="sxs-lookup"><span data-stu-id="86a69-118">Remarks</span></span>

<span data-ttu-id="86a69-119">이 작업은 Hadamard 테스트를 사용 하 여 $ $ \begin{align} \braket{\psi |의 실제 부분을 찾습니다. V ^ {\dagger} U | \psi} \end{align} $ $ where $ \ket{\psi} $는에 의해 준비 된 상태이 `commonPreparation` 고, $U $은의 동작에 대 한 단일 표현 `preparation1` 이며, $V $은에 해당 `preparation2` 합니다.</span><span class="sxs-lookup"><span data-stu-id="86a69-119">This operation uses the Hadamard test to find the real part of $$ \begin{align} \braket{\psi | V^{\dagger} U | \psi} \end{align} $$ where $\ket{\psi}$ is the state prepared by `commonPreparation`, $U$ is the unitary representation of the action of `preparation1`, and where $V$ corresponds to `preparation2`.</span></span>

## <a name="references"></a><span data-ttu-id="86a69-120">참조</span><span class="sxs-lookup"><span data-stu-id="86a69-120">References</span></span>

- <span data-ttu-id="86a69-121">Aharonov *et al.* [/0511096](https://arxiv.org/abs/quant-ph/0511096)입니다.</span><span class="sxs-lookup"><span data-stu-id="86a69-121">Aharonov *et al.* [quant-ph/0511096](https://arxiv.org/abs/quant-ph/0511096).</span></span>

## <a name="see-also"></a><span data-ttu-id="86a69-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="86a69-122">See Also</span></span>

- [<span data-ttu-id="86a69-123">EstimateImagOverlapBetweenStates.</span><span class="sxs-lookup"><span data-stu-id="86a69-123">Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)
- [<span data-ttu-id="86a69-124">EstimateOverlapBetweenStates.</span><span class="sxs-lookup"><span data-stu-id="86a69-124">Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates)