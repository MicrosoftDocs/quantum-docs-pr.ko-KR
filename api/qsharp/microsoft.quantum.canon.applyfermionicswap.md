---
uid: Microsoft.Quantum.Canon.ApplyFermionicSWAP
title: ApplyFermionicSWAP 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyFermionicSWAP
qsharp.summary: Applies the Fermionic SWAP.
ms.openlocfilehash: 0c470705843a6360df0a72374570d86571397e41
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218804"
---
# <a name="applyfermionicswap-operation"></a><span data-ttu-id="cea6d-102">ApplyFermionicSWAP 작업</span><span class="sxs-lookup"><span data-stu-id="cea6d-102">ApplyFermionicSWAP operation</span></span>

<span data-ttu-id="cea6d-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cea6d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cea6d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cea6d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cea6d-105">Fermionic SWAP을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cea6d-105">Applies the Fermionic SWAP.</span></span>

```qsharp
operation ApplyFermionicSWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="cea6d-106">Description</span><span class="sxs-lookup"><span data-stu-id="cea6d-106">Description</span></span>

<span data-ttu-id="cea6d-107">이렇게 하면 기본적으로-1의 글로벌 단계를 적용 하는 동안 두 번째 비트는 모두 1이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cea6d-107">This essentially swaps the qubits while applying a global phase of -1 if both qubits are 1s.</span></span> <span data-ttu-id="cea6d-108">Orbitals의 symmetrization을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="cea6d-108">Preserves anti-symmetrization of orbitals.</span></span>
<span data-ttu-id="cea6d-109">자세한 내용은  항목을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cea6d-109">See  for more information.</span></span>

<span data-ttu-id="cea6d-110">이 작업은 단일 연산자 \begin{align} f_ {swap} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 0 & 1 & 0 & 0 0 & 0 & 0 \\ \\ \\ \\ &-1 \\ \\ \end{bmatrix}.에 의해 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cea6d-110">This operation is represented by the unitary operator \begin{align} f_{swap} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -1 \\\\ \end{bmatrix}.</span></span>
<span data-ttu-id="cea6d-111">\end{align}</span><span class="sxs-lookup"><span data-stu-id="cea6d-111">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="cea6d-112">입력</span><span class="sxs-lookup"><span data-stu-id="cea6d-112">Input</span></span>

### <a name="qubit1--qubit"></a><span data-ttu-id="cea6d-113">qubit1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="cea6d-113">qubit1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="cea6d-114">교환할 첫 번째 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="cea6d-114">The first qubit to be swapped.</span></span>


### <a name="qubit2--qubit"></a><span data-ttu-id="cea6d-115">qubit2: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="cea6d-115">qubit2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="cea6d-116">스왑할 두 번째 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="cea6d-116">The second qubit to be swapped.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cea6d-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cea6d-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="cea6d-118">참조 항목</span><span class="sxs-lookup"><span data-stu-id="cea6d-118">References</span></span>

- [<span data-ttu-id="cea6d-119">*Ryan Babbush, 네, Wiebe, Jarrod McClean, James McClain, Hartmut Neven, Garnet Kin-Lic 변경 (*, arxiv: 1706.00023</span><span class="sxs-lookup"><span data-stu-id="cea6d-119"> *Ryan Babbush, Nathan Wiebe, Jarrod McClean, James McClain, Hartmut Neven, Garnet Kin-Lic Chan*, arXiv:1706.00023 </span></span>](https://arxiv.org/pdf/1706.00023.pdf)

## <a name="see-also"></a><span data-ttu-id="cea6d-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cea6d-120">See Also</span></span>

- [<span data-ttu-id="cea6d-121">Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cea6d-121">Microsoft.Quantum.Intrinsic.SWAP</span></span>](xref:Microsoft.Quantum.Intrinsic.SWAP)