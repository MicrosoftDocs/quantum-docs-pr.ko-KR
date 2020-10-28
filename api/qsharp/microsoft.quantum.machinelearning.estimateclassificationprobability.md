---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbability
title: EstimateClassificationProbability 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbability
qsharp.summary: Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.
ms.openlocfilehash: 79e40bc4bc0954dc6742307122609950bf22ec71
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709773"
---
# <a name="estimateclassificationprobability-operation"></a><span data-ttu-id="b14d9-102">EstimateClassificationProbability 작업</span><span class="sxs-lookup"><span data-stu-id="b14d9-102">EstimateClassificationProbability operation</span></span>

<span data-ttu-id="b14d9-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="b14d9-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="b14d9-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b14d9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b14d9-105">샘플 및 순차 분류자가 지정 된 경우 지정 된 샘플에서 분류자의 출력을 반복적으로 측정 하 여 해당 샘플에 대 한 분류 확률을 예측 합니다.</span><span class="sxs-lookup"><span data-stu-id="b14d9-105">Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.</span></span>

```qsharp
operation EstimateClassificationProbability (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, sample : Double[], nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="b14d9-106">입력</span><span class="sxs-lookup"><span data-stu-id="b14d9-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="b14d9-107">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b14d9-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b14d9-108">샘플을 상태 준비 작업으로 인코딩할 수 있는 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="b14d9-108">The tolerance to allow in encoding the sample into a state preparation operation.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="b14d9-109">모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="b14d9-109">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="b14d9-110">지정 된 샘플의 분류 확률을 예측 하는 데 사용할 순차 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="b14d9-110">The sequential model to be used to estimate the classification probability for the given sample.</span></span>


### <a name="sample--double"></a><span data-ttu-id="b14d9-111">샘플: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="b14d9-111">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="b14d9-112">분류할 샘플의 기능 벡터입니다.</span><span class="sxs-lookup"><span data-stu-id="b14d9-112">The feature vector for the sample to be classified.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="b14d9-113">n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b14d9-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b14d9-114">분류 확률을 예측 하는 데 사용할 측정 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b14d9-114">The number of measurements to use in estimating the classification probability.</span></span>



## <a name="output--double"></a><span data-ttu-id="b14d9-115">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b14d9-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b14d9-116">지정 된 샘플에 대 한 예상 분류 확률입니다.</span><span class="sxs-lookup"><span data-stu-id="b14d9-116">An estimate of the classification probability for the given sample.</span></span>