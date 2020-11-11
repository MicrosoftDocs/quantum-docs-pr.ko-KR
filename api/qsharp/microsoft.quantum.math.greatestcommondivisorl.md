---
uid: Microsoft.Quantum.Math.GreatestCommonDivisorL
title: GreatestCommonDivisorL 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: GreatestCommonDivisorL
qsharp.summary: Computes the greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 77bdb040908e9a8af81dee09451a3582f7b7d159
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723644"
---
# <a name="greatestcommondivisorl-function"></a><span data-ttu-id="4d8f3-102">GreatestCommonDivisorL 함수</span><span class="sxs-lookup"><span data-stu-id="4d8f3-102">GreatestCommonDivisorL function</span></span>

<span data-ttu-id="4d8f3-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="4d8f3-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="4d8f3-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4d8f3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4d8f3-105">$A $ 및 $b $의 최대 공약수를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d8f3-105">Computes the greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="4d8f3-106">GCD는 항상 양수입니다.</span><span class="sxs-lookup"><span data-stu-id="4d8f3-106">The GCD is always positive.</span></span>

```qsharp
function GreatestCommonDivisorL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="4d8f3-107">입력</span><span class="sxs-lookup"><span data-stu-id="4d8f3-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="4d8f3-108">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="4d8f3-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="4d8f3-109">확장 된 최대 공약수를 계산 하는 첫 번째 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="4d8f3-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--bigint"></a><span data-ttu-id="4d8f3-110">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="4d8f3-110">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="4d8f3-111">확장 된 최대 공약수를 계산 하는 두 번째 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="4d8f3-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--bigint"></a><span data-ttu-id="4d8f3-112">출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="4d8f3-112">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="4d8f3-113">$a $ 및 $b $의 최대 공약수</span><span class="sxs-lookup"><span data-stu-id="4d8f3-113">Greatest common divisor of $a$ and $b$</span></span>