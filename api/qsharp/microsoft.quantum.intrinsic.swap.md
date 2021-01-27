---
uid: Microsoft.Quantum.Intrinsic.SWAP
title: 교환 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: SWAP
qsharp.summary: >-
  Applies the SWAP gate to a pair of qubits.

  \begin{align} \operatorname{SWAP} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: 4d8d037404ac835a1dd032790e7fd03f29591c41
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849265"
---
# <a name="swap-operation"></a><span data-ttu-id="12649-102">교환 작업</span><span class="sxs-lookup"><span data-stu-id="12649-102">SWAP operation</span></span>

<span data-ttu-id="12649-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="12649-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="12649-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="12649-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="12649-105">교환 게이트를 다양 한 쌍에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="12649-105">Applies the SWAP gate to a pair of qubits.</span></span>

<span data-ttu-id="12649-106">\begin{align} \operatorname{SWAP} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 0 & 1 & 0 & \\ \\ 0 \\ \\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}</span><span class="sxs-lookup"><span data-stu-id="12649-106">\begin{align} \operatorname{SWAP} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}</span></span>

<span data-ttu-id="12649-107">여기에서 행과 열은 퀀텀 개념 가이드에서로 정렬 됩니다.</span><span class="sxs-lookup"><span data-stu-id="12649-107">where rows and columns are ordered as in the quantum concepts guide.</span></span>

```qsharp
operation SWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="12649-108">입력</span><span class="sxs-lookup"><span data-stu-id="12649-108">Input</span></span>

### <a name="qubit1--qubit"></a><span data-ttu-id="12649-109">qubit1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="12649-109">qubit1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="12649-110">교환할 첫 번째 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="12649-110">First qubit to be swapped.</span></span>


### <a name="qubit2--qubit"></a><span data-ttu-id="12649-111">qubit2: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="12649-111">qubit2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="12649-112">스왑할 두 번째 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="12649-112">Second qubit to be swapped.</span></span>



## <a name="output--unit"></a><span data-ttu-id="12649-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="12649-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="12649-114">설명</span><span class="sxs-lookup"><span data-stu-id="12649-114">Remarks</span></span>

<span data-ttu-id="12649-115">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="12649-115">Equivalent to:</span></span>

```qsharp
CNOT(qubit1, qubit2);
CNOT(qubit2, qubit1);
CNOT(qubit1, qubit2);
```