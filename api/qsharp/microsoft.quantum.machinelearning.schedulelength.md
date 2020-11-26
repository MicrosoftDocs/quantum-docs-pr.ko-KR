---
uid: Microsoft.Quantum.MachineLearning.ScheduleLength
title: ScheduleLength 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ScheduleLength
qsharp.summary: Returns the number of elements in a given sampling schedule.
ms.openlocfilehash: 008bdcdc0a7c0ad2775dea65ebba46556092beed
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211596"
---
# <a name="schedulelength-function"></a><span data-ttu-id="fa13e-102">ScheduleLength 함수</span><span class="sxs-lookup"><span data-stu-id="fa13e-102">ScheduleLength function</span></span>

<span data-ttu-id="fa13e-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="fa13e-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="fa13e-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="fa13e-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="fa13e-105">지정 된 샘플링 일정의 요소 수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa13e-105">Returns the number of elements in a given sampling schedule.</span></span>

```qsharp
function ScheduleLength (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Int
```


## <a name="input"></a><span data-ttu-id="fa13e-106">입력</span><span class="sxs-lookup"><span data-stu-id="fa13e-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="fa13e-107">일정: [Samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="fa13e-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="fa13e-108">길이가 반환 될 샘플링 일정입니다.</span><span class="sxs-lookup"><span data-stu-id="fa13e-108">A sampling schedule whose length is to be returned.</span></span>



## <a name="output--int"></a><span data-ttu-id="fa13e-109">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fa13e-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fa13e-110">지정 된 샘플링 일정의 요소 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fa13e-110">The number of elements in the given sampling schedule.</span></span>