---
uid: Microsoft.Quantum.Arrays.EmptyArray
title: EmptyArray 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EmptyArray
qsharp.summary: Returns the empty array of a given type.
ms.openlocfilehash: cf15e61862bb64fb3408db2318fafb56d532b365
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846171"
---
# <a name="emptyarray-function"></a><span data-ttu-id="6a1a6-102">EmptyArray 함수</span><span class="sxs-lookup"><span data-stu-id="6a1a6-102">EmptyArray function</span></span>

<span data-ttu-id="6a1a6-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6a1a6-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6a1a6-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="6a1a6-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="6a1a6-105">지정 된 형식의 빈 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a1a6-105">Returns the empty array of a given type.</span></span>

```qsharp
function EmptyArray<'TElement> () : 'TElement[]
```


## <a name="output--telement"></a><span data-ttu-id="6a1a6-106">출력: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="6a1a6-106">Output : 'TElement[]</span></span>

<span data-ttu-id="6a1a6-107">빈 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="6a1a6-107">The empty array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6a1a6-108">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6a1a6-108">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="6a1a6-109">' TElement</span><span class="sxs-lookup"><span data-stu-id="6a1a6-109">'TElement</span></span>

<span data-ttu-id="6a1a6-110">배열의 요소 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="6a1a6-110">The type of elements of the array.</span></span>

## <a name="example"></a><span data-ttu-id="6a1a6-111">예제</span><span class="sxs-lookup"><span data-stu-id="6a1a6-111">Example</span></span>

```qsharp
let empty = EmptyArray<Int>();
```