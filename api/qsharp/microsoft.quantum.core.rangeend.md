---
uid: Microsoft.Quantum.Core.RangeEnd
title: 범위 종료 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 4dbcf517c4dc17775040444c77deb0e449082390
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713245"
---
# <a name="rangeend-function"></a><span data-ttu-id="e4a3e-102">범위 종료 함수</span><span class="sxs-lookup"><span data-stu-id="e4a3e-102">RangeEnd function</span></span>

<span data-ttu-id="e4a3e-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="e4a3e-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="e4a3e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e4a3e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e4a3e-105">시퀀스의 마지막 요소가 아닐 수 있는 지정 된 범위의 정의 된 끝 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4a3e-105">Returns the defined end value of the given range, which is not necessarily the last element in the sequence.</span></span>

```qsharp
function RangeEnd (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="e4a3e-106">입력</span><span class="sxs-lookup"><span data-stu-id="e4a3e-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="e4a3e-107">범위: [범위](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="e4a3e-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="e4a3e-108">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e4a3e-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e4a3e-109">지정 된 범위의 정의 된 끝 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e4a3e-109">The defined end value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4a3e-110">설명</span><span class="sxs-lookup"><span data-stu-id="e4a3e-110">Remarks</span></span>

<span data-ttu-id="e4a3e-111">범위 식의 첫 번째 요소는이 `start` `start+step` `start+step+step` 전달 될 때까지, 두 번째 요소는, 세 번째 요소는 등입니다. `end`</span><span class="sxs-lookup"><span data-stu-id="e4a3e-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="e4a3e-112">범위의 정의 된 끝 값은 범위에 지정 된 시퀀스의 마지막 요소와 다를 수 있습니다. 예를 들어, 범위는 0 .입니다.</span><span class="sxs-lookup"><span data-stu-id="e4a3e-112">Note that the defined end value of a range can differ from the last element in the sequence specified by the range; for example, in a range 0 ..</span></span> <span data-ttu-id="e4a3e-113">2..</span><span class="sxs-lookup"><span data-stu-id="e4a3e-113">2 ..</span></span> <span data-ttu-id="e4a3e-114">5 마지막 요소는 4 이지만 끝 값은 5입니다.</span><span class="sxs-lookup"><span data-stu-id="e4a3e-114">5 the last element is 4 but the end value is 5.</span></span>