---
uid: Microsoft.Quantum.Intrinsic.CNOT
title: CNOT 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CNOT
qsharp.summary: >-
  Applies the controlled-NOT (CNOT) gate to a pair of qubits.

  \begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: 02ae795c785dcbc25b56ac513a9237540e57ea63
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849433"
---
# <a name="cnot-operation"></a><span data-ttu-id="faf95-102">CNOT 작업</span><span class="sxs-lookup"><span data-stu-id="faf95-102">CNOT operation</span></span>

<span data-ttu-id="faf95-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="faf95-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="faf95-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="faf95-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="faf95-105">제어 되지 않는 (CNOT) 게이트를 한 쌍의 비트에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf95-105">Applies the controlled-NOT (CNOT) gate to a pair of qubits.</span></span>

<span data-ttu-id="faf95-106">\begin{align} \operatorname{CNOT} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 0 & 0 & 0 & 1 0 & 0 & \\ \\ \\ \\ 1 & 0 \end{bmatrix}, \end{align}</span><span class="sxs-lookup"><span data-stu-id="faf95-106">\begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}</span></span>

<span data-ttu-id="faf95-107">여기에서 행과 열은 퀀텀 개념 가이드에서로 정렬 됩니다.</span><span class="sxs-lookup"><span data-stu-id="faf95-107">where rows and columns are ordered as in the quantum concepts guide.</span></span>

```qsharp
operation CNOT (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="faf95-108">입력</span><span class="sxs-lookup"><span data-stu-id="faf95-108">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="faf95-109">제어: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="faf95-109">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="faf95-110">CNOT gate의 비트를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf95-110">Control qubit for the CNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="faf95-111">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="faf95-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="faf95-112">CNOT gate의 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="faf95-112">Target qubit for the CNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="faf95-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="faf95-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="faf95-114">설명</span><span class="sxs-lookup"><span data-stu-id="faf95-114">Remarks</span></span>

<span data-ttu-id="faf95-115">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf95-115">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```