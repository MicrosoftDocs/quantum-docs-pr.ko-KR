---
uid: Microsoft.Quantum.Core.RangeStart
title: 범위 시작 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStart
qsharp.summary: Returns the defined start value of the given range.
ms.openlocfilehash: 3e4b0cebe34b4c98cb1d582a9cd11b46ff778517
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713168"
---
# <a name="rangestart-function"></a><span data-ttu-id="9f881-102">범위 시작 함수</span><span class="sxs-lookup"><span data-stu-id="9f881-102">RangeStart function</span></span>

<span data-ttu-id="9f881-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="9f881-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="9f881-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9f881-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9f881-105">지정 된 범위의 정의 된 시작 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f881-105">Returns the defined start value of the given range.</span></span>

```qsharp
function RangeStart (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="9f881-106">입력</span><span class="sxs-lookup"><span data-stu-id="9f881-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="9f881-107">범위: [범위](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="9f881-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="9f881-108">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9f881-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9f881-109">지정 된 범위의 정의 된 시작 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9f881-109">The defined start value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f881-110">설명</span><span class="sxs-lookup"><span data-stu-id="9f881-110">Remarks</span></span>

<span data-ttu-id="9f881-111">범위 식의 첫 번째 요소는이 `start` `start+step` `start+step+step` 전달 될 때까지, 두 번째 요소는, 세 번째 요소는 등입니다. `end`</span><span class="sxs-lookup"><span data-stu-id="9f881-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="9f881-112">범위에서 정의 된 시작 값은 범위에서 빈 시퀀스 (예: 2.)를 지정 하는 경우를 제외 하 고는 시퀀스의 첫 번째 요소와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f881-112">Note that the defined start value of a range is the same as the first element of the sequence, unless the range specifies an empty sequence (for example, 2 ..</span></span> <span data-ttu-id="9f881-113">1).</span><span class="sxs-lookup"><span data-stu-id="9f881-113">1).</span></span>