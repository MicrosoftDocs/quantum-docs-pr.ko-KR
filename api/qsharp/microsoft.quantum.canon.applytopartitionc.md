---
uid: Microsoft.Quantum.Canon.ApplyToPartitionC
title: ApplyToPartitionC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionC
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 840c93c653d71af1a82fb0dc51d9e056176ba88b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717116"
---
# <a name="applytopartitionc-operation"></a><span data-ttu-id="9098f-102">ApplyToPartitionC 작업</span><span class="sxs-lookup"><span data-stu-id="9098f-102">ApplyToPartitionC operation</span></span>

<span data-ttu-id="9098f-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9098f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9098f-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9098f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9098f-105">지정 된 레지스터 파티션에 작업 쌍을 두 부분으로 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9098f-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>
<span data-ttu-id="9098f-106">한정자는 `C` 작업을 제어할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9098f-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToPartitionC (op : ((Qubit[], Qubit[]) => Unit is Ctl), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="9098f-107">입력</span><span class="sxs-lookup"><span data-stu-id="9098f-107">Input</span></span>

### <a name="op--qubitqubit--unit-ctl"></a><span data-ttu-id="9098f-108">op[: ((), [](xref:microsoft.quantum.lang-ref.qubit)][, [](xref:microsoft.quantum.lang-ref.qubit)]) => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="9098f-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="9098f-109">지정 된 파티션에 적용할 작업 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="9098f-109">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="9098f-110">numberOfQubitsToFirstArgument: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9098f-110">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9098f-111">파티션의 첫 번째 부분에 배치할 대상의 요소 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9098f-111">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="9098f-112">나머지는 파티션의 두 번째 부분을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9098f-112">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="9098f-113">target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9098f-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9098f-114">지정 된 두 작업을 통해 분할 되 고 작동 하는 나머지 비트의 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="9098f-114">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9098f-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9098f-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="9098f-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9098f-116">See Also</span></span>

- [<span data-ttu-id="9098f-117">ApplyToPartition입니다.</span><span class="sxs-lookup"><span data-stu-id="9098f-117">Microsoft.Quantum.Canon.ApplyToPartition</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartition)