---
uid: Microsoft.Quantum.Canon.ApplyLowDepthAnd
title: ApplyLowDepthAnd 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyLowDepthAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, with T-depth 1, using measurement to perform the adjoint operation.
ms.openlocfilehash: 092a350e42d8d90942de13530fefd761b5187e1d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717984"
---
# <a name="applylowdepthand-operation"></a><span data-ttu-id="32da0-102">ApplyLowDepthAnd 작업</span><span class="sxs-lookup"><span data-stu-id="32da0-102">ApplyLowDepthAnd operation</span></span>

<span data-ttu-id="32da0-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="32da0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="32da0-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="32da0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="32da0-105">지정 된 대상 값을 반전 합니다. 두 컨트롤이 모두 1 상태에 있는 경우에만 T-수준 1을 사용 하 여 adjoint 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="32da0-105">Inverts a given target qubit if and only if both control qubits are in the 1 state, with T-depth 1, using measurement to perform the adjoint operation.</span></span>

```qsharp
operation ApplyLowDepthAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="32da0-106">Description</span><span class="sxs-lookup"><span data-stu-id="32da0-106">Description</span></span>

<span data-ttu-id="32da0-107">`target`두 컨트롤이 모두 1 인 경우에만를 반전 하지만는 `target` 상태 0 이라고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32da0-107">Inverts `target` if and only if both controls are 1, but assumes that `target` is in state 0.</span></span>  <span data-ttu-id="32da0-108">작업은 T-수 4, T-깊이 1을 사용 하 고 하나의 도우미를 필요로 하며, 따라서 `target` 가 0으로 알려진 경우 CCNOT 연산에 더 적합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32da0-108">The operation has T-count 4, T-depth 1 and requires one helper qubit, and may therefore be preferable to a CCNOT operation, if `target` is known to be 0.</span></span>  <span data-ttu-id="32da0-109">이 작업의 adjoint는 측정을 기반으로 하며, T 게이트는 없으며 도우미를 사용 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32da0-109">The adjoint of this operation is measurement based and requires no T gates, and no helper qubit.</span></span>

## <a name="input"></a><span data-ttu-id="32da0-110">입력</span><span class="sxs-lookup"><span data-stu-id="32da0-110">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="32da0-111">control1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="32da0-111">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="32da0-112">첫 번째 제어 비트</span><span class="sxs-lookup"><span data-stu-id="32da0-112">First control qubit</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="32da0-113">control2: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="32da0-113">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="32da0-114">두 번째 제어 비트</span><span class="sxs-lookup"><span data-stu-id="32da0-114">Second control qubit</span></span>


### <a name="target--qubit"></a><span data-ttu-id="32da0-115">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="32da0-115">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="32da0-116">대상 보조 비트 상태 0 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32da0-116">Target auxiliary qubit; must be in state 0</span></span>



## <a name="output--unit"></a><span data-ttu-id="32da0-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="32da0-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="32da0-118">참조</span><span class="sxs-lookup"><span data-stu-id="32da0-118">References</span></span>

- <span data-ttu-id="32da0-119">Cody Jones: "내결함성 Toffoli 게이트 Novel 생성", Phys 87, 022328, 2013 [Arxiv: 1212.5069](https://arxiv.org/abs/1212.5069) doi: 10.1103/PhysRevA. 87.022328</span><span class="sxs-lookup"><span data-stu-id="32da0-119">Cody Jones: "Novel constructions for the fault-tolerant Toffoli gate", Phys. Rev. A 87, 022328, 2013 [arXiv:1212.5069](https://arxiv.org/abs/1212.5069) doi:10.1103/PhysRevA.87.022328</span></span>
- <span data-ttu-id="32da0-120">Peter Selinger: "T-depth one의 퀀텀 회로", Phys 87, 042302, 2013 [Arxiv: 1210.0974](https://arxiv.org/abs/1210.0974) doi: 10.1103/PhysRevA. 87.042302</span><span class="sxs-lookup"><span data-stu-id="32da0-120">Peter Selinger: "Quantum circuits of T-depth one", Phys. Rev. A 87, 042302, 2013 [arXiv:1210.0974](https://arxiv.org/abs/1210.0974) doi:10.1103/PhysRevA.87.042302</span></span>