---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: GetQubitsAvailableToBorrow 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow. This includes unused qubits; that is, this includes the qubits returned by `GetQubitsAvailableToUse`.
ms.openlocfilehash: cb56ce4aefd7a03c0f0827b8d34688ef17988f56
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712587"
---
# <a name="getqubitsavailabletoborrow-operation"></a><span data-ttu-id="0a8ec-102">GetQubitsAvailableToBorrow 작업</span><span class="sxs-lookup"><span data-stu-id="0a8ec-102">GetQubitsAvailableToBorrow operation</span></span>

<span data-ttu-id="0a8ec-103">네임 스페이스: [Microsoft 퀀텀. 환경](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="0a8ec-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="0a8ec-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0a8ec-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0a8ec-105">현재 사용할 수 있는 데 사용할 수 있는 고 비트 수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a8ec-105">Returns the number of qubits currently available to borrow.</span></span>
<span data-ttu-id="0a8ec-106">사용 되지 않은 비트를 포함 합니다. 즉,에 의해 반환 되는의 비트를 포함 `GetQubitsAvailableToUse` 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a8ec-106">This includes unused qubits; that is, this includes the qubits returned by `GetQubitsAvailableToUse`.</span></span>

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a><span data-ttu-id="0a8ec-107">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0a8ec-107">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0a8ec-108">문에 할당 될 수 있는 값입니다 `borrowing` .</span><span class="sxs-lookup"><span data-stu-id="0a8ec-108">The number of qubits that could be allocated in a `borrowing` statement.</span></span>
<span data-ttu-id="0a8ec-109">사용 중인 대상 컴퓨터에서이 정보를 제공 하지 않으면이 `-1` 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a8ec-109">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a8ec-110">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0a8ec-110">See Also</span></span>

- [<span data-ttu-id="0a8ec-111">GetQubitsAvailableToUse.</span><span class="sxs-lookup"><span data-stu-id="0a8ec-111">Microsoft.Quantum.Environment.GetQubitsAvailableToUse</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)