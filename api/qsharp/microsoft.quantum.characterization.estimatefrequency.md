---
uid: Microsoft.Quantum.Characterization.EstimateFrequency
title: EstimateFrequency 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequency
qsharp.summary: Given a preparation and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: 30b21a8e86eb5a4dd8dd8207dbdc6a0970308319
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216254"
---
# <a name="estimatefrequency-operation"></a><span data-ttu-id="82df1-102">EstimateFrequency 작업</span><span class="sxs-lookup"><span data-stu-id="82df1-102">EstimateFrequency operation</span></span>

<span data-ttu-id="82df1-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="82df1-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="82df1-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="82df1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="82df1-105">준비 및 측정을 고려 하 여 `Zero` 지정 된 수의 평가판을 수행 하 여 측정값이 성공 (반환) 하는 빈도를 추정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82df1-105">Given a preparation and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.</span></span>

```qsharp
operation EstimateFrequency (preparation : (Qubit[] => Unit), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="82df1-106">입력</span><span class="sxs-lookup"><span data-stu-id="82df1-106">Input</span></span>

### <a name="preparation--qubit--unit"></a><span data-ttu-id="82df1-107">준비: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="82df1-107">preparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="82df1-108">지정 된 상태 $ \rho $를 해당 입력 레지스터에 준비 하는 작업을 $ $P 합니다.</span><span class="sxs-lookup"><span data-stu-id="82df1-108">An operation $P$ that prepares a given state $\rho$ on its input register.</span></span>


### <a name="measurement--qubit--__invalidresult__"></a><span data-ttu-id="82df1-109">측정: [값](xref:microsoft.quantum.lang-ref.qubit)이 __잘못 <Result> 된__></span><span class="sxs-lookup"><span data-stu-id="82df1-109">measurement : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __invalid<Result>__</span></span> 

<span data-ttu-id="82df1-110">작업 $M $는 관심 측정을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="82df1-110">An operation $M$ representing the measurement of interest.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="82df1-111">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="82df1-111">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="82df1-112">각 작업의 준비 및 측정값이 작동 하는 데 사용할 수 있는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="82df1-112">The number of qubits on which the preparation and measurement each act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="82df1-113">n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="82df1-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="82df1-114">관련 빈도를 예측 하기 위해 측정이 수행 되어야 하는 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="82df1-114">The number of times that the measurement should be performed in order to estimate the frequency of interest.</span></span>



## <a name="output--double"></a><span data-ttu-id="82df1-115">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="82df1-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="82df1-116">$M (P (\ket{00 \cdots 0} \bra{00 \cdots 0})) $가 반환 되 `Zero` 고, 비편향 이항 평가기 $ \hat{p} = n {\uparrow}/n {\text{measurements}} $를 사용 하 여 얻은 빈도의 예상 $ \hat{p} $ \_ \_ \_ 입니다. 여기서 $n {\uparrow} $은 관찰 된 결과의 수입니다 `Zero` .</span><span class="sxs-lookup"><span data-stu-id="82df1-116">An estimate $\hat{p}$ of the frequency with which $M(P(\ket{00 \cdots 0}\bra{00 \cdots 0}))$ returns `Zero`, obtained using the unbiased binomial estimator $\hat{p} = n\_{\uparrow} / n\_{\text{measurements}}$, where $n\_{\uparrow}$ is the number of `Zero` results observed.</span></span>

<span data-ttu-id="82df1-117">이는 확률을 측정할 수 없다는 점에서 물리적인 제한을 적용 하는 대상 컴퓨터에서 특히 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="82df1-117">This is particularly important on target machines which respect physical limitations, such that probabilities cannot be measured.</span></span>