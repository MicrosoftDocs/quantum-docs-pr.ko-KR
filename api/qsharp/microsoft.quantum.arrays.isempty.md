---
uid: Microsoft.Quantum.Arrays.IsEmpty
title: IsEmpty 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsEmpty
qsharp.summary: Returns true if and only if an array is empty.
ms.openlocfilehash: ae3ad8763987bab9fdae07a5fe9bd4aabef65205
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220980"
---
# <a name="isempty-function"></a><span data-ttu-id="e8b4f-102">IsEmpty 함수</span><span class="sxs-lookup"><span data-stu-id="e8b4f-102">IsEmpty function</span></span>

<span data-ttu-id="e8b4f-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e8b4f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e8b4f-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e8b4f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e8b4f-105">배열이 비어 있는 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8b4f-105">Returns true if and only if an array is empty.</span></span>

```qsharp
function IsEmpty<'T> (array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="e8b4f-106">입력</span><span class="sxs-lookup"><span data-stu-id="e8b4f-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="e8b4f-107">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="e8b4f-107">array : 'T[]</span></span>

<span data-ttu-id="e8b4f-108">확인할 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="e8b4f-108">The array to be checked.</span></span>



## <a name="output--bool"></a><span data-ttu-id="e8b4f-109">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e8b4f-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e8b4f-110">`true` 배열이 비어 있으면 (길이가 0 인 경우에만)입니다.</span><span class="sxs-lookup"><span data-stu-id="e8b4f-110">`true` if and only if the array is empty (has length 0).</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e8b4f-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e8b4f-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e8b4f-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="e8b4f-112">'T</span></span>

