---
uid: Microsoft.Quantum.Math.ExpModL
title: ExpModL 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 07da113caeb9f6f3f3f3f92f13478f33021bfa14
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210752"
---
# <a name="expmodl-function"></a><span data-ttu-id="98ef4-102">ExpModL 함수</span><span class="sxs-lookup"><span data-stu-id="98ef4-102">ExpModL function</span></span>

<span data-ttu-id="98ef4-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="98ef4-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="98ef4-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="98ef4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="98ef4-105">지정 된 모듈러스와 관련 하 여 지정 된 지 수 만큼 거듭제곱 한 정수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="98ef4-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModL (expBase : BigInt, power : BigInt, modulus : BigInt) : BigInt
```


## <a name="description"></a><span data-ttu-id="98ef4-106">Description</span><span class="sxs-lookup"><span data-stu-id="98ef4-106">Description</span></span>

<span data-ttu-id="98ef4-107">$X $, power by $p $ 및 모듈러스를 $N $로 하 여이를 기반으로 하는 것을 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98ef4-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="98ef4-108">함수는 $x ^ p \operatorname{mod} N $을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="98ef4-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="98ef4-109">$N $, $x $는 양수가 고 전원은 음수가 아닌 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="98ef4-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="98ef4-110">입력</span><span class="sxs-lookup"><span data-stu-id="98ef4-110">Input</span></span>

### <a name="expbase--bigint"></a><span data-ttu-id="98ef4-111">기본: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="98ef4-111">expBase : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="power--bigint"></a><span data-ttu-id="98ef4-112">power: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="98ef4-112">power : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="modulus--bigint"></a><span data-ttu-id="98ef4-113">모듈러스: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="98ef4-113">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigint"></a><span data-ttu-id="98ef4-114">출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="98ef4-114">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>



## <a name="remarks"></a><span data-ttu-id="98ef4-115">설명</span><span class="sxs-lookup"><span data-stu-id="98ef4-115">Remarks</span></span>

<span data-ttu-id="98ef4-116">는 자체가 아닌의 비트 수에 비례하여 시간을 사용 `power` `power` 합니다.</span><span class="sxs-lookup"><span data-stu-id="98ef4-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>