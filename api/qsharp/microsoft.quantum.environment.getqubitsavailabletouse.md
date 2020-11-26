---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: GetQubitsAvailableToUse 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: ce461b03a08b4c83b9de142c957ce5c590fe9659
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201413"
---
# <a name="getqubitsavailabletouse-operation"></a><span data-ttu-id="980f4-102">GetQubitsAvailableToUse 작업</span><span class="sxs-lookup"><span data-stu-id="980f4-102">GetQubitsAvailableToUse operation</span></span>

<span data-ttu-id="980f4-103">네임 스페이스: [Microsoft 퀀텀. 환경](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="980f4-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="980f4-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="980f4-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="980f4-105">현재 사용할 수 있는 범위의 비트 수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="980f4-105">Returns the number of qubits currently available to use.</span></span>

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a><span data-ttu-id="980f4-106">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="980f4-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="980f4-107">문에 할당 될 수 있는 값입니다 `using` .</span><span class="sxs-lookup"><span data-stu-id="980f4-107">The number of qubits that could be allocated in a `using` statement.</span></span>
<span data-ttu-id="980f4-108">사용 중인 대상 컴퓨터에서이 정보를 제공 하지 않으면이 `-1` 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="980f4-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="980f4-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="980f4-109">See Also</span></span>

- [<span data-ttu-id="980f4-110">GetQubitsAvailableToBorrow.</span><span class="sxs-lookup"><span data-stu-id="980f4-110">Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)