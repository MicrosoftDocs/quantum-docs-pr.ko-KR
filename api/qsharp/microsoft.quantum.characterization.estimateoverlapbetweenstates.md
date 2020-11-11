---
uid: Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates
title: EstimateOverlapBetweenStates 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the squared overlap between the states prepared by each operation.
ms.openlocfilehash: 58a367c7ff7d13ac5c1eb1588fb8dac66414776c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714995"
---
# <a name="estimateoverlapbetweenstates-operation"></a><span data-ttu-id="4c3ab-102">EstimateOverlapBetweenStates 작업</span><span class="sxs-lookup"><span data-stu-id="4c3ab-102">EstimateOverlapBetweenStates operation</span></span>

<span data-ttu-id="4c3ab-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="4c3ab-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="4c3ab-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4c3ab-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4c3ab-105">각각 상태의 복사본을 준비 하는 두 개의 작업이 지정 된 경우 각 작업에 의해 준비 된 상태 사이에서 제곱이 중복 되는 것을 추정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c3ab-105">Given two operations which each prepare copies of a state, estimates the squared overlap between the states prepared by each operation.</span></span>

```qsharp
operation EstimateOverlapBetweenStates (preparation1 : (Qubit[] => Unit is Adj), preparation2 : (Qubit[] => Unit is Adj), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="4c3ab-106">입력</span><span class="sxs-lookup"><span data-stu-id="4c3ab-106">Input</span></span>

### <a name="preparation1--qubit--unit-adj"></a><span data-ttu-id="4c3ab-107">preparation1: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4c3ab-107">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="4c3ab-108">비교할 두 개의 상태 준비 작업 중 첫 번째 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="4c3ab-108">The first of the two state preparation operations to be compared.</span></span>


### <a name="preparation2--qubit--unit-adj"></a><span data-ttu-id="4c3ab-109">preparation2: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4c3ab-109">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="4c3ab-110">비교할 두 개의 상태 준비 작업 중 두 번째입니다.</span><span class="sxs-lookup"><span data-stu-id="4c3ab-110">The second of the two state preparation operations to be compared.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="4c3ab-111">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4c3ab-111">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4c3ab-112">`commonPreparation`, `preparation1` 및가 모두 작동 하는 데 사용할 수 있는 값입니다 `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="4c3ab-112">The number of qubits on which `commonPreparation`, `preparation1`, and `preparation2` all act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="4c3ab-113">n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4c3ab-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4c3ab-114">겹치기를 추정 하는 데 사용할 측정 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4c3ab-114">The number of measurements to use in estimating the overlap.</span></span>



## <a name="output--double"></a><span data-ttu-id="4c3ab-115">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4c3ab-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="4c3ab-116">설명</span><span class="sxs-lookup"><span data-stu-id="4c3ab-116">Remarks</span></span>

<span data-ttu-id="4c3ab-117">이 작업은 교환 테스트를 사용 하 여 $ $ \begin{align} \left |를 찾습니다. \braket{00\cdots 0 | V ^ {\dagger} U | 00 \ cdots 0} \right | ^ 2 \end{align} $ $ 여기서 $U $은의 동작에 대 한 단일 표현 `preparation1` 이며 $V $는에 해당 `preparation2` 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c3ab-117">This operation uses the SWAP test to find $$ \begin{align} \left| \braket{00\cdots 0 | V^{\dagger} U | 00\cdots 0} \right|^2 \end{align} $$ where $U$ is the unitary representation of the action of `preparation1`, and where $V$ corresponds to `preparation2`.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c3ab-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4c3ab-118">See Also</span></span>

- [<span data-ttu-id="4c3ab-119">EstimateRealOverlapBetweenStates.</span><span class="sxs-lookup"><span data-stu-id="4c3ab-119">Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates)
- [<span data-ttu-id="4c3ab-120">EstimateImagOverlapBetweenStates.</span><span class="sxs-lookup"><span data-stu-id="4c3ab-120">Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)