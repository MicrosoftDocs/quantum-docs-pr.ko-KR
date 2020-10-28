---
uid: Microsoft.Quantum.Core.RangeStep
title: RangeStep 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStep
qsharp.summary: Returns the integer that specifies how the next value of a range is calculated.
ms.openlocfilehash: f8e4c42330f2d6afdc1c0a9bdde36081ccab2f94
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713161"
---
# <a name="rangestep-function"></a><span data-ttu-id="df568-102">RangeStep 함수</span><span class="sxs-lookup"><span data-stu-id="df568-102">RangeStep function</span></span>

<span data-ttu-id="df568-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="df568-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="df568-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="df568-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="df568-105">범위의 다음 값이 계산 되는 방법을 지정 하는 정수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="df568-105">Returns the integer that specifies how the next value of a range is calculated.</span></span>

```qsharp
function RangeStep (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="df568-106">입력</span><span class="sxs-lookup"><span data-stu-id="df568-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="df568-107">범위: [범위](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="df568-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="df568-108">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="df568-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="df568-109">지정 된 범위의 정의 된 단계 값입니다.</span><span class="sxs-lookup"><span data-stu-id="df568-109">The defined step value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="df568-110">설명</span><span class="sxs-lookup"><span data-stu-id="df568-110">Remarks</span></span>

<span data-ttu-id="df568-111">범위 식의 첫 번째 요소는이 `start` `start+step` `start+step+step` 전달 될 때까지, 두 번째 요소는, 세 번째 요소는 등입니다. `end`</span><span class="sxs-lookup"><span data-stu-id="df568-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>