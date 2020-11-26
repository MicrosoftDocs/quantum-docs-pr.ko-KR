---
uid: Microsoft.Quantum.Canon.AndLadder
title: AndLadder 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: AndLadder
qsharp.summary: Performs a controlled "AND ladder" on a register of target qubits.
ms.openlocfilehash: 2c6114ec8a5caabdeea8ab7e26a4877e1633671c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209726"
---
# <a name="andladder-operation"></a><span data-ttu-id="40e53-102">AndLadder 작업</span><span class="sxs-lookup"><span data-stu-id="40e53-102">AndLadder operation</span></span>

<span data-ttu-id="40e53-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="40e53-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="40e53-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="40e53-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="40e53-105">대상의 레지스터에서 제어 되는 "및 사다리"를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="40e53-105">Performs a controlled "AND ladder" on a register of target qubits.</span></span>

```qsharp
operation AndLadder (ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="40e53-106">Description</span><span class="sxs-lookup"><span data-stu-id="40e53-106">Description</span></span>

<span data-ttu-id="40e53-107">이 작업은 계산 기준, $ $ \begin{align} \ket{x \_ 1, \dots, x \_ n} \ket{y \_ 1, \dots, y \_ {n-1}} \maps\ket{x \_ 1, \dots, x \_ n} \ket{y \_ 1 \oplus (x 1 \stx 2), \sti의 매핑에 의해 설명 된 변환을 적용 합니다. \_ \_ y \_ {n-1} \oplus (x \_ 1 \stx \_ 2 \st\cststomx \_ {n-1}}, \end{align} $ $ where $ \ket{x \_ 1, \dots, x \_ n} $는의 계산 기준 상태를 나타내며 `controls` , 여기서 $ \ket{y \_ 1, \dots, y \_ {n-1}} $는의 계산 기준 상태를 나타냅니다 `targets` .</span><span class="sxs-lookup"><span data-stu-id="40e53-107">This operation applies a transformation described by the following mapping of the computational basis, $$ \begin{align} \ket{x\_1, \dots, x\_n} \ket{y\_1, \dots, y\_{n - 1}} \mapsto \ket{x\_1, \dots, x\_n} \ket{ y\_1 \oplus (x\_1 \land x\_2), \dots, y\_{n - 1} \oplus (x\_1 \land x\_2 \land \cdots \land x\_{n - 1} }, \end{align} $$ where $\ket{x\_1, \dots, x\_n}$ refers to the computational basis states of `controls`, and where $\ket{y\_1, \dots, y\_{n - 1}}$ refers to the computational basis states of `targets`.</span></span>

## <a name="input"></a><span data-ttu-id="40e53-108">입력</span><span class="sxs-lookup"><span data-stu-id="40e53-108">Input</span></span>

### <a name="ccnot--ccnotop"></a><span data-ttu-id="40e53-109">ccnot: [Ccnotop](xref:Microsoft.Quantum.Canon.CCNOTop)</span><span class="sxs-lookup"><span data-stu-id="40e53-109">ccnot : [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span></span>

<span data-ttu-id="40e53-110">생성에 사용할 CCNOT gate입니다.</span><span class="sxs-lookup"><span data-stu-id="40e53-110">The CCNOT gate to use for the construction.</span></span>


### <a name="controls--qubit"></a><span data-ttu-id="40e53-111">컨트롤: [이상](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="40e53-111">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="40e53-112">및 사다리의 컨트롤로 사용할 비트의 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="40e53-112">A register of qubits to be used as controls for the and ladder.</span></span>
<span data-ttu-id="40e53-113">이 작업은 고정의 계산 기준 상태를 유지 `controls` 합니다.</span><span class="sxs-lookup"><span data-stu-id="40e53-113">This operation leaves computational basis states of `controls` invariant.</span></span>
<span data-ttu-id="40e53-114">의 길이는 `controls` 2 자 이상 이어야 하며,의 길이는 1과 같아야 합니다 `targets` .</span><span class="sxs-lookup"><span data-stu-id="40e53-114">The length of `controls` must be at least 2, and must be equal to one plus the length of `targets`.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="40e53-115">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="40e53-115">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="40e53-116">의 길이는 `targets` 1 자 이상 이어야 하 고 1의 길이에서 1을 뺀 값 사이 여야 합니다 `controls` .</span><span class="sxs-lookup"><span data-stu-id="40e53-116">The length of `targets` must be at least 1 and equal to the length of `controls` minus one.</span></span>



## <a name="output--unit"></a><span data-ttu-id="40e53-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="40e53-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="40e53-118">설명</span><span class="sxs-lookup"><span data-stu-id="40e53-118">Remarks</span></span>

- <span data-ttu-id="40e53-119">및의 일부로 사용 <xref:microsoft.quantum.canon.applymulticontrolledc> <xref:microsoft.quantum.canon.applymulticontrolledca> 됩니다.</span><span class="sxs-lookup"><span data-stu-id="40e53-119">Used as a part of <xref:microsoft.quantum.canon.applymulticontrolledc> and <xref:microsoft.quantum.canon.applymulticontrolledca>.</span></span>
- <span data-ttu-id="40e53-120">설명 및 회로 다이어그램의 경우 그림 4.10, Nielsen & Chuang의 섹션 4.3을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="40e53-120">For the explanation and circuit diagram see Figure 4.10, Section 4.3 in Nielsen & Chuang.</span></span>

## <a name="references"></a><span data-ttu-id="40e53-121">참조 항목</span><span class="sxs-lookup"><span data-stu-id="40e53-121">References</span></span>

- [<span data-ttu-id="40e53-122">*Michael Nielsen, Isaac Chuang*, 퀀텀 계산 및 퀀텀 정보</span><span class="sxs-lookup"><span data-stu-id="40e53-122"> *Michael A. Nielsen , Isaac L. Chuang*, Quantum Computation and Quantum Information </span></span>](http://doi.org/10.1017/CBO9780511976667)