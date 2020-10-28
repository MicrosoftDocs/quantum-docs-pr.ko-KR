---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbabilities
title: EstimateClassificationProbabilities 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbabilities
qsharp.summary: Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.
ms.openlocfilehash: 2b7845d39256f718cc3e415207b8a47b24620bdb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709787"
---
# <a name="estimateclassificationprobabilities-operation"></a><span data-ttu-id="b8fb3-102">EstimateClassificationProbabilities 작업</span><span class="sxs-lookup"><span data-stu-id="b8fb3-102">EstimateClassificationProbabilities operation</span></span>

<span data-ttu-id="b8fb3-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="b8fb3-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="b8fb3-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b8fb3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b8fb3-105">샘플 집합과 순차 분류자가 지정 된 경우 각 샘플에서 분류자의 출력을 반복적으로 측정 하 여 해당 샘플에 대 한 분류 확률을 예측 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8fb3-105">Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.</span></span>

```qsharp
operation EstimateClassificationProbabilities (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Double[][], nMeasurements : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="b8fb3-106">입력</span><span class="sxs-lookup"><span data-stu-id="b8fb3-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="b8fb3-107">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b8fb3-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b8fb3-108">샘플을 상태 준비 작업으로 인코딩할 수 있는 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="b8fb3-108">The tolerance to allow in encoding the sample into a state preparation operation.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="b8fb3-109">모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="b8fb3-109">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="b8fb3-110">지정 된 샘플에 대 한 분류 확률을 예측 하는 데 사용할 순차 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="b8fb3-110">The sequential model to be used to estimate the classification probabilities for the given samples.</span></span>


### <a name="samples--double"></a><span data-ttu-id="b8fb3-111">샘플: [Double](xref:microsoft.quantum.lang-ref.double)[] []</span><span class="sxs-lookup"><span data-stu-id="b8fb3-111">samples : [Double](xref:microsoft.quantum.lang-ref.double)[][]</span></span>

<span data-ttu-id="b8fb3-112">분류할 각 샘플에 대 한 기능 벡터의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="b8fb3-112">An array of feature vectors for each sample to be classified.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="b8fb3-113">n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b8fb3-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b8fb3-114">분류 확률을 예측 하는 데 사용할 측정 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b8fb3-114">The number of measurements to use in estimating the classification probability.</span></span>



## <a name="output--double"></a><span data-ttu-id="b8fb3-115">Output: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="b8fb3-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="b8fb3-116">지정 된 각 샘플에 대 한 분류 확률의 예상 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="b8fb3-116">An array of estimates of the classification probability for each given sample.</span></span>