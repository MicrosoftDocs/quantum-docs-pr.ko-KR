---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterCA
title: RestrictedToSubregisterCA 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterCA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: e81193a85451b72a69a595fa81a9fb07f3038c22
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715527"
---
# <a name="restrictedtosubregisterca-function"></a><span data-ttu-id="dda2b-102">RestrictedToSubregisterCA 함수</span><span class="sxs-lookup"><span data-stu-id="dda2b-102">RestrictedToSubregisterCA function</span></span>

<span data-ttu-id="dda2b-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="dda2b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="dda2b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dda2b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dda2b-105">작업을 레지스터의 인덱스 배열, 즉 subregister로 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda2b-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>
<span data-ttu-id="dda2b-106">한정자는 `CA` 작업을 제어 하 고 adjointable 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dda2b-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
function RestrictedToSubregisterCA (op : (Qubit[] => Unit is Adj + Ctl), idxs : Int[]) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="dda2b-107">입력</span><span class="sxs-lookup"><span data-stu-id="dda2b-107">Input</span></span>

### <a name="op--qubit--unit-adj--ctl"></a><span data-ttu-id="dda2b-108">op: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="dda2b-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="dda2b-109">Subregister로 제한 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="dda2b-109">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="dda2b-110">idxs: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="dda2b-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="dda2b-111">작업을 제한할 비트를 나타내는 인덱스의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="dda2b-111">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="dda2b-112">출력: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="dda2b-112">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>



## <a name="see-also"></a><span data-ttu-id="dda2b-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="dda2b-113">See Also</span></span>

- [<span data-ttu-id="dda2b-114">RestrictedToSubregister입니다.</span><span class="sxs-lookup"><span data-stu-id="dda2b-114">Microsoft.Quantum.Canon.RestrictedToSubregister</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)