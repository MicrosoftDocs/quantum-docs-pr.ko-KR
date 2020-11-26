---
uid: Microsoft.Quantum.Logical.EqualC
title: EqualC 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualC
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 4c511489888613d95adaf154c005b3211af75446
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198387"
---
# <a name="equalc-function"></a><span data-ttu-id="92d8c-102">EqualC 함수</span><span class="sxs-lookup"><span data-stu-id="92d8c-102">EqualC function</span></span>

<span data-ttu-id="92d8c-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="92d8c-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="92d8c-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="92d8c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="92d8c-105">두 입력이 같으면 true를 반환 하 고,</span><span class="sxs-lookup"><span data-stu-id="92d8c-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualC (a : Microsoft.Quantum.Math.Complex, b : Microsoft.Quantum.Math.Complex) : Bool
```


## <a name="input"></a><span data-ttu-id="92d8c-106">입력</span><span class="sxs-lookup"><span data-stu-id="92d8c-106">Input</span></span>

### <a name="a--complex"></a><span data-ttu-id="92d8c-107">a: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="92d8c-107">a : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="92d8c-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="92d8c-108">The first value to be compared.</span></span>


### <a name="b--complex"></a><span data-ttu-id="92d8c-109">b: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="92d8c-109">b : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="92d8c-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="92d8c-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="92d8c-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="92d8c-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="92d8c-112">`true` 가와 같으면이 고, 그렇지 않으면입니다 `a` `b` .</span><span class="sxs-lookup"><span data-stu-id="92d8c-112">`true` if and only if `a` is equal to `b`.</span></span>