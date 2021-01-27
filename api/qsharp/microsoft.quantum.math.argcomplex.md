---
uid: Microsoft.Quantum.Math.ArgComplex
title: ArgComplex 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: e8ce73a43940ab0ed66338f962cc6f76fc2b694b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842766"
---
# <a name="argcomplex-function"></a><span data-ttu-id="d32f2-102">ArgComplex 함수</span><span class="sxs-lookup"><span data-stu-id="d32f2-102">ArgComplex function</span></span>

<span data-ttu-id="d32f2-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="d32f2-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="d32f2-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d32f2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d32f2-105">복소수 형식의 단계를 반환 합니다 `Complex` .</span><span class="sxs-lookup"><span data-stu-id="d32f2-105">Returns the phase of a complex number of type `Complex`.</span></span>

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a><span data-ttu-id="d32f2-106">입력</span><span class="sxs-lookup"><span data-stu-id="d32f2-106">Input</span></span>

### <a name="input--complex"></a><span data-ttu-id="d32f2-107">입력: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="d32f2-107">input : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="d32f2-108">복소수 $c = x + i y $입니다.</span><span class="sxs-lookup"><span data-stu-id="d32f2-108">Complex number $c = x + i y$.</span></span>



## <a name="output--double"></a><span data-ttu-id="d32f2-109">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d32f2-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d32f2-110">단계 $ \text{Arg} [c] = \text{ArcTan} (y, x) \in (-\pi, \pi] $.</span><span class="sxs-lookup"><span data-stu-id="d32f2-110">Phase $\text{Arg}[c] = \text{ArcTan}(y,x) \in (-\pi,\pi]$.</span></span>