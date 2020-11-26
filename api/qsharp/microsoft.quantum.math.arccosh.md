---
uid: Microsoft.Quantum.Math.ArcCosh
title: ArcCosh 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArcCosh
qsharp.summary: Computes the inverse hyperbolic cosine of a number.
ms.openlocfilehash: a919cd200b378e22aaef609e3c89ba39f3338042
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211222"
---
# <a name="arccosh-function"></a><span data-ttu-id="a2254-102">ArcCosh 함수</span><span class="sxs-lookup"><span data-stu-id="a2254-102">ArcCosh function</span></span>

<span data-ttu-id="a2254-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="a2254-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="a2254-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a2254-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a2254-105">숫자의 역 쌍 곡 코사인을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2254-105">Computes the inverse hyperbolic cosine of a number.</span></span>

```qsharp
function ArcCosh (x : Double) : Double
```


## <a name="input"></a><span data-ttu-id="a2254-106">입력</span><span class="sxs-lookup"><span data-stu-id="a2254-106">Input</span></span>

### <a name="x--double"></a><span data-ttu-id="a2254-107">x: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a2254-107">x : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a2254-108">실수 $x \geq $1.</span><span class="sxs-lookup"><span data-stu-id="a2254-108">A real number $x\geq 1$.</span></span>



## <a name="output--double"></a><span data-ttu-id="a2254-109">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a2254-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a2254-110">$X = \cosh (y) $와 같은 실수 $y $입니다.</span><span class="sxs-lookup"><span data-stu-id="a2254-110">A real number $y$ such that $x = \cosh(y)$.</span></span>