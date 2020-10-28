---
uid: Microsoft.Quantum.Canon.RestrictedToSubregister
title: RestrictedToSubregister 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregister
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister.
ms.openlocfilehash: a8b599035de6fede10bdaf8cef17f2124a59f064
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715541"
---
# <a name="restrictedtosubregister-function"></a><span data-ttu-id="b99e4-102">RestrictedToSubregister 함수</span><span class="sxs-lookup"><span data-stu-id="b99e4-102">RestrictedToSubregister function</span></span>

<span data-ttu-id="b99e4-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b99e4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b99e4-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b99e4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b99e4-105">작업을 레지스터의 인덱스 배열, 즉 subregister로 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="b99e4-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>

```qsharp
function RestrictedToSubregister (op : (Qubit[] => Unit), idxs : Int[]) : (Qubit[] => Unit)
```


## <a name="input"></a><span data-ttu-id="b99e4-106">입력</span><span class="sxs-lookup"><span data-stu-id="b99e4-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="b99e4-107">op:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b99e4-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b99e4-108">Subregister로 제한 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="b99e4-108">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="b99e4-109">idxs: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="b99e4-109">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="b99e4-110">작업을 제한할 비트를 나타내는 인덱스의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="b99e4-110">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit"></a><span data-ttu-id="b99e4-111">출력:가 중 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b99e4-111">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 



## <a name="see-also"></a><span data-ttu-id="b99e4-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b99e4-112">See Also</span></span>

- [<span data-ttu-id="b99e4-113">RestrictedToSubregisterA입니다.</span><span class="sxs-lookup"><span data-stu-id="b99e4-113">Microsoft.Quantum.Canon.RestrictedToSubregisterA</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterA)
- [<span data-ttu-id="b99e4-114">RestrictedToSubregisterC입니다.</span><span class="sxs-lookup"><span data-stu-id="b99e4-114">Microsoft.Quantum.Canon.RestrictedToSubregisterC</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterC)
- [<span data-ttu-id="b99e4-115">RestrictedToSubregisterCA입니다.</span><span class="sxs-lookup"><span data-stu-id="b99e4-115">Microsoft.Quantum.Canon.RestrictedToSubregisterCA</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterCA)