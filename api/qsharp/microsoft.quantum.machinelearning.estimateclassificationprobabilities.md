---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbabilities
title: EstimateClassificationProbabilities 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbabilities
qsharp.summary: Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.
ms.openlocfilehash: eea503d042d6ffc241186c117a7c02ee72983b09
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847715"
---
# <a name="estimateclassificationprobabilities-operation"></a><span data-ttu-id="95f53-102">EstimateClassificationProbabilities 작업</span><span class="sxs-lookup"><span data-stu-id="95f53-102">EstimateClassificationProbabilities operation</span></span>

<span data-ttu-id="95f53-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="95f53-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="95f53-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="95f53-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="95f53-105">샘플 집합과 순차 분류자가 지정 된 경우 각 샘플에서 분류자의 출력을 반복적으로 측정 하 여 해당 샘플에 대 한 분류 확률을 예측 합니다.</span><span class="sxs-lookup"><span data-stu-id="95f53-105">Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.</span></span>

```qsharp
operation EstimateClassificationProbabilities (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Double[][], nMeasurements : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="95f53-106">입력</span><span class="sxs-lookup"><span data-stu-id="95f53-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="95f53-107">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="95f53-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="95f53-108">샘플을 상태 준비 작업으로 인코딩할 수 있는 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="95f53-108">The tolerance to allow in encoding the sample into a state preparation operation.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="95f53-109">모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="95f53-109">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="95f53-110">지정 된 샘플에 대 한 분류 확률을 예측 하는 데 사용할 순차 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="95f53-110">The sequential model to be used to estimate the classification probabilities for the given samples.</span></span>


### <a name="samples--double"></a><span data-ttu-id="95f53-111">샘플: [Double](xref:microsoft.quantum.lang-ref.double)[] []</span><span class="sxs-lookup"><span data-stu-id="95f53-111">samples : [Double](xref:microsoft.quantum.lang-ref.double)[][]</span></span>

<span data-ttu-id="95f53-112">분류할 각 샘플에 대 한 기능 벡터의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="95f53-112">An array of feature vectors for each sample to be classified.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="95f53-113">n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="95f53-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="95f53-114">분류 확률을 예측 하는 데 사용할 측정 수입니다.</span><span class="sxs-lookup"><span data-stu-id="95f53-114">The number of measurements to use in estimating the classification probability.</span></span>



## <a name="output--double"></a><span data-ttu-id="95f53-115">Output: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="95f53-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="95f53-116">지정 된 각 샘플에 대 한 분류 확률의 예상 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="95f53-116">An array of estimates of the classification probability for each given sample.</span></span>