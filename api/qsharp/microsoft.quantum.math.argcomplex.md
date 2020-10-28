---
uid: Microsoft.Quantum.Math.ArgComplex
title: ArgComplex 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: 629aa32ad80e5aa3d6f5ff75ac65df9b1a96fc15
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723266"
---
# <a name="argcomplex-function"></a><span data-ttu-id="0c5a8-102">ArgComplex 함수</span><span class="sxs-lookup"><span data-stu-id="0c5a8-102">ArgComplex function</span></span>

<span data-ttu-id="0c5a8-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="0c5a8-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="0c5a8-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0c5a8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0c5a8-105">복소수 형식의 단계를 반환 합니다 `Complex` .</span><span class="sxs-lookup"><span data-stu-id="0c5a8-105">Returns the phase of a complex number of type `Complex`.</span></span>

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a><span data-ttu-id="0c5a8-106">입력</span><span class="sxs-lookup"><span data-stu-id="0c5a8-106">Input</span></span>

### <a name="input--complex"></a><span data-ttu-id="0c5a8-107">입력: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="0c5a8-107">input : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="0c5a8-108">복소수 $c = x + i y $입니다.</span><span class="sxs-lookup"><span data-stu-id="0c5a8-108">Complex number $c = x + i y$.</span></span>



## <a name="output--double"></a><span data-ttu-id="0c5a8-109">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0c5a8-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0c5a8-110">단계 $ \text{Arg} [c] = \text{ArcTan} (y, x) \in (-\pi, \pi] $.</span><span class="sxs-lookup"><span data-stu-id="0c5a8-110">Phase $\text{Arg}[c] = \text{ArcTan}(y,x) \in (-\pi,\pi]$.</span></span>