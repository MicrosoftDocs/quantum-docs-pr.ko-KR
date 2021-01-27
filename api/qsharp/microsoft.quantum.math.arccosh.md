---
uid: Microsoft.Quantum.Math.ArcCosh
title: ArcCosh 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArcCosh
qsharp.summary: Computes the inverse hyperbolic cosine of a number.
ms.openlocfilehash: 5598e45f7cc34cdc686b26655c267a06b8476db0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848959"
---
# <a name="arccosh-function"></a><span data-ttu-id="58ab7-102">ArcCosh 함수</span><span class="sxs-lookup"><span data-stu-id="58ab7-102">ArcCosh function</span></span>

<span data-ttu-id="58ab7-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="58ab7-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="58ab7-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="58ab7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="58ab7-105">숫자의 역 쌍 곡 코사인을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="58ab7-105">Computes the inverse hyperbolic cosine of a number.</span></span>

```qsharp
function ArcCosh (x : Double) : Double
```


## <a name="input"></a><span data-ttu-id="58ab7-106">입력</span><span class="sxs-lookup"><span data-stu-id="58ab7-106">Input</span></span>

### <a name="x--double"></a><span data-ttu-id="58ab7-107">x: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="58ab7-107">x : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="58ab7-108">실수 $x \geq $1.</span><span class="sxs-lookup"><span data-stu-id="58ab7-108">A real number $x\geq 1$.</span></span>



## <a name="output--double"></a><span data-ttu-id="58ab7-109">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="58ab7-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="58ab7-110">$X = \cosh (y) $와 같은 실수 $y $입니다.</span><span class="sxs-lookup"><span data-stu-id="58ab7-110">A real number $y$ such that $x = \cosh(y)$.</span></span>