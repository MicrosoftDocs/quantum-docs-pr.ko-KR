---
uid: Microsoft.Quantum.Arrays.IsEmpty
title: IsEmpty 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsEmpty
qsharp.summary: Returns true if and only if an array is empty.
ms.openlocfilehash: 1d402b5cfe3a42b47d4ded7064fee06a393772b9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845768"
---
# <a name="isempty-function"></a><span data-ttu-id="ea265-102">IsEmpty 함수</span><span class="sxs-lookup"><span data-stu-id="ea265-102">IsEmpty function</span></span>

<span data-ttu-id="ea265-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ea265-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ea265-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ea265-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ea265-105">배열이 비어 있는 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea265-105">Returns true if and only if an array is empty.</span></span>

```qsharp
function IsEmpty<'T> (array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="ea265-106">입력</span><span class="sxs-lookup"><span data-stu-id="ea265-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="ea265-107">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="ea265-107">array : 'T[]</span></span>

<span data-ttu-id="ea265-108">확인할 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ea265-108">The array to be checked.</span></span>



## <a name="output--bool"></a><span data-ttu-id="ea265-109">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ea265-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ea265-110">`true` 배열이 비어 있으면 (길이가 0 인 경우에만)입니다.</span><span class="sxs-lookup"><span data-stu-id="ea265-110">`true` if and only if the array is empty (has length 0).</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ea265-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ea265-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ea265-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="ea265-112">'T</span></span>

