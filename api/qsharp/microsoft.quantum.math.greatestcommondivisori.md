---
uid: Microsoft.Quantum.Math.GreatestCommonDivisorI
title: GreatestCommonDivisorI 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: GreatestCommonDivisorI
qsharp.summary: Computes the greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 9f76d5ac47faed9a353db4172cc9037411ab1198
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847309"
---
# <a name="greatestcommondivisori-function"></a><span data-ttu-id="9e820-102">GreatestCommonDivisorI 함수</span><span class="sxs-lookup"><span data-stu-id="9e820-102">GreatestCommonDivisorI function</span></span>

<span data-ttu-id="9e820-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="9e820-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="9e820-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9e820-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9e820-105">$A $ 및 $b $의 최대 공약수를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e820-105">Computes the greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="9e820-106">GCD는 항상 양수입니다.</span><span class="sxs-lookup"><span data-stu-id="9e820-106">The GCD is always positive.</span></span>

```qsharp
function GreatestCommonDivisorI (a : Int, b : Int) : Int
```


## <a name="input"></a><span data-ttu-id="9e820-107">입력</span><span class="sxs-lookup"><span data-stu-id="9e820-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="9e820-108">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9e820-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9e820-109">확장 된 최대 공약수를 계산 하는 첫 번째 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="9e820-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--int"></a><span data-ttu-id="9e820-110">b: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9e820-110">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9e820-111">확장 된 최대 공약수를 계산 하는 두 번째 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="9e820-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--int"></a><span data-ttu-id="9e820-112">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9e820-112">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9e820-113">$a $ 및 $b $의 최대 공약수</span><span class="sxs-lookup"><span data-stu-id="9e820-113">Greatest common divisor of $a$ and $b$</span></span>