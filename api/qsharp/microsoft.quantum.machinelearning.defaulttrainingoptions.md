---
uid: Microsoft.Quantum.MachineLearning.DefaultTrainingOptions
title: DefaultTrainingOptions 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: DefaultTrainingOptions
qsharp.summary: Returns a default set of options for training classifiers.
ms.openlocfilehash: 474683ce5b9ec22bec686fb29d87728afe24d23a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856001"
---
# <a name="defaulttrainingoptions-function"></a><span data-ttu-id="ada28-102">DefaultTrainingOptions 함수</span><span class="sxs-lookup"><span data-stu-id="ada28-102">DefaultTrainingOptions function</span></span>

<span data-ttu-id="ada28-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ada28-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="ada28-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ada28-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="ada28-105">학습용 분류자에 대 한 기본 옵션 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada28-105">Returns a default set of options for training classifiers.</span></span>

```qsharp
function DefaultTrainingOptions () : Microsoft.Quantum.MachineLearning.TrainingOptions
```


## <a name="output--trainingoptions"></a><span data-ttu-id="ada28-106">출력: [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="ada28-106">Output : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>

<span data-ttu-id="ada28-107">분류자를 학습 하는 데 사용할 적절 한 기본 교육 옵션 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="ada28-107">A reasonable set of default training options for use when training classifiers.</span></span>

## <a name="example"></a><span data-ttu-id="ada28-108">예</span><span class="sxs-lookup"><span data-stu-id="ada28-108">Example</span></span>

<span data-ttu-id="ada28-109">기본 옵션을 사용 하지만 추가 측정을 사용 하려면 연산자를 사용 합니다 `w/` .</span><span class="sxs-lookup"><span data-stu-id="ada28-109">To use the default options, but with additional measurements, use the `w/` operator:</span></span>

```qsharp
let options = DefaultTrainingOptions()
    w/ NMeasurements <- 1000000;
```