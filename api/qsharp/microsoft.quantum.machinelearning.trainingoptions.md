---
uid: Microsoft.Quantum.MachineLearning.TrainingOptions
title: TrainingOptions 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainingOptions
qsharp.summary: A collection of options to be used in training quantum classifiers.
ms.openlocfilehash: 5ecc2b5175a4e8db78f72311ac1d5ff964bae811
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722377"
---
# <a name="trainingoptions-user-defined-type"></a><span data-ttu-id="d4539-102">TrainingOptions 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="d4539-102">TrainingOptions user defined type</span></span>

<span data-ttu-id="d4539-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d4539-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="d4539-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d4539-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d4539-105">퀀텀 분류자 학습에 사용할 옵션의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="d4539-105">A collection of options to be used in training quantum classifiers.</span></span>

```qsharp

newtype TrainingOptions = (LearningRate : Double, Tolerance : Double, MinibatchSize : Int, NMeasurements : Int, MaxEpochs : Int, MaxStalls : Int, StochasticRescaleFactor : Double, ScoringPeriod : Int, VerboseMessage : (String -> Unit));
```



## <a name="named-items"></a><span data-ttu-id="d4539-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="d4539-106">Named Items</span></span>

### <a name="learningrate--double"></a><span data-ttu-id="d4539-107">LearningRate: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d4539-107">LearningRate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d4539-108">학습 단계에서 모델 매개 변수를 업데이트할 때 그라데이션을 재조정 하는 학습 률입니다.</span><span class="sxs-lookup"><span data-stu-id="d4539-108">The learning rate by which gradients should be rescaled when updating model parameters during training steps.</span></span>
### <a name="tolerance--double"></a><span data-ttu-id="d4539-109">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d4539-109">Tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d4539-110">샘플을 퀀텀 상태로 준비할 때 사용할 근사 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="d4539-110">The approximation tolerance to use when preparing samples as quantum states.</span></span>
### <a name="minibatchsize--int"></a><span data-ttu-id="d4539-111">미니 Batchsize: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d4539-111">MinibatchSize : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d4539-112">각 학습 미니 배치에서 사용할 샘플의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d4539-112">The number of samples to use in each training minibatch.</span></span>
### <a name="nmeasurements--int"></a><span data-ttu-id="d4539-113">N 측정값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d4539-113">NMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d4539-114">분류 확률을 예측 하기 위해 각 분류 결과를 측정 하는 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="d4539-114">The number of times to measure each classification result in order to estimate the classification probability.</span></span>
### <a name="maxepochs--int"></a><span data-ttu-id="d4539-115">MaxEpochs: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d4539-115">MaxEpochs : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d4539-116">각 모델을 학습 하는 최대 epoch 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d4539-116">The maximum number of epochs to train each model for.</span></span>
### <a name="maxstalls--int"></a><span data-ttu-id="d4539-117">MaxStalls: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d4539-117">MaxStalls : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d4539-118">학습 epoch가 실패 하기 전까지 정지 (약 0 그라데이션) 할 수 있는 최대 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="d4539-118">The maximum number of times a training epoch is allowed to stall (approximately zero gradient) before failing.</span></span>
### <a name="stochasticrescalefactor--double"></a><span data-ttu-id="d4539-119">StochasticRescaleFactor: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d4539-119">StochasticRescaleFactor : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d4539-120">업데이트를 다시 시도 하기 전에 지연 된 모델의 크기를 조정 하는 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="d4539-120">The amount to rescale stalled models by before retrying an update.</span></span>
### <a name="scoringperiod--int"></a><span data-ttu-id="d4539-121">ScoringPeriod: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d4539-121">ScoringPeriod : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d4539-122">점수 매기기 점수 사이에 수행할 그라데이션 단계 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d4539-122">The number of gradient steps to be taken between scoring points.</span></span>
<span data-ttu-id="d4539-123">최상의 정확도를 위해를 1로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4539-123">For best accuracy, set to 1.</span></span>
### <a name="verbosemessage--string---unit"></a><span data-ttu-id="d4539-124">VerboseMessage: [문자열](xref:microsoft.quantum.lang-ref.string) -> [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d4539-124">VerboseMessage : [String](xref:microsoft.quantum.lang-ref.string) -> [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="d4539-125">자세한 피드백을 제공 하는 데 사용할 수 있는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="d4539-125">A function that can be used to provide verbose feedback.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4539-126">설명</span><span class="sxs-lookup"><span data-stu-id="d4539-126">Remarks</span></span>

<span data-ttu-id="d4539-127">이 UDT는 직접 만들 수 없습니다. 대신를 호출 하 @"microsoft.quantum.machinelearning.defaulttrainingoptions" 고 연산자를 사용 하 여 다른 기본값을 재정의 하 여 지정 해야 합니다 `w/` .</span><span class="sxs-lookup"><span data-stu-id="d4539-127">This UDT should not be created directly, but rather should be specified by calling @"microsoft.quantum.machinelearning.defaulttrainingoptions" and then using the `w/` operator to override different defaults.</span></span>

<span data-ttu-id="d4539-128">예를 들어 10만 측정치와 최대 8 교육 epoch를 사용 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4539-128">For example, to use 100,000 measurements and at most 8 training epochs:</span></span>

```Q#
let options = DefaultTrainingOptions()
              w/ NMeasurements <- 100000
              w/ MaxEpochs <- 8;
```

## <a name="references"></a><span data-ttu-id="d4539-129">참조</span><span class="sxs-lookup"><span data-stu-id="d4539-129">References</span></span>

- [<span data-ttu-id="d4539-130">arXiv: 1804.00633</span><span class="sxs-lookup"><span data-stu-id="d4539-130">arXiv:1804.00633</span></span>](https://arxiv.org/abs/1804.00633)