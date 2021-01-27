---
uid: Microsoft.Quantum.Canon.ApplyCNOTChainWithTarget
title: ApplyCNOTChainWithTarget 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChainWithTarget
qsharp.summary: Computes the parity of an array of qubits into a target qubit.
ms.openlocfilehash: ba1a4e99c411a4718b5a09fdcd57a7239eb4dbd6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845128"
---
# <a name="applycnotchainwithtarget-operation"></a><span data-ttu-id="bb730-102">ApplyCNOTChainWithTarget 작업</span><span class="sxs-lookup"><span data-stu-id="bb730-102">ApplyCNOTChainWithTarget operation</span></span>

<span data-ttu-id="bb730-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bb730-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bb730-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bb730-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bb730-105">대상 비트의 배열에 대 한 패리티를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb730-105">Computes the parity of an array of qubits into a target qubit.</span></span>

```qsharp
operation ApplyCNOTChainWithTarget (qubits : Qubit[], targetQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="bb730-106">설명</span><span class="sxs-lookup"><span data-stu-id="bb730-106">Description</span></span>

<span data-ttu-id="bb730-107">배열이 처음에 $ \ket{q_0} \ket{q_1} \cdots q_ {\text{target}}} $ 상태에 있는 경우, 최종 상태는 $ \ket{q_0} \ket{q_1 \cdots q_0} \cdots \text{target}}} q_ {n-1} \cdots \co\o q_0 \cdots {$로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb730-107">If the array is initially in the state $\ket{q_0} \ket{q_1} \cdots \ket{q_{\text{target}}}$, the final state is given by $\ket{q_0} \ket{q_1 \oplus q_0} \cdots \ket{q_{n - 1} \oplus \cdots \oplus q_0 \oplus q_{\text{target}}}$.</span></span>

## <a name="input"></a><span data-ttu-id="bb730-108">입력</span><span class="sxs-lookup"><span data-stu-id="bb730-108">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="bb730-109">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="bb730-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="bb730-110">패리티를 계산 하는 데 사용할 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="bb730-110">Array of qubits on which the parity is computed.</span></span>


### <a name="targetqubit--qubit"></a><span data-ttu-id="bb730-111">Targetbit [:](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="bb730-111">targetQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="bb730-112">'가 중 비트 '의 패리티가 XORed 하는 마지막입니다.</span><span class="sxs-lookup"><span data-stu-id="bb730-112">Final qubit into which the parity of 'qubits' is XORed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bb730-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bb730-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="bb730-114">설명</span><span class="sxs-lookup"><span data-stu-id="bb730-114">Remarks</span></span>

<span data-ttu-id="bb730-115">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb730-115">The following are equivalent:</span></span>

```qsharp
ApplyCNOTChainWithTarget(Most(qs), Last(qs));
```

<span data-ttu-id="bb730-116">및</span><span class="sxs-lookup"><span data-stu-id="bb730-116">and</span></span>

```qsharp
ApplyCNOTChain(qs);
```