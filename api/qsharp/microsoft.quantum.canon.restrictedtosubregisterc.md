---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterC
title: RestrictedToSubregisterC 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterC
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 2ca32cf8c85f33f498a30f71833b3dd69db6da6e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715513"
---
# <a name="restrictedtosubregisterc-function"></a><span data-ttu-id="9057e-102">RestrictedToSubregisterC 함수</span><span class="sxs-lookup"><span data-stu-id="9057e-102">RestrictedToSubregisterC function</span></span>

<span data-ttu-id="9057e-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9057e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9057e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9057e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9057e-105">작업을 레지스터의 인덱스 배열, 즉 subregister로 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="9057e-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>
<span data-ttu-id="9057e-106">한정자는 `C` 작업을 제어할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9057e-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
function RestrictedToSubregisterC (op : (Qubit[] => Unit is Ctl), idxs : Int[]) : (Qubit[] => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="9057e-107">입력</span><span class="sxs-lookup"><span data-stu-id="9057e-107">Input</span></span>

### <a name="op--qubit--unit-ctl"></a><span data-ttu-id="9057e-108">op:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="9057e-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="9057e-109">Subregister로 제한 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="9057e-109">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="9057e-110">idxs: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="9057e-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="9057e-111">작업을 제한할 비트를 나타내는 인덱스의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9057e-111">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit-ctl"></a><span data-ttu-id="9057e-112">출력:가 중 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="9057e-112">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>



## <a name="see-also"></a><span data-ttu-id="9057e-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9057e-113">See Also</span></span>

- [<span data-ttu-id="9057e-114">RestrictedToSubregister입니다.</span><span class="sxs-lookup"><span data-stu-id="9057e-114">Microsoft.Quantum.Canon.RestrictedToSubregister</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)