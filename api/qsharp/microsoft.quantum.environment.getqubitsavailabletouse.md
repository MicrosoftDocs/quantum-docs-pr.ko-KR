---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: GetQubitsAvailableToUse 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: 25d43d369193fc7453fd5ce9c50769c438a69afb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712580"
---
# <a name="getqubitsavailabletouse-operation"></a><span data-ttu-id="0a939-102">GetQubitsAvailableToUse 작업</span><span class="sxs-lookup"><span data-stu-id="0a939-102">GetQubitsAvailableToUse operation</span></span>

<span data-ttu-id="0a939-103">네임 스페이스: [Microsoft 퀀텀. 환경](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="0a939-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="0a939-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0a939-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0a939-105">현재 사용할 수 있는 범위의 비트 수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a939-105">Returns the number of qubits currently available to use.</span></span>

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a><span data-ttu-id="0a939-106">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0a939-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0a939-107">문에 할당 될 수 있는 값입니다 `using` .</span><span class="sxs-lookup"><span data-stu-id="0a939-107">The number of qubits that could be allocated in a `using` statement.</span></span>
<span data-ttu-id="0a939-108">사용 중인 대상 컴퓨터에서이 정보를 제공 하지 않으면이 `-1` 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a939-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a939-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0a939-109">See Also</span></span>

- [<span data-ttu-id="0a939-110">GetQubitsAvailableToBorrow.</span><span class="sxs-lookup"><span data-stu-id="0a939-110">Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)