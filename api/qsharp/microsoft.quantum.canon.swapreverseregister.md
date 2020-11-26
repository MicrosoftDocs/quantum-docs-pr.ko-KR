---
uid: Microsoft.Quantum.Canon.SwapReverseRegister
title: SwapReverseRegister 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: SwapReverseRegister
qsharp.summary: Uses SWAP gates to Reversed the order of the qubits in a register.
ms.openlocfilehash: 9df62c4ef97a186b274a62bd493fa9e7bbb74fa1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204983"
---
# <a name="swapreverseregister-operation"></a><span data-ttu-id="b6f8f-102">SwapReverseRegister 작업</span><span class="sxs-lookup"><span data-stu-id="b6f8f-102">SwapReverseRegister operation</span></span>

<span data-ttu-id="b6f8f-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b6f8f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b6f8f-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b6f8f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b6f8f-105">에서는 교환 게이트를 사용 하 여 레지스터에서의 비트 순서를 반대로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-105">Uses SWAP gates to Reversed the order of the qubits in a register.</span></span>

```qsharp
operation SwapReverseRegister (register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="b6f8f-106">입력</span><span class="sxs-lookup"><span data-stu-id="b6f8f-106">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="b6f8f-107">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b6f8f-107">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b6f8f-108">바꾸기 게이트를 사용 하 여 되돌려야 하는의 비트 순서</span><span class="sxs-lookup"><span data-stu-id="b6f8f-108">The qubits order of which should be reversed using SWAP gates</span></span>



## <a name="output--unit"></a><span data-ttu-id="b6f8f-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b6f8f-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

