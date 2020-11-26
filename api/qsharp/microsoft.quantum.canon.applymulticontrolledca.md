---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledCA
title: ApplyMultiControlledCA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledCA
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: 28797583c23e21eb4bcae996a34c70ee06c6dbe8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209284"
---
# <a name="applymulticontrolledca-operation"></a><span data-ttu-id="c2e32-102">ApplyMultiControlledCA 작업</span><span class="sxs-lookup"><span data-stu-id="c2e32-102">ApplyMultiControlledCA operation</span></span>

<span data-ttu-id="c2e32-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c2e32-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c2e32-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c2e32-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c2e32-105">단일 제어 작업의 곱셈 제어 버전을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e32-105">Applies a multiply controlled version of a singly controlled operation.</span></span>
<span data-ttu-id="c2e32-106">한정자는 `CA` 단일의 비트 작업을 제어 하 고 adjointable 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c2e32-106">The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyMultiControlledCA (singlyControlledOp : (Qubit[] => Unit is Adj), ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c2e32-107">입력</span><span class="sxs-lookup"><span data-stu-id="c2e32-107">Input</span></span>

### <a name="singlycontrolledop--qubit--unit--is-adj"></a><span data-ttu-id="c2e32-108">singlyControlledOp: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is</span><span class="sxs-lookup"><span data-stu-id="c2e32-108">singlyControlledOp : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="c2e32-109">단일 비트에 대해 제어 되는 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="c2e32-109">An operation controlled on a single qubit.</span></span>
<span data-ttu-id="c2e32-110">작업의 인수에서 첫 번째 인수는 컨트롤로 간주 되 고 나머지는 대상 비트 비트로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2e32-110">The first qubit in the argument of the operation assumed to be a control and the rest are assumed to be target qubits.</span></span>
<span data-ttu-id="c2e32-111">`ApplyMultiControlled` 항상 `singlyControlledOp` 1 이상의 길이 인수를 사용 하 여를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e32-111">`ApplyMultiControlled` always calls `singlyControlledOp` with an argument of length at least 1.</span></span>


### <a name="ccnot--ccnotop"></a><span data-ttu-id="c2e32-112">ccnot: [Ccnotop](xref:Microsoft.Quantum.Canon.CCNOTop)</span><span class="sxs-lookup"><span data-stu-id="c2e32-112">ccnot : [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span></span>

<span data-ttu-id="c2e32-113">생성에 사용할 제어 되지 않은 제어 된 게이트입니다.</span><span class="sxs-lookup"><span data-stu-id="c2e32-113">The controlled-controlled-NOT gate to use for the construction.</span></span>


### <a name="controls--qubit"></a><span data-ttu-id="c2e32-114">컨트롤: [이상](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c2e32-114">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c2e32-115">`singlyControlledOp`제어 될의 대상 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="c2e32-115">The qubits that `singlyControlledOp` is to be controlled on.</span></span>
<span data-ttu-id="c2e32-116">의 길이는 `controls` 1 이상 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e32-116">The length of `controls` must be at least 1.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="c2e32-117">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c2e32-117">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c2e32-118">에 대해 작동 하는 대상 비트 `singlyControlledOp` 입니다.</span><span class="sxs-lookup"><span data-stu-id="c2e32-118">The target qubits that `singlyControlledOp` acts upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c2e32-119">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c2e32-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c2e32-120">설명</span><span class="sxs-lookup"><span data-stu-id="c2e32-120">Remarks</span></span>

<span data-ttu-id="c2e32-121">이 작업은 clean ancilla  비트만 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e32-121">This operation uses only clean ancilla qubits.</span></span>

<span data-ttu-id="c2e32-122">설명 및 회로 다이어그램의 경우 그림 4.10, Nielsen & Chuang의 섹션 4.3을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2e32-122">For the explanation and circuit diagram see Figure 4.10, Section 4.3 in Nielsen & Chuang</span></span>

## <a name="references"></a><span data-ttu-id="c2e32-123">참조 항목</span><span class="sxs-lookup"><span data-stu-id="c2e32-123">References</span></span>

- [<span data-ttu-id="c2e32-124">*Michael Nielsen, Isaac Chuang*, 퀀텀 계산 및 퀀텀 정보</span><span class="sxs-lookup"><span data-stu-id="c2e32-124"> *Michael A. Nielsen , Isaac L. Chuang*, Quantum Computation and Quantum Information </span></span>](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a><span data-ttu-id="c2e32-125">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c2e32-125">See Also</span></span>

- [<span data-ttu-id="c2e32-126">ApplyMultiControlledC입니다.</span><span class="sxs-lookup"><span data-stu-id="c2e32-126">Microsoft.Quantum.Canon.ApplyMultiControlledC</span></span>](xref:Microsoft.Quantum.Canon.ApplyMultiControlledC)