---
uid: Microsoft.Quantum.Canon.ApplyToSubregister
title: ApplyToSubregister 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregister
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices.
ms.openlocfilehash: be820c87ee19230713d6c3e5681bbe3678040e95
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850482"
---
# <a name="applytosubregister-operation"></a><span data-ttu-id="97201-102">ApplyToSubregister 작업</span><span class="sxs-lookup"><span data-stu-id="97201-102">ApplyToSubregister operation</span></span>

<span data-ttu-id="97201-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="97201-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="97201-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="97201-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="97201-105">인스턴스의 하위 레지스터에 작업을 적용 합니다. 여기서는 해당 인덱스의 배열에 지정 된 것과 같은 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="97201-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>

```qsharp
operation ApplyToSubregister (op : (Qubit[] => Unit), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="97201-106">입력</span><span class="sxs-lookup"><span data-stu-id="97201-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="97201-107">op:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="97201-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="97201-108">Subregister에 적용할 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="97201-108">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="97201-109">idxs: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="97201-109">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="97201-110">작업을 적용 하는 데 사용할 작업을 나타내는 인덱스의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="97201-110">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="97201-111">target: [](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="97201-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="97201-112">작업이 수행 되는 등록입니다.</span><span class="sxs-lookup"><span data-stu-id="97201-112">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="97201-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="97201-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="97201-114">예</span><span class="sxs-lookup"><span data-stu-id="97201-114">Example</span></span>

<span data-ttu-id="97201-115">3 개의 stbit 상태 $ \frac {1} {\sqrt {2} } \ket {0} \_ 2 (\ket {0} \_ 1 \ k {0} _3 + \ket {1} \_ 1 \ k {1} _3) $:</span><span class="sxs-lookup"><span data-stu-id="97201-115">Create three qubit state $\frac{1}{\sqrt{2}}\ket{0}\_2(\ket{0}\_1\ket{0}_3+\ket{1}\_1\ket{1}_3)$:</span></span>

```qsharp
    using (register = Qubit[3]) {
        ApplyToSubregister(Exp([PauliX,PauliY],PI() / 4.0,_), [1,3], register);
    }
```

## <a name="see-also"></a><span data-ttu-id="97201-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="97201-116">See Also</span></span>

- [<span data-ttu-id="97201-117">ApplyToSubregisterA입니다.</span><span class="sxs-lookup"><span data-stu-id="97201-117">Microsoft.Quantum.Canon.ApplyToSubregisterA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterA)
- [<span data-ttu-id="97201-118">Microsoft. 양자. ApplyToSubregisterC</span><span class="sxs-lookup"><span data-stu-id="97201-118">Microsoft.Quantum.Canon.ApplyToSubregisterC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterC)
- [<span data-ttu-id="97201-119">Microsoft. 양자. ApplyToSubregisterCA</span><span class="sxs-lookup"><span data-stu-id="97201-119">Microsoft.Quantum.Canon.ApplyToSubregisterCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterCA)