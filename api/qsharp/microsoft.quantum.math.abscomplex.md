---
uid: Microsoft.Quantum.Math.AbsComplex
title: AbsComplex 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: AbsComplex
qsharp.summary: Returns the absolute value of a complex number of type `Complex`.
ms.openlocfilehash: d9afb4b9b37b6cdd83bfd3829d3174d769c5f41b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211392"
---
# <a name="abscomplex-function"></a><span data-ttu-id="ff838-102">AbsComplex 함수</span><span class="sxs-lookup"><span data-stu-id="ff838-102">AbsComplex function</span></span>

<span data-ttu-id="ff838-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="ff838-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="ff838-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ff838-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ff838-105">형식의 복소수의 절대값을 반환 합니다 `Complex` .</span><span class="sxs-lookup"><span data-stu-id="ff838-105">Returns the absolute value of a complex number of type `Complex`.</span></span>

```qsharp
function AbsComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a><span data-ttu-id="ff838-106">입력</span><span class="sxs-lookup"><span data-stu-id="ff838-106">Input</span></span>

### <a name="input--complex"></a><span data-ttu-id="ff838-107">입력: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="ff838-107">input : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="ff838-108">복소수 $c = x + i y $입니다.</span><span class="sxs-lookup"><span data-stu-id="ff838-108">Complex number $c = x + i y$.</span></span>



## <a name="output--double"></a><span data-ttu-id="ff838-109">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ff838-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ff838-110">절대값 $ | c | = \sqrt{x ^ 2 + y ^ 2} $.</span><span class="sxs-lookup"><span data-stu-id="ff838-110">Absolute value $|c| = \sqrt{x^2 + y^2}$.</span></span>