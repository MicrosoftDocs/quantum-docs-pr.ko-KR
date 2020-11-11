---
uid: Microsoft.Quantum.Intrinsic.R
title: R 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R
qsharp.summary: >-
  Applies a rotation about the given Pauli axis.

  \begin{align} R_{\mu}(\theta) \mathrel{:=} e^{-i \theta \sigma_{\mu} / 2}, \end{align} where $\mu \in \{I, X, Y, Z\}$.
ms.openlocfilehash: 7d1d51031f4587b1c501feab459e614fc1530457
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720932"
---
# <a name="r-operation"></a><span data-ttu-id="6df02-102">R 작업</span><span class="sxs-lookup"><span data-stu-id="6df02-102">R operation</span></span>

<span data-ttu-id="6df02-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="6df02-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="6df02-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6df02-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6df02-105">지정 된 Pauli 축에 대 한 회전을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6df02-105">Applies a rotation about the given Pauli axis.</span></span>

<span data-ttu-id="6df02-106">\begin{align} R_ {\mu} (\ 테타) \mathrel{: =} e ^ {-i \theta \ sigma_ {\mu}/2}, \end{align} where $ \theta \theta \{ i, X, Y, Z \} $.</span><span class="sxs-lookup"><span data-stu-id="6df02-106">\begin{align} R_{\mu}(\theta) \mathrel{:=} e^{-i \theta \sigma_{\mu} / 2}, \end{align} where $\mu \in \{I, X, Y, Z\}$.</span></span>

```qsharp
operation R (pauli : Pauli, theta : Double, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="6df02-107">입력</span><span class="sxs-lookup"><span data-stu-id="6df02-107">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="6df02-108">pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="6df02-108">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="6df02-109">Pauli 연산자 ($ \mu $)를 지수화 하 여 회전을 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6df02-109">Pauli operator ($\mu$) to be exponentiated to form the rotation.</span></span>


### <a name="theta--double"></a><span data-ttu-id="6df02-110">테타: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6df02-110">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6df02-111">해당 하는 비트를 회전할 각도입니다.</span><span class="sxs-lookup"><span data-stu-id="6df02-111">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="6df02-112">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="6df02-112">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="6df02-113">게이트가 적용 되어야 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="6df02-113">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6df02-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6df02-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="6df02-115">설명</span><span class="sxs-lookup"><span data-stu-id="6df02-115">Remarks</span></span>

<span data-ttu-id="6df02-116">을 사용 하 여 호출 되 `pauli = PauliI` 는 경우이 작업은 *글로벌 단계* 를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6df02-116">When called with `pauli = PauliI`, this operation applies a *global phase* .</span></span> <span data-ttu-id="6df02-117">이 단계는 함수에서 사용 하는 경우 중요할 수 있습니다 `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="6df02-117">This phase can be significant when used with the `Controlled` functor.</span></span>