---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterA
title: RestrictedToSubregisterA 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: d45c43caed35df8fb89d9d38e540faf5a21ea064
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715534"
---
# <a name="restrictedtosubregistera-function"></a><span data-ttu-id="9a23a-102">RestrictedToSubregisterA 함수</span><span class="sxs-lookup"><span data-stu-id="9a23a-102">RestrictedToSubregisterA function</span></span>

<span data-ttu-id="9a23a-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9a23a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9a23a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9a23a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9a23a-105">작업을 레지스터의 인덱스 배열, 즉 subregister로 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a23a-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>
<span data-ttu-id="9a23a-106">한정자는 `A` 작업이 adjointable를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9a23a-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
function RestrictedToSubregisterA (op : (Qubit[] => Unit is Adj), idxs : Int[]) : (Qubit[] => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="9a23a-107">입력</span><span class="sxs-lookup"><span data-stu-id="9a23a-107">Input</span></span>

### <a name="op--qubit--unit-adj"></a><span data-ttu-id="9a23a-108">op: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9a23a-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="9a23a-109">Subregister로 제한 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="9a23a-109">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="9a23a-110">idxs: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="9a23a-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="9a23a-111">작업을 제한할 비트를 나타내는 인덱스의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9a23a-111">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit-adj"></a><span data-ttu-id="9a23a-112">출력: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9a23a-112">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>



## <a name="see-also"></a><span data-ttu-id="9a23a-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9a23a-113">See Also</span></span>

- [<span data-ttu-id="9a23a-114">RestrictedToSubregister입니다.</span><span class="sxs-lookup"><span data-stu-id="9a23a-114">Microsoft.Quantum.Canon.RestrictedToSubregister</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)