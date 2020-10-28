---
uid: Microsoft.Quantum.Logical.EqualCP
title: EqualCP 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualCP
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: c8ee7e6a04cc2478f1c97fcc1d964a1574f7b1fa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720757"
---
# <a name="equalcp-function"></a><span data-ttu-id="a1520-102">EqualCP 함수</span><span class="sxs-lookup"><span data-stu-id="a1520-102">EqualCP function</span></span>

<span data-ttu-id="a1520-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a1520-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a1520-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a1520-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a1520-105">두 입력이 같으면 true를 반환 하 고,</span><span class="sxs-lookup"><span data-stu-id="a1520-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualCP (a : Microsoft.Quantum.Math.ComplexPolar, b : Microsoft.Quantum.Math.ComplexPolar) : Bool
```


## <a name="input"></a><span data-ttu-id="a1520-106">입력</span><span class="sxs-lookup"><span data-stu-id="a1520-106">Input</span></span>

### <a name="a--complexpolar"></a><span data-ttu-id="a1520-107">a: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="a1520-107">a : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="a1520-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a1520-108">The first value to be compared.</span></span>


### <a name="b--complexpolar"></a><span data-ttu-id="a1520-109">b: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="a1520-109">b : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="a1520-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a1520-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a1520-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a1520-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a1520-112">`true` 가와 같으면이 고, 그렇지 않으면입니다 `a` `b` .</span><span class="sxs-lookup"><span data-stu-id="a1520-112">`true` if and only if `a` is equal to `b`.</span></span>