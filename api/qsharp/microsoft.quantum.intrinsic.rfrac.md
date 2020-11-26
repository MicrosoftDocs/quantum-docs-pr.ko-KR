---
uid: Microsoft.Quantum.Intrinsic.RFrac
title: RFrac 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: RFrac
qsharp.summary: >-
  Applies a rotation about the given Pauli axis by an angle specified as a dyadic fraction.

  \begin{align} R_{\mu}(n, k) \mathrel{:=} e^{i \pi n \sigma_{\mu} / 2^k}, \end{align} where $\mu \in \{I, X, Y, Z\}$.

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r".
ms.openlocfilehash: bd182ea50d747e07bb0f8051c5dbc128b7ff7674
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198642"
---
# <a name="rfrac-operation"></a><span data-ttu-id="ef799-102">RFrac 작업</span><span class="sxs-lookup"><span data-stu-id="ef799-102">RFrac operation</span></span>

<span data-ttu-id="ef799-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="ef799-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="ef799-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ef799-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ef799-105">Dyadic 분수로 지정 된 각도 만큼 지정 된 Pauli 축에 대 한 회전을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef799-105">Applies a rotation about the given Pauli axis by an angle specified as a dyadic fraction.</span></span>

<span data-ttu-id="ef799-106">\begin{align} R_ {\mu} (n, k) \mathrel{: =} e ^ {i \pi n \ sigma_ {\mu}/2 ^ k}, \end{align} where $ \pi \pi \{ i, X, Y, Z \} $.</span><span class="sxs-lookup"><span data-stu-id="ef799-106">\begin{align} R_{\mu}(n, k) \mathrel{:=} e^{i \pi n \sigma_{\mu} / 2^k}, \end{align} where $\mu \in \{I, X, Y, Z\}$.</span></span>

> [!WARNING]
> <span data-ttu-id="ef799-107">이 작업에서는의 **반대** 서명 규칙을 사용 @"microsoft.quantum.intrinsic.r" 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef799-107">This operation uses the **opposite** sign convention from @"microsoft.quantum.intrinsic.r".</span></span>

```qsharp
operation RFrac (pauli : Pauli, numerator : Int, power : Int, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="ef799-108">입력</span><span class="sxs-lookup"><span data-stu-id="ef799-108">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="ef799-109">pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="ef799-109">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="ef799-110">지수화 하 여 회전을 형성 하는 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="ef799-110">Pauli operator to be exponentiated to form the rotation.</span></span>


### <a name="numerator--int"></a><span data-ttu-id="ef799-111">분자: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ef799-111">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ef799-112">Dyadic 분수를 회전 하는 각도를 나타내는 분자입니다.</span><span class="sxs-lookup"><span data-stu-id="ef799-112">Numerator in the dyadic fraction representation of the angle by which the qubit is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="ef799-113">power: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ef799-113">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ef799-114">제곱 비트를 회전할 각도의 분모를 지정 하는 2의 거듭제곱입니다.</span><span class="sxs-lookup"><span data-stu-id="ef799-114">Power of two specifying the denominator of the angle by which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="ef799-115">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ef799-115">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ef799-116">게이트가 적용 되어야 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="ef799-116">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ef799-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ef799-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ef799-118">설명</span><span class="sxs-lookup"><span data-stu-id="ef799-118">Remarks</span></span>

<span data-ttu-id="ef799-119">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef799-119">Equivalent to:</span></span>

```qsharp
// PI() is a Q# function that returns an approximation of π.
R(pauli, -PI() * IntAsDouble(numerator) / IntAsDouble(2 ^ (power - 1)), qubit);
```