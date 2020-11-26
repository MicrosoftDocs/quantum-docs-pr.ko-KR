---
uid: Microsoft.Quantum.Core.RangeReverse
title: RangeReverse 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: 7bd7c55abe0b56b9d30b4c6e91f7175101dd2948
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213840"
---
# <a name="rangereverse-function"></a><span data-ttu-id="274c6-102">RangeReverse 함수</span><span class="sxs-lookup"><span data-stu-id="274c6-102">RangeReverse function</span></span>

<span data-ttu-id="274c6-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="274c6-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="274c6-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="274c6-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="274c6-105">입력 범위의 역순 인 새 범위를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="274c6-105">Returns a new range which is the reverse of the input range.</span></span>

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a><span data-ttu-id="274c6-106">입력</span><span class="sxs-lookup"><span data-stu-id="274c6-106">Input</span></span>

### <a name="r--range"></a><span data-ttu-id="274c6-107">r: [범위](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="274c6-107">r : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="274c6-108">입력 범위.</span><span class="sxs-lookup"><span data-stu-id="274c6-108">Input range.</span></span>



## <a name="output--range"></a><span data-ttu-id="274c6-109">출력: [범위](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="274c6-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="274c6-110">지정 된 범위의 역순 인 새 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="274c6-110">A new range that is the reverse of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="274c6-111">설명</span><span class="sxs-lookup"><span data-stu-id="274c6-111">Remarks</span></span>

<span data-ttu-id="274c6-112">범위의 `end` `-step` `start` 마지막 요소는와 같을 수 없기 때문에 범위를 반대로 하는 것은 간단 합니다. `end`</span><span class="sxs-lookup"><span data-stu-id="274c6-112">Note that the reverse of a range is not simply `end`..`-step`..`start`, because the actual last element of a range may not be the same as `end`.</span></span>