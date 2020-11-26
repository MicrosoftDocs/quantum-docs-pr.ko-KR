---
uid: Microsoft.Quantum.Canon.ApplyAnd
title: ApplyAnd 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, using measurement to perform the adjoint operation.
ms.openlocfilehash: b749013584c89273375da002ac36b3575085b7f2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219297"
---
# <a name="applyand-operation"></a><span data-ttu-id="a4220-102">ApplyAnd 작업</span><span class="sxs-lookup"><span data-stu-id="a4220-102">ApplyAnd operation</span></span>

<span data-ttu-id="a4220-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a4220-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a4220-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a4220-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a4220-105">Adjoint 작업을 수행 하는 측정을 사용 하 여 두 컨트롤의가 모두 1 상태인 경우에만 지정 된 대상 값을 반전 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4220-105">Inverts a given target qubit if and only if both control qubits are in the 1 state, using measurement to perform the adjoint operation.</span></span>

```qsharp
operation ApplyAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="a4220-106">Description</span><span class="sxs-lookup"><span data-stu-id="a4220-106">Description</span></span>

<span data-ttu-id="a4220-107">`target`두 컨트롤이 모두 1 인 경우에만를 반전 하지만는 `target` 상태 0 이라고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4220-107">Inverts `target` if and only if both controls are 1, but assumes that `target` is in state 0.</span></span>  <span data-ttu-id="a4220-108">작업은 T-카운트 4, T-깊이 2를 포함 하 고 도우미가 필요 하지 않습니다 `target` . 따라서가 0으로 알려진 경우에는 CCNOT 연산에 더 적합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4220-108">The operation has T-count 4, T-depth 2 and requires no helper qubit, and may therefore be preferable to a CCNOT operation, if `target` is known to be 0.</span></span>  <span data-ttu-id="a4220-109">이 작업의 adjoint는 측정을 기반으로 하며 T 게이트가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4220-109">The adjoint of this operation is measurement based and requires no T gates.</span></span>

<span data-ttu-id="a4220-110">이 작업을 제어 하는 응용 프로그램에는 도우미를 사용 하지 않아도 `2^c` `Rz` 되며 깊이에 최적화 되지 않습니다 `c` . 여기서은 작업의 두 컨트롤을 포함 하는 전체 컨트롤의 수입니다 `ApplyAnd` .</span><span class="sxs-lookup"><span data-stu-id="a4220-110">The controlled application of this operation requires no helper qubit, `2^c` `Rz` gates and is not optimized for depth, where `c` is the number of overall control qubits including the two controls from the `ApplyAnd` operation.</span></span>  <span data-ttu-id="a4220-111">Adjoint 제어 응용 프로그램에는 `2^c - 1` `Rz` 게이트가 필요 하며,이는 비 adjoint 작업 크기의 각도가 두 배가 되 고, 도우미가 필요 하지 않으며, 깊이를 위해 최적화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4220-111">The adjoint controlled application requires `2^c - 1` `Rz` gates (with an angle twice the size of the non-adjoint operation), no helper qubit and is not optimized for depth.</span></span>

## <a name="input"></a><span data-ttu-id="a4220-112">입력</span><span class="sxs-lookup"><span data-stu-id="a4220-112">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="a4220-113">control1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a4220-113">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a4220-114">첫 번째 제어 비트</span><span class="sxs-lookup"><span data-stu-id="a4220-114">First control qubit</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="a4220-115">control2: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a4220-115">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a4220-116">두 번째 제어 비트</span><span class="sxs-lookup"><span data-stu-id="a4220-116">Second control qubit</span></span>


### <a name="target--qubit"></a><span data-ttu-id="a4220-117">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a4220-117">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a4220-118">대상 보조 비트 상태 0 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4220-118">Target auxiliary qubit; must be in state 0</span></span>



## <a name="output--unit"></a><span data-ttu-id="a4220-119">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a4220-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="a4220-120">참조 항목</span><span class="sxs-lookup"><span data-stu-id="a4220-120">References</span></span>

- <span data-ttu-id="a4220-121">Cody Jones: "내결함성 Toffoli 게이트 Novel 생성", Phys 87, 022328, 2013 [Arxiv: 1212.5069](https://arxiv.org/abs/1212.5069) doi: 10.1103/PhysRevA. 87.022328</span><span class="sxs-lookup"><span data-stu-id="a4220-121">Cody Jones: "Novel constructions for the fault-tolerant Toffoli gate", Phys. Rev. A 87, 022328, 2013 [arXiv:1212.5069](https://arxiv.org/abs/1212.5069) doi:10.1103/PhysRevA.87.022328</span></span>
- <span data-ttu-id="a4220-122">Craig Gidney: "나누어 the 퀀텀 추가 비용", 퀀텀 2, 페이지 74, 2018 [Arxiv: 1709.06648](https://arxiv.org/abs/1709.06648) doi: 10.1103/PhysRevA. 85.044302</span><span class="sxs-lookup"><span data-stu-id="a4220-122">Craig Gidney: "Halving the cost of quantum addition", Quantum 2, page 74, 2018 [arXiv:1709.06648](https://arxiv.org/abs/1709.06648) doi:10.1103/PhysRevA.85.044302</span></span>
- <span data-ttu-id="a4220-123">Mathias Soeken: "퀀텀 Oracle 회로 및 크리스마스 트리 패턴", [2019 년 12 월 19 일의 블로그 문서](https://msoeken.github.io/blog_qac.html) (참고: 여러 제어 된 생성에 대해 설명)</span><span class="sxs-lookup"><span data-stu-id="a4220-123">Mathias Soeken: "Quantum Oracle Circuits and the Christmas Tree Pattern", [Blog article from December 19, 2019](https://msoeken.github.io/blog_qac.html) (note: explains the multiple controlled construction)</span></span>