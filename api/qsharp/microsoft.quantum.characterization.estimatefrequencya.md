---
uid: Microsoft.Quantum.Characterization.EstimateFrequencyA
title: EstimateFrequencyA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequencyA
qsharp.summary: Given a preparation that is adjointable and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: 88f0a237975c158bffcc015f79d2134b210ce83b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715065"
---
# <a name="estimatefrequencya-operation"></a><span data-ttu-id="783b2-102">EstimateFrequencyA 작업</span><span class="sxs-lookup"><span data-stu-id="783b2-102">EstimateFrequencyA operation</span></span>

<span data-ttu-id="783b2-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="783b2-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="783b2-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="783b2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="783b2-105">Adjointable 및 측정 준비를 고려 하 여 지정 된 수의 평가판을 수행 하 여 측정값이 성공 (반환) 하는 빈도를 추정 `Zero` 합니다.</span><span class="sxs-lookup"><span data-stu-id="783b2-105">Given a preparation that is adjointable and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.</span></span>

```qsharp
operation EstimateFrequencyA (preparation : (Qubit[] => Unit is Adj), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="783b2-106">입력</span><span class="sxs-lookup"><span data-stu-id="783b2-106">Input</span></span>

### <a name="preparation--qubit--unit-adj"></a><span data-ttu-id="783b2-107">준비:가 중 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="783b2-107">preparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="783b2-108">Adjointable 작업은 지정 된 상태 $ \rho $를 입력 레지스터에서 준비 하는 $ $P 합니다.</span><span class="sxs-lookup"><span data-stu-id="783b2-108">An adjointable operation $P$ that prepares a given state $\rho$ on its input register.</span></span>


### <a name="measurement--qubit--__invalidresult__"></a><span data-ttu-id="783b2-109">측정: [값](xref:microsoft.quantum.lang-ref.qubit)이 __잘못 <Result> 된__ ></span><span class="sxs-lookup"><span data-stu-id="783b2-109">measurement : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __invalid<Result>__</span></span> 

<span data-ttu-id="783b2-110">작업 $M $는 관심 측정을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="783b2-110">An operation $M$ representing the measurement of interest.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="783b2-111">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="783b2-111">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="783b2-112">각 작업의 준비 및 측정값이 작동 하는 데 사용할 수 있는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="783b2-112">The number of qubits on which the preparation and measurement each act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="783b2-113">n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="783b2-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="783b2-114">관련 빈도를 예측 하기 위해 측정이 수행 되어야 하는 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="783b2-114">The number of times that the measurement should be performed in order to estimate the frequency of interest.</span></span>



## <a name="output--double"></a><span data-ttu-id="783b2-115">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="783b2-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="783b2-116">$M (P (\ket{00 \cdots 0} \bra{00 \cdots 0})) $가 반환 되 `Zero` 고, 비편향 이항 평가기 $ \hat{p} = n {\uparrow}/n {\text{measurements}} $를 사용 하 여 얻은 빈도의 예상 $ \hat{p} $ \_ \_ \_ 입니다. 여기서 $n {\uparrow} $은 관찰 된 결과의 수입니다 `Zero` .</span><span class="sxs-lookup"><span data-stu-id="783b2-116">An estimate $\hat{p}$ of the frequency with which $M(P(\ket{00 \cdots 0}\bra{00 \cdots 0}))$ returns `Zero`, obtained using the unbiased binomial estimator $\hat{p} = n\_{\uparrow} / n\_{\text{measurements}}$, where $n\_{\uparrow}$ is the number of `Zero` results observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="783b2-117">설명</span><span class="sxs-lookup"><span data-stu-id="783b2-117">Remarks</span></span>

<span data-ttu-id="783b2-118">Adjointable 작업의 경우 작업을 호출 하는 것과 같은 특정 가정을 수행할 수 있습니다 .이 경우 대상 컴퓨터에서 성능 최적화를 수행할 수 있도록 하는 작업을 정확히 동일한 상태로 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="783b2-118">For adjointable operations, certain assumptions can be made such like calling the operation will prepare the qubits to exactly the same state, which allow target machines to make some performance optimizations.</span></span>