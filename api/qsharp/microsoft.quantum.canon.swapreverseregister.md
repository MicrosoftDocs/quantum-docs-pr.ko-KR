---
uid: Microsoft.Quantum.Canon.SwapReverseRegister
title: SwapReverseRegister 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: SwapReverseRegister
qsharp.summary: Uses SWAP gates to Reversed the order of the qubits in a register.
ms.openlocfilehash: ca553670719c7cfff84f2eedad8cbc16189e0e98
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852067"
---
# <a name="swapreverseregister-operation"></a><span data-ttu-id="a8804-102">SwapReverseRegister 작업</span><span class="sxs-lookup"><span data-stu-id="a8804-102">SwapReverseRegister operation</span></span>

<span data-ttu-id="a8804-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a8804-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a8804-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a8804-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a8804-105">에서는 교환 게이트를 사용 하 여 레지스터에서의 비트 순서를 반대로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="a8804-105">Uses SWAP gates to Reversed the order of the qubits in a register.</span></span>

```qsharp
operation SwapReverseRegister (register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a8804-106">입력</span><span class="sxs-lookup"><span data-stu-id="a8804-106">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="a8804-107">register: [](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a8804-107">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a8804-108">바꾸기 게이트를 사용 하 여 되돌려야 하는의 비트 순서</span><span class="sxs-lookup"><span data-stu-id="a8804-108">The qubits order of which should be reversed using SWAP gates</span></span>



## <a name="output--unit"></a><span data-ttu-id="a8804-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a8804-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

