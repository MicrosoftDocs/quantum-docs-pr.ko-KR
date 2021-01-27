---
uid: Microsoft.Quantum.Canon.ApplyToPartition
title: ApplyToPartition 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartition
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts.
ms.openlocfilehash: a0dc3453e7501816132569869e858418d5f3f4e5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850549"
---
# <a name="applytopartition-operation"></a><span data-ttu-id="f3d55-102">ApplyToPartition 작업</span><span class="sxs-lookup"><span data-stu-id="f3d55-102">ApplyToPartition operation</span></span>

<span data-ttu-id="f3d55-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f3d55-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f3d55-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f3d55-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f3d55-105">지정 된 레지스터 파티션에 작업 쌍을 두 부분으로 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d55-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>

```qsharp
operation ApplyToPartition (op : ((Qubit[], Qubit[]) => Unit), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="f3d55-106">입력</span><span class="sxs-lookup"><span data-stu-id="f3d55-106">Input</span></span>

### <a name="op--qubitqubit--unit"></a><span data-ttu-id="f3d55-107">op: (이상[비트](xref:microsoft.quantum.lang-ref.qubit)[[], [](xref:microsoft.quantum.lang-ref.qubit)]) => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f3d55-107">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="f3d55-108">지정 된 파티션에 적용할 작업 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="f3d55-108">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="f3d55-109">numberOfQubitsToFirstArgument: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f3d55-109">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f3d55-110">파티션의 첫 번째 부분에 배치할 대상의 요소 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f3d55-110">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="f3d55-111">나머지는 파티션의 두 번째 부분을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d55-111">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="f3d55-112">target: [](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f3d55-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f3d55-113">지정 된 두 작업을 통해 분할 되 고 작동 하는 나머지 비트의 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="f3d55-113">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f3d55-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f3d55-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="f3d55-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f3d55-115">See Also</span></span>

- [<span data-ttu-id="f3d55-116">ApplyToPartitionA입니다.</span><span class="sxs-lookup"><span data-stu-id="f3d55-116">Microsoft.Quantum.Canon.ApplyToPartitionA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartitionA)
- [<span data-ttu-id="f3d55-117">ApplyToPartitionC입니다.</span><span class="sxs-lookup"><span data-stu-id="f3d55-117">Microsoft.Quantum.Canon.ApplyToPartitionC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartitionC)
- [<span data-ttu-id="f3d55-118">ApplyToPartitionCA입니다.</span><span class="sxs-lookup"><span data-stu-id="f3d55-118">Microsoft.Quantum.Canon.ApplyToPartitionCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartitionCA)