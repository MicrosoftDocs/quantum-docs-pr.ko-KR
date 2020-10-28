---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterCA
title: ApplyToSubregisterCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterCA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 3eb210debf8980f057ed150f647d545f68734459
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716990"
---
# <a name="applytosubregisterca-operation"></a><span data-ttu-id="eab7c-102">ApplyToSubregisterCA 작업</span><span class="sxs-lookup"><span data-stu-id="eab7c-102">ApplyToSubregisterCA operation</span></span>

<span data-ttu-id="eab7c-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="eab7c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="eab7c-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="eab7c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="eab7c-105">인스턴스의 하위 레지스터에 작업을 적용 합니다. 여기서는 해당 인덱스의 배열에 지정 된 것과 같은 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="eab7c-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="eab7c-106">한정자는 `CA` 작업을 제어 하 고 adjointable 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eab7c-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToSubregisterCA (op : (Qubit[] => Unit is Ctl + Adj), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="eab7c-107">입력</span><span class="sxs-lookup"><span data-stu-id="eab7c-107">Input</span></span>

### <a name="op--qubit--unit-ctl--adj"></a><span data-ttu-id="eab7c-108">op: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl +</span><span class="sxs-lookup"><span data-stu-id="eab7c-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="eab7c-109">Subregister에 적용할 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="eab7c-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="eab7c-110">idxs: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="eab7c-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="eab7c-111">작업을 적용 하는 데 사용할 작업을 나타내는 인덱스의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="eab7c-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="eab7c-112">target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="eab7c-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="eab7c-113">작업이 수행 되는 등록입니다.</span><span class="sxs-lookup"><span data-stu-id="eab7c-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eab7c-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eab7c-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="eab7c-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="eab7c-115">See Also</span></span>

- [<span data-ttu-id="eab7c-116">Microsoft. 양자. ApplyToSubregister</span><span class="sxs-lookup"><span data-stu-id="eab7c-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)