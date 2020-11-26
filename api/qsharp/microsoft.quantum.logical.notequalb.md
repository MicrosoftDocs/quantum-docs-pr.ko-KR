---
uid: Microsoft.Quantum.Logical.NotEqualB
title: NotEqualB 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualB
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 7943411b662683df058213a9e4b8eb7c9329ff07
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197384"
---
# <a name="notequalb-function"></a><span data-ttu-id="839e3-102">NotEqualB 함수</span><span class="sxs-lookup"><span data-stu-id="839e3-102">NotEqualB function</span></span>

<span data-ttu-id="839e3-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="839e3-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="839e3-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="839e3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="839e3-105">두 입력이 같지 않은 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="839e3-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="839e3-106">입력</span><span class="sxs-lookup"><span data-stu-id="839e3-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="839e3-107">a: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="839e3-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="839e3-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="839e3-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="839e3-109">b: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="839e3-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="839e3-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="839e3-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="839e3-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="839e3-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="839e3-112">`true``a`가와 같지 않은 경우에만입니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="839e3-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="839e3-113">설명</span><span class="sxs-lookup"><span data-stu-id="839e3-113">Remarks</span></span>

<span data-ttu-id="839e3-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="839e3-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualB(a, b);
```