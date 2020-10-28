---
uid: Microsoft.Quantum.Math.PowL
title: PowL 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PowL
qsharp.summary: Returns a number raised to a given power.
ms.openlocfilehash: 22c05cf85acf691490049ce9ac27a7c6b2a4899e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724750"
---
# <a name="powl-function"></a><span data-ttu-id="253df-102">PowL 함수</span><span class="sxs-lookup"><span data-stu-id="253df-102">PowL function</span></span>

<span data-ttu-id="253df-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="253df-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="253df-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="253df-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="253df-105">지정 된 지 수 만큼 거듭제곱 한 숫자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="253df-105">Returns a number raised to a given power.</span></span>

```qsharp
function PowL (a : BigInt, power : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="253df-106">입력</span><span class="sxs-lookup"><span data-stu-id="253df-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="253df-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="253df-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="253df-108">발생 시킬 $ $a 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="253df-108">The number $a$ that is to be raised.</span></span>


### <a name="power--int"></a><span data-ttu-id="253df-109">power: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="253df-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="253df-110">$A $가 발생 해야 하는 power $b $입니다.</span><span class="sxs-lookup"><span data-stu-id="253df-110">The power $b$ to which $a$ should be raised.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="253df-111">출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="253df-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="253df-112">Power $a ^ b $</span><span class="sxs-lookup"><span data-stu-id="253df-112">The power $a^b$</span></span>