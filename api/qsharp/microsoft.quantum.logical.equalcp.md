---
uid: Microsoft.Quantum.Logical.EqualCP
title: EqualCP 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualCP
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: e3175b9b6fd2890963de0452102e2f0de1026b91
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198234"
---
# <a name="equalcp-function"></a><span data-ttu-id="2b83f-102">EqualCP 함수</span><span class="sxs-lookup"><span data-stu-id="2b83f-102">EqualCP function</span></span>

<span data-ttu-id="2b83f-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="2b83f-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="2b83f-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2b83f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2b83f-105">두 입력이 같으면 true를 반환 하 고,</span><span class="sxs-lookup"><span data-stu-id="2b83f-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualCP (a : Microsoft.Quantum.Math.ComplexPolar, b : Microsoft.Quantum.Math.ComplexPolar) : Bool
```


## <a name="input"></a><span data-ttu-id="2b83f-106">입력</span><span class="sxs-lookup"><span data-stu-id="2b83f-106">Input</span></span>

### <a name="a--complexpolar"></a><span data-ttu-id="2b83f-107">a: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="2b83f-107">a : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="2b83f-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2b83f-108">The first value to be compared.</span></span>


### <a name="b--complexpolar"></a><span data-ttu-id="2b83f-109">b: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="2b83f-109">b : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="2b83f-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2b83f-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="2b83f-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2b83f-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2b83f-112">`true` 가와 같으면이 고, 그렇지 않으면입니다 `a` `b` .</span><span class="sxs-lookup"><span data-stu-id="2b83f-112">`true` if and only if `a` is equal to `b`.</span></span>