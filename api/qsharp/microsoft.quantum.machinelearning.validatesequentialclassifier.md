---
uid: Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier
title: ValidateSequentialClassifier 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidateSequentialClassifier
qsharp.summary: Validates a given sequential classifier against a given set of pre-labeled samples.
ms.openlocfilehash: c100c5786b18996ce13067f1c4618cf0189578f5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848972"
---
# <a name="validatesequentialclassifier-operation"></a><span data-ttu-id="51cae-102">ValidateSequentialClassifier 작업</span><span class="sxs-lookup"><span data-stu-id="51cae-102">ValidateSequentialClassifier operation</span></span>

<span data-ttu-id="51cae-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="51cae-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="51cae-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="51cae-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="51cae-105">지정 된 미리 레이블이 지정 된 샘플 집합에 대해 지정 된 순차 분류자의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="51cae-105">Validates a given sequential classifier against a given set of pre-labeled samples.</span></span>

```qsharp
operation ValidateSequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], tolerance : Double, nMeasurements : Int, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Microsoft.Quantum.MachineLearning.ValidationResults
```


## <a name="input"></a><span data-ttu-id="51cae-106">입력</span><span class="sxs-lookup"><span data-stu-id="51cae-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="51cae-107">모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="51cae-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="51cae-108">유효성을 검사할 순차 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="51cae-108">The sequential model to be validated.</span></span>


### <a name="samples--labeledsample"></a><span data-ttu-id="51cae-109">샘플: [Labeledsample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span><span class="sxs-lookup"><span data-stu-id="51cae-109">samples : [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span></span>

<span data-ttu-id="51cae-110">지정 된 모델의 유효성을 검사 하는 데 사용할 샘플입니다.</span><span class="sxs-lookup"><span data-stu-id="51cae-110">The samples to be used to validate the given model.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="51cae-111">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="51cae-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="51cae-112">각 샘플을 순차 분류자에 대 한 입력으로 인코딩할 때 사용 하는 근사 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="51cae-112">The approximation tolerance to use in encoding each sample as an input to the sequential classifier.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="51cae-113">n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="51cae-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="51cae-114">각 샘플을 분류 하는 데 사용할 측정 수입니다.</span><span class="sxs-lookup"><span data-stu-id="51cae-114">The number of measurements to use in classifying each sample.</span></span>


### <a name="validationschedule--samplingschedule"></a><span data-ttu-id="51cae-115">validationSchedule: [Samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="51cae-115">validationSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="51cae-116">유효성 검사 집합에서 샘플을 그려야 하는 일정입니다.</span><span class="sxs-lookup"><span data-stu-id="51cae-116">The schedule by which samples should be drawn from the validation set.</span></span>



## <a name="output--validationresults"></a><span data-ttu-id="51cae-117">출력: [Validationresults](xref:Microsoft.Quantum.MachineLearning.ValidationResults)</span><span class="sxs-lookup"><span data-stu-id="51cae-117">Output : [ValidationResults](xref:Microsoft.Quantum.MachineLearning.ValidationResults)</span></span>

<span data-ttu-id="51cae-118">지정 된 유효성 검사의 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="51cae-118">The results of the given validation.</span></span>