---
uid: Microsoft.Quantum.Intrinsic.CNOT
title: CNOT 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CNOT
qsharp.summary: >-
  Applies the controlled-NOT (CNOT) gate to a pair of qubits.

  \begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: 90e84f7d0ea7373498632474dfafa23335f0c78e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198979"
---
# <a name="cnot-operation"></a><span data-ttu-id="f0867-102">CNOT 작업</span><span class="sxs-lookup"><span data-stu-id="f0867-102">CNOT operation</span></span>

<span data-ttu-id="f0867-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="f0867-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="f0867-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="f0867-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="f0867-105">제어 되지 않는 (CNOT) 게이트를 한 쌍의 비트에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0867-105">Applies the controlled-NOT (CNOT) gate to a pair of qubits.</span></span>

<span data-ttu-id="f0867-106">\begin{align} \operatorname{CNOT} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 0 & 0 & 0 & 1 0 & 0 & \\ \\ \\ \\ 1 & 0 \end{bmatrix}, \end{align}</span><span class="sxs-lookup"><span data-stu-id="f0867-106">\begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}</span></span>

<span data-ttu-id="f0867-107">여기에서 행과 열은 퀀텀 개념 가이드에서로 정렬 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0867-107">where rows and columns are ordered as in the quantum concepts guide.</span></span>

```qsharp
operation CNOT (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="f0867-108">입력</span><span class="sxs-lookup"><span data-stu-id="f0867-108">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="f0867-109">제어: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f0867-109">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f0867-110">CNOT gate의 비트를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0867-110">Control qubit for the CNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="f0867-111">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f0867-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f0867-112">CNOT gate의 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="f0867-112">Target qubit for the CNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f0867-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f0867-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f0867-114">설명</span><span class="sxs-lookup"><span data-stu-id="f0867-114">Remarks</span></span>

<span data-ttu-id="f0867-115">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0867-115">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```