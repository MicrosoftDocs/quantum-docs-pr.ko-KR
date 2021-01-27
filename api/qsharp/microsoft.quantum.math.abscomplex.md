---
uid: Microsoft.Quantum.Math.AbsComplex
title: AbsComplex 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: AbsComplex
qsharp.summary: Returns the absolute value of a complex number of type `Complex`.
ms.openlocfilehash: 2bb4caa140bef36d893da834eac1c94b8dd8b0e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846080"
---
# <a name="abscomplex-function"></a><span data-ttu-id="ac6a3-102">AbsComplex 함수</span><span class="sxs-lookup"><span data-stu-id="ac6a3-102">AbsComplex function</span></span>

<span data-ttu-id="ac6a3-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="ac6a3-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="ac6a3-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ac6a3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ac6a3-105">형식의 복소수의 절대값을 반환 합니다 `Complex` .</span><span class="sxs-lookup"><span data-stu-id="ac6a3-105">Returns the absolute value of a complex number of type `Complex`.</span></span>

```qsharp
function AbsComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a><span data-ttu-id="ac6a3-106">입력</span><span class="sxs-lookup"><span data-stu-id="ac6a3-106">Input</span></span>

### <a name="input--complex"></a><span data-ttu-id="ac6a3-107">입력: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="ac6a3-107">input : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="ac6a3-108">복소수 $c = x + i y $입니다.</span><span class="sxs-lookup"><span data-stu-id="ac6a3-108">Complex number $c = x + i y$.</span></span>



## <a name="output--double"></a><span data-ttu-id="ac6a3-109">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ac6a3-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ac6a3-110">절대값 $ | c | = \sqrt{x ^ 2 + y ^ 2} $.</span><span class="sxs-lookup"><span data-stu-id="ac6a3-110">Absolute value $|c| = \sqrt{x^2 + y^2}$.</span></span>