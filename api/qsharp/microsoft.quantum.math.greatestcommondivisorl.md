---
uid: Microsoft.Quantum.Math.GreatestCommonDivisorL
title: GreatestCommonDivisorL 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: GreatestCommonDivisorL
qsharp.summary: Computes the greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 0f545f7888f5a9a353cc6000a12988648ac82dd8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856372"
---
# <a name="greatestcommondivisorl-function"></a><span data-ttu-id="d90f9-102">GreatestCommonDivisorL 함수</span><span class="sxs-lookup"><span data-stu-id="d90f9-102">GreatestCommonDivisorL function</span></span>

<span data-ttu-id="d90f9-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="d90f9-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="d90f9-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d90f9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d90f9-105">$A $ 및 $b $의 최대 공약수를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="d90f9-105">Computes the greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="d90f9-106">GCD는 항상 양수입니다.</span><span class="sxs-lookup"><span data-stu-id="d90f9-106">The GCD is always positive.</span></span>

```qsharp
function GreatestCommonDivisorL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="d90f9-107">입력</span><span class="sxs-lookup"><span data-stu-id="d90f9-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="d90f9-108">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d90f9-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d90f9-109">확장 된 최대 공약수를 계산 하는 첫 번째 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="d90f9-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--bigint"></a><span data-ttu-id="d90f9-110">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d90f9-110">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d90f9-111">확장 된 최대 공약수를 계산 하는 두 번째 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="d90f9-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--bigint"></a><span data-ttu-id="d90f9-112">출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d90f9-112">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d90f9-113">$a $ 및 $b $의 최대 공약수</span><span class="sxs-lookup"><span data-stu-id="d90f9-113">Greatest common divisor of $a$ and $b$</span></span>