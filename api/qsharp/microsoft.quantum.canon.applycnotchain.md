---
uid: Microsoft.Quantum.Canon.ApplyCNOTChain
title: ApplyCNOTChain 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChain
qsharp.summary: Computes the parity of a register of qubits in-place.
ms.openlocfilehash: c98fe24ca352952162acb7a9c4fc93d5da4285b8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718376"
---
# <a name="applycnotchain-operation"></a><span data-ttu-id="5eec9-102">ApplyCNOTChain 작업</span><span class="sxs-lookup"><span data-stu-id="5eec9-102">ApplyCNOTChain operation</span></span>

<span data-ttu-id="5eec9-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5eec9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5eec9-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5eec9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5eec9-105">내부에서의 레지스터 패리티를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eec9-105">Computes the parity of a register of qubits in-place.</span></span>

```qsharp
operation ApplyCNOTChain (qubits : Qubit[]) : Unit
```


## <a name="description"></a><span data-ttu-id="5eec9-106">Description</span><span class="sxs-lookup"><span data-stu-id="5eec9-106">Description</span></span>

<span data-ttu-id="5eec9-107">이 작업을 수행 하면 해당 입력의 상태가 $ $ \begin{align} \ket{q_0} \ket{q_1} \cdots} q_ {n-1}} & \maps\ket{q_0} \ket{q_0 \cdots} \ket{q_1 \cdots q_0 \cdots q_1} \cdots q_2 \cdots \co\o {n-1}}로 변환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5eec9-107">This operation transforms the state of its input as $$ \begin{align} \ket{q_0} \ket{q_1} \cdots \ket{q_{n - 1}} & \mapsto \ket{q_0} \ket{q_0 \oplus q_1} \ket{q_0 \oplus q_1 \oplus q_2} \cdots \ket{q_0 \oplus \cdots \oplus q_{n - 1}}.</span></span>
<span data-ttu-id="5eec9-108">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="5eec9-108">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="5eec9-109">입력</span><span class="sxs-lookup"><span data-stu-id="5eec9-109">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="5eec9-110">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5eec9-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5eec9-111">패리티를 계산 하 고 저장 하는 데 사용할 수 있는 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5eec9-111">Array of qubits whose parity is to be computed and stored.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5eec9-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5eec9-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

