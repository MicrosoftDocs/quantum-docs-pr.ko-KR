---
uid: Microsoft.Quantum.Diagnostics.DumpOperation
title: DumpOperation 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpOperation
qsharp.summary: Given an operation, displays diagnostics about the operation that are made available by the current execution target.
ms.openlocfilehash: 444d42e2440b30b3bdf50d55a399568bed063222
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712860"
---
# <a name="dumpoperation-operation"></a><span data-ttu-id="5bc89-102">DumpOperation 작업</span><span class="sxs-lookup"><span data-stu-id="5bc89-102">DumpOperation operation</span></span>

<span data-ttu-id="5bc89-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="5bc89-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="5bc89-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5bc89-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5bc89-105">작업을 수행 하는 경우 현재 실행 대상에서 사용할 수 있는 작업에 대 한 진단을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc89-105">Given an operation, displays diagnostics about the operation that are made available by the current execution target.</span></span>

```qsharp
operation DumpOperation (nQubits : Int, op : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="5bc89-106">입력</span><span class="sxs-lookup"><span data-stu-id="5bc89-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="5bc89-107">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5bc89-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5bc89-108">지정 된 작업이 작동 하는 값의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc89-108">The number of qubits on which the given operation acts.</span></span>


### <a name="op--qubit--unit-adj"></a><span data-ttu-id="5bc89-109">op: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5bc89-109">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="5bc89-110">진단할 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc89-110">The operation that is to be diagnosed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5bc89-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5bc89-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5bc89-112">설명</span><span class="sxs-lookup"><span data-stu-id="5bc89-112">Remarks</span></span>

<span data-ttu-id="5bc89-113">이 작업을 호출 하면 Q # 내에서 관찰할 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc89-113">Calling this operation has no observable effect from within Q#.</span></span> <span data-ttu-id="5bc89-114">표시 되는 정확한 진단 (있는 경우)은 현재 실행 대상 및 편집기 환경에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="5bc89-114">The exact diagnostics that are displayed, if any, are dependent on the current execution target and editor environment.</span></span>
<span data-ttu-id="5bc89-115">예를 들어 전체 상태 퀀텀 시뮬레이터에서 사용 되는 경우를 나타내는 데 사용 되는 단일 매트릭스가 `op` 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bc89-115">For example, when used on the full-state quantum simulator, a unitary matrix used to represent `op` is displayed.</span></span>

<span data-ttu-id="5bc89-116">전역 단계 모호성을 허용 하는 시뮬레이터에서 실행 하는 경우 (예: 전체 상태 시뮬레이터) 반환 된 표현은 글로벌 단계까지 달라질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc89-116">Note that, when run on simulators that admit a global phase ambiguity (e.g.: the full-state simulator), returned representations may vary up to a global phase.</span></span>

<span data-ttu-id="5bc89-117">마찬가지로 행 및 열 행렬 표현의 순서 지정은이 작업을 지 원하는 각 시뮬레이터에서 사용 되는 규칙에 따라 달라질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc89-117">Similarly, the ordering of rows and columns matrix representations may vary with the conventions used by each simulator supporting this operation.</span></span>