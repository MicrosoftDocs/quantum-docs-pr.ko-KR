---
uid: Microsoft.Quantum.Math.GreatestCommonDivisorI
title: GreatestCommonDivisorI 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: GreatestCommonDivisorI
qsharp.summary: Computes the greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 2b6ba8a6d5ac78b69e6ee20160f3a3b1df61a879
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228477"
---
# <a name="greatestcommondivisori-function"></a><span data-ttu-id="f57a9-102">GreatestCommonDivisorI 함수</span><span class="sxs-lookup"><span data-stu-id="f57a9-102">GreatestCommonDivisorI function</span></span>

<span data-ttu-id="f57a9-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="f57a9-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="f57a9-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f57a9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f57a9-105">$A $ 및 $b $의 최대 공약수를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="f57a9-105">Computes the greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="f57a9-106">GCD는 항상 양수입니다.</span><span class="sxs-lookup"><span data-stu-id="f57a9-106">The GCD is always positive.</span></span>

```qsharp
function GreatestCommonDivisorI (a : Int, b : Int) : Int
```


## <a name="input"></a><span data-ttu-id="f57a9-107">입력</span><span class="sxs-lookup"><span data-stu-id="f57a9-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="f57a9-108">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f57a9-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f57a9-109">확장 된 최대 공약수를 계산 하는 첫 번째 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="f57a9-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--int"></a><span data-ttu-id="f57a9-110">b: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f57a9-110">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f57a9-111">확장 된 최대 공약수를 계산 하는 두 번째 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="f57a9-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--int"></a><span data-ttu-id="f57a9-112">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f57a9-112">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f57a9-113">$a $ 및 $b $의 최대 공약수</span><span class="sxs-lookup"><span data-stu-id="f57a9-113">Greatest common divisor of $a$ and $b$</span></span>