---
uid: Microsoft.Quantum.MachineLearning.ScheduleLength
title: ScheduleLength 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ScheduleLength
qsharp.summary: Returns the number of elements in a given sampling schedule.
ms.openlocfilehash: 77538984fbd7334712df423b991ef43ce31ed849
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722405"
---
# <a name="schedulelength-function"></a><span data-ttu-id="78045-102">ScheduleLength 함수</span><span class="sxs-lookup"><span data-stu-id="78045-102">ScheduleLength function</span></span>

<span data-ttu-id="78045-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="78045-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="78045-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="78045-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="78045-105">지정 된 샘플링 일정의 요소 수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="78045-105">Returns the number of elements in a given sampling schedule.</span></span>

```qsharp
function ScheduleLength (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Int
```


## <a name="input"></a><span data-ttu-id="78045-106">입력</span><span class="sxs-lookup"><span data-stu-id="78045-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="78045-107">일정: [Samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="78045-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="78045-108">길이가 반환 될 샘플링 일정입니다.</span><span class="sxs-lookup"><span data-stu-id="78045-108">A sampling schedule whose length is to be returned.</span></span>



## <a name="output--int"></a><span data-ttu-id="78045-109">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="78045-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="78045-110">지정 된 샘플링 일정의 요소 수입니다.</span><span class="sxs-lookup"><span data-stu-id="78045-110">The number of elements in the given sampling schedule.</span></span>