---
uid: Microsoft.Quantum.Core.RangeEnd
title: 범위 종료 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 90a9e31bf5c4a5e92a35998ddaec8c9e9de9888e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224040"
---
# <a name="rangeend-function"></a><span data-ttu-id="2d9de-102">범위 종료 함수</span><span class="sxs-lookup"><span data-stu-id="2d9de-102">RangeEnd function</span></span>

<span data-ttu-id="2d9de-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="2d9de-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="2d9de-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="2d9de-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="2d9de-105">시퀀스의 마지막 요소가 아닐 수 있는 지정 된 범위의 정의 된 끝 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9de-105">Returns the defined end value of the given range, which is not necessarily the last element in the sequence.</span></span>

```qsharp
function RangeEnd (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="2d9de-106">입력</span><span class="sxs-lookup"><span data-stu-id="2d9de-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="2d9de-107">범위: [범위](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="2d9de-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="2d9de-108">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2d9de-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2d9de-109">지정 된 범위의 정의 된 끝 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9de-109">The defined end value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d9de-110">설명</span><span class="sxs-lookup"><span data-stu-id="2d9de-110">Remarks</span></span>

<span data-ttu-id="2d9de-111">범위 식의 첫 번째 요소는이 `start` `start+step` `start+step+step` 전달 될 때까지, 두 번째 요소는, 세 번째 요소는 등입니다. `end`</span><span class="sxs-lookup"><span data-stu-id="2d9de-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="2d9de-112">범위의 정의 된 끝 값은 범위에 지정 된 시퀀스의 마지막 요소와 다를 수 있습니다. 예를 들어, 범위는 0 .입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9de-112">Note that the defined end value of a range can differ from the last element in the sequence specified by the range; for example, in a range 0 ..</span></span> <span data-ttu-id="2d9de-113">2..</span><span class="sxs-lookup"><span data-stu-id="2d9de-113">2 ..</span></span> <span data-ttu-id="2d9de-114">5 마지막 요소는 4 이지만 끝 값은 5입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9de-114">5 the last element is 4 but the end value is 5.</span></span>