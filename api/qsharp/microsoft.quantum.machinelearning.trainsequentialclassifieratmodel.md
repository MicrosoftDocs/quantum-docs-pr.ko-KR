---
uid: Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel
title: TrainSequentialClassifierAtModel 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainSequentialClassifierAtModel
qsharp.summary: Given the structure of a sequential classifier, trains the classifier on a given labeled training set, starting from a particular model.
ms.openlocfilehash: b9e30e4e5bc23f56d9119083045967caff28f13a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720457"
---
# <a name="trainsequentialclassifieratmodel-operation"></a><span data-ttu-id="6e213-102">TrainSequentialClassifierAtModel 작업</span><span class="sxs-lookup"><span data-stu-id="6e213-102">TrainSequentialClassifierAtModel operation</span></span>

<span data-ttu-id="6e213-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="6e213-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="6e213-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6e213-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6e213-105">순차 분류자의 구조가 지정 된 경우 특정 모델에서 시작 하 여 지정 된 레이블이 지정 된 학습 집합에 분류자를 학습 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e213-105">Given the structure of a sequential classifier, trains the classifier on a given labeled training set, starting from a particular model.</span></span>

```qsharp
operation TrainSequentialClassifierAtModel (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, trainingSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : (Microsoft.Quantum.MachineLearning.SequentialModel, Int)
```


## <a name="input"></a><span data-ttu-id="6e213-106">입력</span><span class="sxs-lookup"><span data-stu-id="6e213-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="6e213-107">모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="6e213-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="6e213-108">학습을 위한 시작 지점으로 사용할 순차 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="6e213-108">The sequential model to be used as a starting point for training.</span></span>


### <a name="samples--labeledsample"></a><span data-ttu-id="6e213-109">샘플: [Labeledsample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span><span class="sxs-lookup"><span data-stu-id="6e213-109">samples : [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span></span>

<span data-ttu-id="6e213-110">학습을 수행 하는 데 사용 되는 레이블이 지정 된 학습 데이터의 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="6e213-110">A set of labeled training data that will be used to perform training.</span></span>


### <a name="options--trainingoptions"></a><span data-ttu-id="6e213-111">옵션: [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="6e213-111">options : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>

<span data-ttu-id="6e213-112">학습 시 사용할 구성 @"microsoft.quantum.machinelearning.trainingoptions" 자세한 내용은 및 @"microsoft.quantum.machinelearning.defaulttrainingoptions" 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e213-112">Configuration to be used when training; see @"microsoft.quantum.machinelearning.trainingoptions" and @"microsoft.quantum.machinelearning.defaulttrainingoptions" for more details.</span></span>


### <a name="trainingschedule--samplingschedule"></a><span data-ttu-id="6e213-113">trainingSchedule: [Samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="6e213-113">trainingSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="6e213-114">학습 단계 중 학습 데이터에서 샘플을 선택할 때 사용할 샘플링 일정입니다.</span><span class="sxs-lookup"><span data-stu-id="6e213-114">A sampling schedule to use when selecting samples from the training data during training steps.</span></span>


### <a name="validationschedule--samplingschedule"></a><span data-ttu-id="6e213-115">validationSchedule: [Samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="6e213-115">validationSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="6e213-116">최상의 분류자 점수를 발생 시킨 시작점을 선택할 때 학습 데이터에서 샘플을 선택 하는 경우 사용할 샘플링 일정입니다.</span><span class="sxs-lookup"><span data-stu-id="6e213-116">A sampling schedule to use when selecting samples from the training data when selecting which start point resulted in the best classifier score.</span></span>



## <a name="output--sequentialmodelint"></a><span data-ttu-id="6e213-117">출력: ([SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[Int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="6e213-117">Output : ([SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

- <span data-ttu-id="6e213-118">지정 된 분류자의 매개 변수화 및 두 클래스 간의 바이어스는 각각의 지정 된 시작점에서 최상의 결과에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e213-118">A parameterization of the given classifier and a bias between the two classes, together corresponding to the best result from each of the given start points.</span></span>
- <span data-ttu-id="6e213-119">최상의 분류자 모델에서 관찰 된 누락 수입니다.</span><span class="sxs-lookup"><span data-stu-id="6e213-119">The number of misses observed at the best classifier model.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e213-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6e213-120">See Also</span></span>

- [<span data-ttu-id="6e213-121">MachineLearning. TrainSequentialClassifier</span><span class="sxs-lookup"><span data-stu-id="6e213-121">Microsoft.Quantum.MachineLearning.TrainSequentialClassifier</span></span>](xref:Microsoft.Quantum.MachineLearning.TrainSequentialClassifier)
- [<span data-ttu-id="6e213-122">MachineLearning. ValidateSequentialClassifier</span><span class="sxs-lookup"><span data-stu-id="6e213-122">Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier</span></span>](xref:Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier)