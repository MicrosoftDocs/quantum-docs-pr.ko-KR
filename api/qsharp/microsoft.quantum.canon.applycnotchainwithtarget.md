---
uid: Microsoft.Quantum.Canon.ApplyCNOTChainWithTarget
title: ApplyCNOTChainWithTarget 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChainWithTarget
qsharp.summary: Computes the parity of an array of qubits into a target qubit.
ms.openlocfilehash: fd0a0f3e1db89946aec2c63f3cde7a021608eea5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718364"
---
# <a name="applycnotchainwithtarget-operation"></a><span data-ttu-id="df3fd-102">ApplyCNOTChainWithTarget 작업</span><span class="sxs-lookup"><span data-stu-id="df3fd-102">ApplyCNOTChainWithTarget operation</span></span>

<span data-ttu-id="df3fd-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="df3fd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="df3fd-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="df3fd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="df3fd-105">대상 비트의 배열에 대 한 패리티를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="df3fd-105">Computes the parity of an array of qubits into a target qubit.</span></span>

```qsharp
operation ApplyCNOTChainWithTarget (qubits : Qubit[], targetQubit : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="df3fd-106">Description</span><span class="sxs-lookup"><span data-stu-id="df3fd-106">Description</span></span>

<span data-ttu-id="df3fd-107">배열이 처음에 $ \ket{q_0} \ket{q_1} \cdots q_ {\text{target}}} $ 상태에 있는 경우, 최종 상태는 $ \ket{q_0} \ket{q_1 \cdots q_0} \cdots \text{target}}} q_ {n-1} \cdots \co\o q_0 \cdots {$로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df3fd-107">If the array is initially in the state $\ket{q_0} \ket{q_1} \cdots \ket{q_{\text{target}}}$, the final state is given by $\ket{q_0} \ket{q_1 \oplus q_0} \cdots \ket{q_{n - 1} \oplus \cdots \oplus q_0 \oplus q_{\text{target}}}$.</span></span>

## <a name="input"></a><span data-ttu-id="df3fd-108">입력</span><span class="sxs-lookup"><span data-stu-id="df3fd-108">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="df3fd-109">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="df3fd-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="df3fd-110">패리티를 계산 하는 데 사용할 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="df3fd-110">Array of qubits on which the parity is computed.</span></span>


### <a name="targetqubit--qubit"></a><span data-ttu-id="df3fd-111">Targetbit [:](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="df3fd-111">targetQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="df3fd-112">'가 중 비트 '의 패리티가 XORed 하는 마지막입니다.</span><span class="sxs-lookup"><span data-stu-id="df3fd-112">Final qubit into which the parity of 'qubits' is XORed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="df3fd-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="df3fd-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="df3fd-114">설명</span><span class="sxs-lookup"><span data-stu-id="df3fd-114">Remarks</span></span>

<span data-ttu-id="df3fd-115">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="df3fd-115">The following are equivalent:</span></span>

```qsharp
ApplyCNOTChainWithTarget(Most(qs), Last(qs));
```

<span data-ttu-id="df3fd-116">및</span><span class="sxs-lookup"><span data-stu-id="df3fd-116">and</span></span>

```qsharp
ApplyCNOTChain(qs);
```