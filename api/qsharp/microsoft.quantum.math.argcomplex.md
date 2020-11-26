---
uid: Microsoft.Quantum.Math.ArgComplex
title: ArgComplex 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: 259296f397207cde4a7d6dfe6cfb1a18e8055216
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211103"
---
# <a name="argcomplex-function"></a><span data-ttu-id="5b516-102">ArgComplex 함수</span><span class="sxs-lookup"><span data-stu-id="5b516-102">ArgComplex function</span></span>

<span data-ttu-id="5b516-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="5b516-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="5b516-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5b516-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5b516-105">복소수 형식의 단계를 반환 합니다 `Complex` .</span><span class="sxs-lookup"><span data-stu-id="5b516-105">Returns the phase of a complex number of type `Complex`.</span></span>

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a><span data-ttu-id="5b516-106">입력</span><span class="sxs-lookup"><span data-stu-id="5b516-106">Input</span></span>

### <a name="input--complex"></a><span data-ttu-id="5b516-107">입력: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="5b516-107">input : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="5b516-108">복소수 $c = x + i y $입니다.</span><span class="sxs-lookup"><span data-stu-id="5b516-108">Complex number $c = x + i y$.</span></span>



## <a name="output--double"></a><span data-ttu-id="5b516-109">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5b516-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5b516-110">단계 $ \text{Arg} [c] = \text{ArcTan} (y, x) \in (-\pi, \pi] $.</span><span class="sxs-lookup"><span data-stu-id="5b516-110">Phase $\text{Arg}[c] = \text{ArcTan}(y,x) \in (-\pi,\pi]$.</span></span>