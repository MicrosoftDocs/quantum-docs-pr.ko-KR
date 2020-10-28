---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterC
title: ApplyToSubregisterC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterC
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: ba5be1e7e822197eb76aac029be8617a70d51ddb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717004"
---
# <a name="applytosubregisterc-operation"></a><span data-ttu-id="a93ea-102">ApplyToSubregisterC 작업</span><span class="sxs-lookup"><span data-stu-id="a93ea-102">ApplyToSubregisterC operation</span></span>

<span data-ttu-id="a93ea-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a93ea-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a93ea-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a93ea-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a93ea-105">인스턴스의 하위 레지스터에 작업을 적용 합니다. 여기서는 해당 인덱스의 배열에 지정 된 것과 같은 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a93ea-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="a93ea-106">한정자는 `C` 작업을 제어할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a93ea-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToSubregisterC (op : (Qubit[] => Unit is Ctl), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="a93ea-107">입력</span><span class="sxs-lookup"><span data-stu-id="a93ea-107">Input</span></span>

### <a name="op--qubit--unit-ctl"></a><span data-ttu-id="a93ea-108">op:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="a93ea-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="a93ea-109">Subregister에 적용할 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a93ea-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="a93ea-110">idxs: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="a93ea-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="a93ea-111">작업을 적용 하는 데 사용할 작업을 나타내는 인덱스의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="a93ea-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="a93ea-112">target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a93ea-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a93ea-113">작업이 수행 되는 등록입니다.</span><span class="sxs-lookup"><span data-stu-id="a93ea-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a93ea-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a93ea-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="a93ea-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a93ea-115">See Also</span></span>

- [<span data-ttu-id="a93ea-116">Microsoft. 양자. ApplyToSubregister</span><span class="sxs-lookup"><span data-stu-id="a93ea-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)