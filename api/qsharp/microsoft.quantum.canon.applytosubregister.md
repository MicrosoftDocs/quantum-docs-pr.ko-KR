---
uid: Microsoft.Quantum.Canon.ApplyToSubregister
title: ApplyToSubregister 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregister
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices.
ms.openlocfilehash: c9181b8962d36b20f7a9140eb7aaef11aee7faa0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717032"
---
# <a name="applytosubregister-operation"></a><span data-ttu-id="5bcb0-102">ApplyToSubregister 작업</span><span class="sxs-lookup"><span data-stu-id="5bcb0-102">ApplyToSubregister operation</span></span>

<span data-ttu-id="5bcb0-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5bcb0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5bcb0-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5bcb0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5bcb0-105">인스턴스의 하위 레지스터에 작업을 적용 합니다. 여기서는 해당 인덱스의 배열에 지정 된 것과 같은 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bcb0-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>

```qsharp
operation ApplyToSubregister (op : (Qubit[] => Unit), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="5bcb0-106">입력</span><span class="sxs-lookup"><span data-stu-id="5bcb0-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="5bcb0-107">op:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5bcb0-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5bcb0-108">Subregister에 적용할 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="5bcb0-108">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="5bcb0-109">idxs: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5bcb0-109">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="5bcb0-110">작업을 적용 하는 데 사용할 작업을 나타내는 인덱스의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5bcb0-110">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="5bcb0-111">target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5bcb0-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5bcb0-112">작업이 수행 되는 등록입니다.</span><span class="sxs-lookup"><span data-stu-id="5bcb0-112">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5bcb0-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5bcb0-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="5bcb0-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5bcb0-114">See Also</span></span>

- [<span data-ttu-id="5bcb0-115">ApplyToSubregisterA입니다.</span><span class="sxs-lookup"><span data-stu-id="5bcb0-115">Microsoft.Quantum.Canon.ApplyToSubregisterA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterA)
- [<span data-ttu-id="5bcb0-116">Microsoft. 양자. ApplyToSubregisterC</span><span class="sxs-lookup"><span data-stu-id="5bcb0-116">Microsoft.Quantum.Canon.ApplyToSubregisterC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterC)
- [<span data-ttu-id="5bcb0-117">Microsoft. 양자. ApplyToSubregisterCA</span><span class="sxs-lookup"><span data-stu-id="5bcb0-117">Microsoft.Quantum.Canon.ApplyToSubregisterCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterCA)