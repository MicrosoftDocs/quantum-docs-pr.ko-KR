---
uid: Microsoft.Quantum.Arrays.IsEmpty
title: IsEmpty 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsEmpty
qsharp.summary: Returns true if and only if an array is empty.
ms.openlocfilehash: f658c2a25b6991d9a826706a7e95b68169901f0e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719113"
---
# <a name="isempty-function"></a><span data-ttu-id="faba7-102">IsEmpty 함수</span><span class="sxs-lookup"><span data-stu-id="faba7-102">IsEmpty function</span></span>

<span data-ttu-id="faba7-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="faba7-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="faba7-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="faba7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="faba7-105">배열이 비어 있는 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="faba7-105">Returns true if and only if an array is empty.</span></span>

```qsharp
function IsEmpty<'T> (array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="faba7-106">입력</span><span class="sxs-lookup"><span data-stu-id="faba7-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="faba7-107">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="faba7-107">array : 'T[]</span></span>

<span data-ttu-id="faba7-108">확인할 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="faba7-108">The array to be checked.</span></span>



## <a name="output--bool"></a><span data-ttu-id="faba7-109">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="faba7-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="faba7-110">`true` 배열이 비어 있으면 (길이가 0 인 경우에만)입니다.</span><span class="sxs-lookup"><span data-stu-id="faba7-110">`true` if and only if the array is empty (has length 0).</span></span>

## <a name="type-parameters"></a><span data-ttu-id="faba7-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="faba7-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="faba7-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="faba7-112">'T</span></span>

