---
uid: Microsoft.Quantum.Synthesis.MaskToQubitsPair
title: MaskToQubitsPair 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: MaskToQubitsPair
qsharp.summary: Transform mask of control and target bits to a pair of control qubits and target qubits
ms.openlocfilehash: fed196a2f2b64dae9f34f399477db14740af6f8a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855380"
---
# <a name="masktoqubitspair-function"></a><span data-ttu-id="f4314-102">MaskToQubitsPair 함수</span><span class="sxs-lookup"><span data-stu-id="f4314-102">MaskToQubitsPair function</span></span>

<span data-ttu-id="f4314-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="f4314-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="f4314-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f4314-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f4314-105">컨트롤 및 대상 비트의 마스크를 컨트롤의 비트와 대상 비트의 쌍으로 변환</span><span class="sxs-lookup"><span data-stu-id="f4314-105">Transform mask of control and target bits to a pair of control qubits and target qubits</span></span>

```qsharp
function MaskToQubitsPair (qubits : Qubit[], mask : Microsoft.Quantum.Synthesis.MCMTMask) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="f4314-106">입력</span><span class="sxs-lookup"><span data-stu-id="f4314-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="f4314-107">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f4314-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="mask--mcmtmask"></a><span data-ttu-id="f4314-108">마스크: [Mcmtmask](xref:Microsoft.Quantum.Synthesis.MCMTMask)</span><span class="sxs-lookup"><span data-stu-id="f4314-108">mask : [MCMTMask](xref:Microsoft.Quantum.Synthesis.MCMTMask)</span></span>





## <a name="output--qubitqubit"></a><span data-ttu-id="f4314-109">Output[: ((),](xref:microsoft.quantum.lang-ref.qubit)[[], [](xref:microsoft.quantum.lang-ref.qubit)])</span><span class="sxs-lookup"><span data-stu-id="f4314-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

