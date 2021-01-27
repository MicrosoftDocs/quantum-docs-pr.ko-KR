---
uid: Microsoft.Quantum.Preparation.PrepareQubit
title: PrepareQubit 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareQubit
qsharp.summary: >-
  > [!WARNING]

  > PrepareQubit has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate> instead.


  Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.

  If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).

  If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.
ms.openlocfilehash: e6a88ccf4c01b2f0a7344e3823b2748790cf9650
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854328"
---
# <a name="preparequbit-operation"></a><span data-ttu-id="92bf7-102">PrepareQubit 작업</span><span class="sxs-lookup"><span data-stu-id="92bf7-102">PrepareQubit operation</span></span>

<span data-ttu-id="92bf7-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="92bf7-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="92bf7-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="92bf7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="92bf7-105">PrepareQubit는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92bf7-105">PrepareQubit has been deprecated.</span></span> <span data-ttu-id="92bf7-106">대신 <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate>를 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="92bf7-106">Please use <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate> instead.</span></span>

<span data-ttu-id="92bf7-107">`Zero`지정 된 Pauli 연산자의 + 1 () eigenstate에서 eibit를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="92bf7-107">Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator.</span></span>
<span data-ttu-id="92bf7-108">Id 연산자가 지정 된 경우에는 최대 혼합 된 상태에서 해당 비트를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="92bf7-108">If the identity operator is given, then the qubit is prepared in the maximally mixed state.</span></span>

<span data-ttu-id="92bf7-109">이 작업은 처음에 $ \ket $ 상태에 있는 경우 {0} 이 작업을 통해 지정 된 Pauli 연산자의 $ + $1 eigenstate 또는의 최대 mixed 상태 ()에 대 한 추가 비트를 준비 `PauliI` 합니다 (참조 <xref:microsoft.quantum.preparation.preparesinglequbitidentity> ).</span><span class="sxs-lookup"><span data-stu-id="92bf7-109">If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).</span></span>

<span data-ttu-id="92bf7-110">이 연산은 $ \ket $ 이외의 상태에 있는 경우 {0} 다음 게이트를 적용 합니다. $H $ for `PauliX` , $HS $ for `PauliY` , $I $ for `PauliZ` 및 <xref:microsoft.quantum.preparation.preparesinglequbitidentity> `PauliI`</span><span class="sxs-lookup"><span data-stu-id="92bf7-110">If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.</span></span>

```qsharp
operation PrepareQubit (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="92bf7-111">입력</span><span class="sxs-lookup"><span data-stu-id="92bf7-111">Input</span></span>

### <a name="basis--pauli"></a><span data-ttu-id="92bf7-112">기준: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="92bf7-112">basis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="92bf7-113">Pauli 연산자 $P $.</span><span class="sxs-lookup"><span data-stu-id="92bf7-113">A Pauli operator $P$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="92bf7-114">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="92bf7-114">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="92bf7-115">준비할 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="92bf7-115">A qubit to be prepared.</span></span>



## <a name="output--unit"></a><span data-ttu-id="92bf7-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="92bf7-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

