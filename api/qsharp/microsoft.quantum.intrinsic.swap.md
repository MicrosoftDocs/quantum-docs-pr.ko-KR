---
uid: Microsoft.Quantum.Intrinsic.SWAP
title: 교환 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: SWAP
qsharp.summary: >-
  Applies the SWAP gate to a pair of qubits.

  \begin{align} \operatorname{SWAP} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: 18b910741e9d0883fc5fcd025eb647407c823269
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719996"
---
# <a name="swap-operation"></a><span data-ttu-id="df4a5-102">교환 작업</span><span class="sxs-lookup"><span data-stu-id="df4a5-102">SWAP operation</span></span>

<span data-ttu-id="df4a5-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="df4a5-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="df4a5-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="df4a5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="df4a5-105">교환 게이트를 다양 한 쌍에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="df4a5-105">Applies the SWAP gate to a pair of qubits.</span></span>

<span data-ttu-id="df4a5-106">\begin{align} \operatorname{SWAP} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 0 & 1 & 0 & \\ \\ 0 \\ \\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}</span><span class="sxs-lookup"><span data-stu-id="df4a5-106">\begin{align} \operatorname{SWAP} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}</span></span>

<span data-ttu-id="df4a5-107">여기에서 행과 열은 퀀텀 개념 가이드에서로 정렬 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df4a5-107">where rows and columns are ordered as in the quantum concepts guide.</span></span>

```qsharp
operation SWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="df4a5-108">입력</span><span class="sxs-lookup"><span data-stu-id="df4a5-108">Input</span></span>

### <a name="qubit1--qubit"></a><span data-ttu-id="df4a5-109">qubit1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="df4a5-109">qubit1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="df4a5-110">교환할 첫 번째 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="df4a5-110">First qubit to be swapped.</span></span>


### <a name="qubit2--qubit"></a><span data-ttu-id="df4a5-111">qubit2: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="df4a5-111">qubit2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="df4a5-112">스왑할 두 번째 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="df4a5-112">Second qubit to be swapped.</span></span>



## <a name="output--unit"></a><span data-ttu-id="df4a5-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="df4a5-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="df4a5-114">설명</span><span class="sxs-lookup"><span data-stu-id="df4a5-114">Remarks</span></span>

<span data-ttu-id="df4a5-115">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="df4a5-115">Equivalent to:</span></span>

```qsharp
CNOT(qubit1, qubit2);
CNOT(qubit2, qubit1);
CNOT(qubit1, qubit2);
```