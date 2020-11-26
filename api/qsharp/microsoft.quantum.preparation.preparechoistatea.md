---
uid: Microsoft.Quantum.Preparation.PrepareChoiStateA
title: PrepareChoiStateA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiStateA
qsharp.summary: Prepares the Choi–Jamiołkowski state for a given operation with an adjoint variant onto given reference and target registers.
ms.openlocfilehash: 59d47a549a6e2a208906b79504ea93bd9ebaabd7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230126"
---
# <a name="preparechoistatea-operation"></a><span data-ttu-id="33c03-102">PrepareChoiStateA 작업</span><span class="sxs-lookup"><span data-stu-id="33c03-102">PrepareChoiStateA operation</span></span>

<span data-ttu-id="33c03-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="33c03-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="33c03-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="33c03-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="33c03-105">지정 된 참조 및 대상 레지스터에 대해 adjoint variant를 사용 하 여 지정 된 작업에 대 한 Choi – Jamiołkowski 상태를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="33c03-105">Prepares the Choi–Jamiołkowski state for a given operation with an adjoint variant onto given reference and target registers.</span></span>

```qsharp
operation PrepareChoiStateA (op : (Qubit[] => Unit is Adj), reference : Qubit[], target : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="33c03-106">입력</span><span class="sxs-lookup"><span data-stu-id="33c03-106">Input</span></span>

### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="33c03-107">op: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is</span><span class="sxs-lookup"><span data-stu-id="33c03-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="reference--qubit"></a><span data-ttu-id="33c03-108">참조:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="33c03-108">reference : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="33c03-109">target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="33c03-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="33c03-110">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="33c03-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="33c03-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="33c03-111">See Also</span></span>

- [<span data-ttu-id="33c03-112">PrepareChoiState.</span><span class="sxs-lookup"><span data-stu-id="33c03-112">Microsoft.Quantum.Preparation.PrepareChoiState</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiState)