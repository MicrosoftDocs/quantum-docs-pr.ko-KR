---
uid: Microsoft.Quantum.MachineLearning.EstimateGradient
title: EstimateGradient 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateGradient
qsharp.summary: Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.
ms.openlocfilehash: 38edcb67e7dcc5d2e971fb507a792937774a702c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844391"
---
# <a name="estimategradient-operation"></a><span data-ttu-id="e0c60-102">EstimateGradient 작업</span><span class="sxs-lookup"><span data-stu-id="e0c60-102">EstimateGradient operation</span></span>

<span data-ttu-id="e0c60-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="e0c60-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="e0c60-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="e0c60-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="e0c60-105">특정 모델 및 지정 된 인코딩된 입력에 대 한 순차 분류자의 학습 그라데이션을 추정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0c60-105">Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.</span></span>

```qsharp
operation EstimateGradient (model : Microsoft.Quantum.MachineLearning.SequentialModel, encodedInput : Microsoft.Quantum.MachineLearning.StateGenerator, nMeasurements : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="e0c60-106">입력</span><span class="sxs-lookup"><span data-stu-id="e0c60-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="e0c60-107">모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="e0c60-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="e0c60-108">그라데이션을 예상할 순차 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="e0c60-108">The sequential model whose gradient is to be estimated.</span></span>


### <a name="encodedinput--stategenerator"></a><span data-ttu-id="e0c60-109">encodedInput: [Stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="e0c60-109">encodedInput : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="e0c60-110">상태 준비 작업으로 인코딩된 순차 분류자에 대 한 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="e0c60-110">An input to the sequential classifier, encoded into a state preparation operation.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="e0c60-111">n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e0c60-111">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e0c60-112">그라데이션을 예측 하는 데 사용할 측정 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e0c60-112">The number of measurements to use in estimating the gradient.</span></span>



## <a name="output--double"></a><span data-ttu-id="e0c60-113">Output: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="e0c60-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="e0c60-114">지정 된 입력 및 모델 매개 변수에 대 한 예상 학습 그라데이션입니다.</span><span class="sxs-lookup"><span data-stu-id="e0c60-114">An estimate of the training gradient at the given input and model parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0c60-115">설명</span><span class="sxs-lookup"><span data-stu-id="e0c60-115">Remarks</span></span>

<span data-ttu-id="e0c60-116">이 작업에서는 Hadamard 테스트를 사용 하 고 매개 변수를 함께 사용 하 여 그라데이션을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0c60-116">This operation uses a Hadamard test and the parameter shift technique together to estimate the gradient.</span></span>