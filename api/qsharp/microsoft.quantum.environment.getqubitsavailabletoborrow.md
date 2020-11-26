---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: GetQubitsAvailableToBorrow 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow.
ms.openlocfilehash: 30b97c2b6e1353f008d085c3bae6160763557c67
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201464"
---
# <a name="getqubitsavailabletoborrow-operation"></a><span data-ttu-id="1047f-102">GetQubitsAvailableToBorrow 작업</span><span class="sxs-lookup"><span data-stu-id="1047f-102">GetQubitsAvailableToBorrow operation</span></span>

<span data-ttu-id="1047f-103">네임 스페이스: [Microsoft 퀀텀. 환경](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="1047f-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="1047f-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="1047f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="1047f-105">현재 사용할 수 있는 데 사용할 수 있는 고 비트 수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1047f-105">Returns the number of qubits currently available to borrow.</span></span>

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a><span data-ttu-id="1047f-106">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1047f-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1047f-107">사용할 수 있으며 문의 일부로 할당 되지 않는 원하는 비트 수입니다 `borrowing` .</span><span class="sxs-lookup"><span data-stu-id="1047f-107">The number of qubits that could be borrowed and won't be allocated as part of a `borrowing` statement.</span></span>
<span data-ttu-id="1047f-108">사용 중인 대상 컴퓨터에서이 정보를 제공 하지 않으면이 `-1` 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1047f-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="1047f-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1047f-109">See Also</span></span>

- [<span data-ttu-id="1047f-110">GetQubitsAvailableToUse.</span><span class="sxs-lookup"><span data-stu-id="1047f-110">Microsoft.Quantum.Environment.GetQubitsAvailableToUse</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)