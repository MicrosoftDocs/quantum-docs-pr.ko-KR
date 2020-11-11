---
uid: Microsoft.Quantum.MachineLearning._RunSingleTrainingStep
title: _RunSingleTrainingStep 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: _RunSingleTrainingStep
qsharp.summary: attempts a single parameter update in the direction of mini batch gradient
ms.openlocfilehash: c40bf6f1ceecef2cb196846b4f5a1c49023f1f74
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720625"
---
# <a name="_runsingletrainingstep-operation"></a><span data-ttu-id="a7a9f-102">_RunSingleTrainingStep 작업</span><span class="sxs-lookup"><span data-stu-id="a7a9f-102">_RunSingleTrainingStep operation</span></span>

<span data-ttu-id="a7a9f-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="a7a9f-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="a7a9f-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a7a9f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a7a9f-105">미니 일괄 처리 그라데이션의 단일 매개 변수 업데이트를 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-105">attempts a single parameter update in the direction of mini batch gradient</span></span>

```qsharp
operation _RunSingleTrainingStep (miniBatch : (Microsoft.Quantum.MachineLearning.LabeledSample, Microsoft.Quantum.MachineLearning.StateGenerator)[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, model : Microsoft.Quantum.MachineLearning.SequentialModel) : (Double, Microsoft.Quantum.MachineLearning.SequentialModel)
```


## <a name="input"></a><span data-ttu-id="a7a9f-106">입력</span><span class="sxs-lookup"><span data-stu-id="a7a9f-106">Input</span></span>

### <a name="minibatch--labeledsamplestategenerator"></a><span data-ttu-id="a7a9f-107">미니 일괄 처리: ([Labeledsample](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)) []</span><span class="sxs-lookup"><span data-stu-id="a7a9f-107">miniBatch : ([LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator))[]</span></span>

<span data-ttu-id="a7a9f-108">미니 배치에서 레이블이 지정 된 샘플의 컨테이너</span><span class="sxs-lookup"><span data-stu-id="a7a9f-108">container of labeled samples in the mini batch</span></span>


### <a name="options--trainingoptions"></a><span data-ttu-id="a7a9f-109">옵션: [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="a7a9f-109">options : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>




### <a name="model--sequentialmodel"></a><span data-ttu-id="a7a9f-110">모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="a7a9f-110">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>





## <a name="output--doublesequentialmodel"></a><span data-ttu-id="a7a9f-111">출력: ([Double](xref:microsoft.quantum.lang-ref.double),[SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel))</span><span class="sxs-lookup"><span data-stu-id="a7a9f-111">Output : ([Double](xref:microsoft.quantum.lang-ref.double),[SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel))</span></span>

<span data-ttu-id="a7a9f-112">(유틸리티, (새) 매개 변수) 쌍</span><span class="sxs-lookup"><span data-stu-id="a7a9f-112">(utility, (new)parameters) pair</span></span>