---
uid: Microsoft.Quantum.MachineLearning._RunSingleTrainingEpoch
title: _RunSingleTrainingEpoch 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: _RunSingleTrainingEpoch
qsharp.summary: Perform one epoch of sequential classifier training on a subset of data samples.
ms.openlocfilehash: 2b4f629eac0bd8e60bd4d86077521c60085d4809
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720632"
---
# <a name="_runsingletrainingepoch-operation"></a><span data-ttu-id="db8e5-102">_RunSingleTrainingEpoch 작업</span><span class="sxs-lookup"><span data-stu-id="db8e5-102">_RunSingleTrainingEpoch operation</span></span>

<span data-ttu-id="db8e5-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="db8e5-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="db8e5-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="db8e5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="db8e5-105">데이터 샘플의 하위 집합에 대 한 순차 분류자 교육의 한 epoch를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="db8e5-105">Perform one epoch of sequential classifier training on a subset of data samples.</span></span>

```qsharp
operation _RunSingleTrainingEpoch (encodedSamples : (Microsoft.Quantum.MachineLearning.LabeledSample, Microsoft.Quantum.MachineLearning.StateGenerator)[], schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, periodScore : Int, options : Microsoft.Quantum.MachineLearning.TrainingOptions, model : Microsoft.Quantum.MachineLearning.SequentialModel, nPreviousBestMisses : Int) : (Int, Microsoft.Quantum.MachineLearning.SequentialModel)
```


## <a name="input"></a><span data-ttu-id="db8e5-106">입력</span><span class="sxs-lookup"><span data-stu-id="db8e5-106">Input</span></span>

### <a name="encodedsamples--labeledsamplestategenerator"></a><span data-ttu-id="db8e5-107">encodedSamples: ([Labeledsample](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)) []</span><span class="sxs-lookup"><span data-stu-id="db8e5-107">encodedSamples : ([LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator))[]</span></span>




### <a name="schedule--samplingschedule"></a><span data-ttu-id="db8e5-108">일정: [Samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="db8e5-108">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>




### <a name="periodscore--int"></a><span data-ttu-id="db8e5-109">periodScore: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="db8e5-109">periodScore : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="db8e5-110">점수 매기기 점수 사이에 수행할 그라데이션 단계 수입니다.</span><span class="sxs-lookup"><span data-stu-id="db8e5-110">The number of gradient steps to be taken between scoring points.</span></span>
<span data-ttu-id="db8e5-111">최상의 정확도를 위해를 1로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db8e5-111">For best accuracy, set to 1.</span></span>


### <a name="options--trainingoptions"></a><span data-ttu-id="db8e5-112">옵션: [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="db8e5-112">options : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>

<span data-ttu-id="db8e5-113">학습에 사용 되는 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="db8e5-113">Options to be used in training.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="db8e5-114">모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="db8e5-114">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="db8e5-115">학습할 순차 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="db8e5-115">The sequential model to be trained.</span></span>


### <a name="npreviousbestmisses--int"></a><span data-ttu-id="db8e5-116">nPreviousBestMisses: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="db8e5-116">nPreviousBestMisses : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="db8e5-117">이전 epoch에서 관찰 되는 가장 좋은 오 분류 수입니다.</span><span class="sxs-lookup"><span data-stu-id="db8e5-117">The best number of misclassifications observed in previous epochs.</span></span>



## <a name="output--intsequentialmodel"></a><span data-ttu-id="db8e5-118">Output: ([Int](xref:microsoft.quantum.lang-ref.int),[SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel))</span><span class="sxs-lookup"><span data-stu-id="db8e5-118">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel))</span></span>

- <span data-ttu-id="db8e5-119">이 epoch로 관찰 된 최소 분류 수입니다.</span><span class="sxs-lookup"><span data-stu-id="db8e5-119">The smallest number of misclassifications observed through to this epoch.</span></span>
- <span data-ttu-id="db8e5-120">가장 적합 한 새 순차 모델을 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="db8e5-120">The new best sequential model found.</span></span>