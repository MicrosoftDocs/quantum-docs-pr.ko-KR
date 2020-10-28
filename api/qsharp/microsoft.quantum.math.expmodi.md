---
uid: Microsoft.Quantum.Math.ExpModI
title: 예기치 않은 Modi 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModI
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: e31273702a9850d0162f160ca412ff6d50f38b28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723364"
---
# <a name="expmodi-function"></a><span data-ttu-id="1cfdc-102">예기치 않은 Modi 함수</span><span class="sxs-lookup"><span data-stu-id="1cfdc-102">ExpModI function</span></span>

<span data-ttu-id="1cfdc-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="1cfdc-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="1cfdc-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1cfdc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1cfdc-105">지정 된 모듈러스와 관련 하 여 지정 된 지 수 만큼 거듭제곱 한 정수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModI (expBase : Int, power : Int, modulus : Int) : Int
```


## <a name="description"></a><span data-ttu-id="1cfdc-106">Description</span><span class="sxs-lookup"><span data-stu-id="1cfdc-106">Description</span></span>

<span data-ttu-id="1cfdc-107">$X $, power by $p $ 및 모듈러스를 $N $로 하 여이를 기반으로 하는 것을 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="1cfdc-108">함수는 $x ^ p \operatorname{mod} N $을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="1cfdc-109">$N $, $x $는 양수가 고 전원은 음수가 아닌 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="1cfdc-110">입력</span><span class="sxs-lookup"><span data-stu-id="1cfdc-110">Input</span></span>

### <a name="expbase--int"></a><span data-ttu-id="1cfdc-111">기본: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1cfdc-111">expBase : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="power--int"></a><span data-ttu-id="1cfdc-112">power: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1cfdc-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="modulus--int"></a><span data-ttu-id="1cfdc-113">모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1cfdc-113">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--int"></a><span data-ttu-id="1cfdc-114">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1cfdc-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="remarks"></a><span data-ttu-id="1cfdc-115">설명</span><span class="sxs-lookup"><span data-stu-id="1cfdc-115">Remarks</span></span>

<span data-ttu-id="1cfdc-116">는 자체가 아닌의 비트 수에 비례하여 시간을 사용 `power` `power` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>