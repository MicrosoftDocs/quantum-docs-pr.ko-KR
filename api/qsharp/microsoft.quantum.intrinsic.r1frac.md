---
uid: Microsoft.Quantum.Intrinsic.R1Frac
title: R1Frac 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1Frac
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by an angle specified as a dyadic fraction.

  \begin{align} R_1(n, k) \mathrel{:=} \operatorname{diag}(1, e^{i \pi k / 2^n}). \end{align}

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r", and does not include the > factor of $1/ 2$ included by @"microsoft.quantum.intrinsic.r1".
ms.openlocfilehash: bfa6cd60eebd05feec8cfa2bf71e09dc0d02843a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720901"
---
# <a name="r1frac-operation"></a><span data-ttu-id="e578c-102">R1Frac 작업</span><span class="sxs-lookup"><span data-stu-id="e578c-102">R1Frac operation</span></span>

<span data-ttu-id="e578c-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="e578c-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="e578c-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e578c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e578c-105">Dyadic 분수로 지정 된 각도로 $ \ket $ 상태에 대 한 회전을 적용 {1} 합니다.</span><span class="sxs-lookup"><span data-stu-id="e578c-105">Applies a rotation about the $\ket{1}$ state by an angle specified as a dyadic fraction.</span></span>

<span data-ttu-id="e578c-106">\begin{align} R_1 (n, k) \mathrel{: =} \operatorname{diag} (1, e ^ {i \pi k/2 ^ n}).</span><span class="sxs-lookup"><span data-stu-id="e578c-106">\begin{align} R_1(n, k) \mathrel{:=} \operatorname{diag}(1, e^{i \pi k / 2^n}).</span></span>
<span data-ttu-id="e578c-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="e578c-107">\end{align}</span></span>

> [!WARNING]
> <span data-ttu-id="e578c-108">이 작업은에서 **반대** 부호 규칙을 사용 @"microsoft.quantum.intrinsic.r" 하며에 포함 된 $1/2 $의 요소를 포함 하지 않습니다 @"microsoft.quantum.intrinsic.r1" .</span><span class="sxs-lookup"><span data-stu-id="e578c-108">This operation uses the **opposite** sign convention from @"microsoft.quantum.intrinsic.r", and does not include the factor of $1/ 2$ included by @"microsoft.quantum.intrinsic.r1".</span></span>

```qsharp
operation R1Frac (numerator : Int, power : Int, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="e578c-109">입력</span><span class="sxs-lookup"><span data-stu-id="e578c-109">Input</span></span>

### <a name="numerator--int"></a><span data-ttu-id="e578c-110">분자: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e578c-110">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e578c-111">Dyadic 분수를 회전 하는 각도를 나타내는 분자입니다.</span><span class="sxs-lookup"><span data-stu-id="e578c-111">Numerator in the dyadic fraction representation of the angle by which the qubit is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="e578c-112">power: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e578c-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e578c-113">제곱 비트를 회전할 각도의 분모를 지정 하는 2의 거듭제곱입니다.</span><span class="sxs-lookup"><span data-stu-id="e578c-113">Power of two specifying the denominator of the angle by which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="e578c-114">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e578c-114">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e578c-115">게이트가 적용 되어야 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="e578c-115">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e578c-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e578c-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e578c-117">설명</span><span class="sxs-lookup"><span data-stu-id="e578c-117">Remarks</span></span>

<span data-ttu-id="e578c-118">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="e578c-118">Equivalent to:</span></span>

```qsharp
RFrac(PauliZ, -numerator, denominator + 1, qubit);
RFrac(PauliI, numerator, denominator + 1, qubit);
```