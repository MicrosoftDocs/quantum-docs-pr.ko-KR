---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: 샘플링 된 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: 9f9f91bc50861c5b31a76e28050189d13efda71e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722426"
---
# <a name="sampled-function"></a><span data-ttu-id="2943a-102">샘플링 된 함수</span><span class="sxs-lookup"><span data-stu-id="2943a-102">Sampled function</span></span>

<span data-ttu-id="2943a-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="2943a-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="2943a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2943a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2943a-105">지정 된 일정을 사용 하 여 지정 된 배열을 샘플링 합니다.</span><span class="sxs-lookup"><span data-stu-id="2943a-105">Samples a given array, using the given schedule.</span></span>

```qsharp
function Sampled<'T> (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, values : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="2943a-106">입력</span><span class="sxs-lookup"><span data-stu-id="2943a-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="2943a-107">일정: [Samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="2943a-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="2943a-108">샘플링 값에 사용할 일정입니다.</span><span class="sxs-lookup"><span data-stu-id="2943a-108">A schedule to use in sampling values.</span></span>


### <a name="values--t"></a><span data-ttu-id="2943a-109">값: ' ' '</span><span class="sxs-lookup"><span data-stu-id="2943a-109">values : 'T[]</span></span>

<span data-ttu-id="2943a-110">샘플링할 값의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="2943a-110">An array of values to be sampled.</span></span>



## <a name="output--t"></a><span data-ttu-id="2943a-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="2943a-111">Output : 'T[]</span></span>

<span data-ttu-id="2943a-112">지정 된 일정에 따라 값의 요소 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="2943a-112">An array of elements from values, following the given schedule.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2943a-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2943a-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2943a-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="2943a-114">'T</span></span>
