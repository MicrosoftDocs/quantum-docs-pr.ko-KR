---
uid: Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier
title: ValidateSequentialClassifier 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidateSequentialClassifier
qsharp.summary: Validates a given sequential classifier against a given set of pre-labeled samples.
ms.openlocfilehash: 802f1045ea4086bd371d68018a481182cb75b209
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720445"
---
# <a name="validatesequentialclassifier-operation"></a><span data-ttu-id="01066-102">ValidateSequentialClassifier 작업</span><span class="sxs-lookup"><span data-stu-id="01066-102">ValidateSequentialClassifier operation</span></span>

<span data-ttu-id="01066-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="01066-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="01066-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="01066-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="01066-105">지정 된 미리 레이블이 지정 된 샘플 집합에 대해 지정 된 순차 분류자의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="01066-105">Validates a given sequential classifier against a given set of pre-labeled samples.</span></span>

```qsharp
operation ValidateSequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], tolerance : Double, nMeasurements : Int, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Microsoft.Quantum.MachineLearning.ValidationResults
```


## <a name="input"></a><span data-ttu-id="01066-106">입력</span><span class="sxs-lookup"><span data-stu-id="01066-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="01066-107">모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="01066-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="01066-108">유효성을 검사할 순차 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="01066-108">The sequential model to be validated.</span></span>


### <a name="samples--labeledsample"></a><span data-ttu-id="01066-109">샘플: [Labeledsample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span><span class="sxs-lookup"><span data-stu-id="01066-109">samples : [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span></span>

<span data-ttu-id="01066-110">지정 된 모델의 유효성을 검사 하는 데 사용할 샘플입니다.</span><span class="sxs-lookup"><span data-stu-id="01066-110">The samples to be used to validate the given model.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="01066-111">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="01066-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="01066-112">각 샘플을 순차 분류자에 대 한 입력으로 인코딩할 때 사용 하는 근사 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="01066-112">The approximation tolerance to use in encoding each sample as an input to the sequential classifier.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="01066-113">n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="01066-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="01066-114">각 샘플을 분류 하는 데 사용할 측정 수입니다.</span><span class="sxs-lookup"><span data-stu-id="01066-114">The number of measurements to use in classifying each sample.</span></span>


### <a name="validationschedule--samplingschedule"></a><span data-ttu-id="01066-115">validationSchedule: [Samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="01066-115">validationSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="01066-116">유효성 검사 집합에서 샘플을 그려야 하는 일정입니다.</span><span class="sxs-lookup"><span data-stu-id="01066-116">The schedule by which samples should be drawn from the validation set.</span></span>



## <a name="output--validationresults"></a><span data-ttu-id="01066-117">출력: [Validationresults](xref:Microsoft.Quantum.MachineLearning.ValidationResults)</span><span class="sxs-lookup"><span data-stu-id="01066-117">Output : [ValidationResults](xref:Microsoft.Quantum.MachineLearning.ValidationResults)</span></span>

<span data-ttu-id="01066-118">지정 된 유효성 검사의 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="01066-118">The results of the given validation.</span></span>