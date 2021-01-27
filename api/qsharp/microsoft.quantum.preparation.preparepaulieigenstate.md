---
uid: Microsoft.Quantum.Preparation.PreparePauliEigenstate
title: PreparePauliEigenstate 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PreparePauliEigenstate
qsharp.summary: Prepares a qubit in the positive eigenstate of a given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.
ms.openlocfilehash: 473bb2fa4429a14f69bcae4573354aad87dc37df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854351"
---
# <a name="preparepaulieigenstate-operation"></a><span data-ttu-id="d655f-102">PreparePauliEigenstate 작업</span><span class="sxs-lookup"><span data-stu-id="d655f-102">PreparePauliEigenstate operation</span></span>

<span data-ttu-id="d655f-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="d655f-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="d655f-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d655f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d655f-105">지정 된 Pauli 연산자의 긍정 eigenstate에서 원하는 비트를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="d655f-105">Prepares a qubit in the positive eigenstate of a given Pauli operator.</span></span>
<span data-ttu-id="d655f-106">Id 연산자가 지정 된 경우에는 최대 혼합 된 상태에서 해당 비트를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="d655f-106">If the identity operator is given, then the qubit is prepared in the maximally mixed state.</span></span>

```qsharp
operation PreparePauliEigenstate (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="d655f-107">설명</span><span class="sxs-lookup"><span data-stu-id="d655f-107">Description</span></span>

<span data-ttu-id="d655f-108">이 작업은 처음에 $ \ket $ 상태에 있는 경우 {0} 이 작업을 통해 지정 된 Pauli 연산자의 $ + $1 eigenstate 또는의 최대 mixed 상태 ()에 대 한 추가 비트를 준비 `PauliI` 합니다 (참조 <xref:microsoft.quantum.preparation.preparesinglequbitidentity> ).</span><span class="sxs-lookup"><span data-stu-id="d655f-108">If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).</span></span>

<span data-ttu-id="d655f-109">이 연산은 $ \ket $ 이외의 상태에 있는 경우 {0} 다음 게이트를 적용 합니다. $H $ for `PauliX` , $HS $ for `PauliY` , $I $ for `PauliZ` 및 <xref:microsoft.quantum.preparation.preparesinglequbitidentity> `PauliI`</span><span class="sxs-lookup"><span data-stu-id="d655f-109">If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.</span></span>

## <a name="input"></a><span data-ttu-id="d655f-110">입력</span><span class="sxs-lookup"><span data-stu-id="d655f-110">Input</span></span>

### <a name="basis--pauli"></a><span data-ttu-id="d655f-111">기준: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="d655f-111">basis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="d655f-112">Pauli 연산자 $P $.</span><span class="sxs-lookup"><span data-stu-id="d655f-112">A Pauli operator $P$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="d655f-113">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d655f-113">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d655f-114">준비할 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="d655f-114">A qubit to be prepared.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d655f-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d655f-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="d655f-116">예</span><span class="sxs-lookup"><span data-stu-id="d655f-116">Example</span></span>

<span data-ttu-id="d655f-117">$ \Ket{+} $ 상태에서이를 준비 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d655f-117">To prepare a qubit in the $\ket{+}$ state:</span></span>

```qsharp
using (q = Qubit()) {
    PreparePauliEigenstate(PauliX, qubit);
    // ...
}
```