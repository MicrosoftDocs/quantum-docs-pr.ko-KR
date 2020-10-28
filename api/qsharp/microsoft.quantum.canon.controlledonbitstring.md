---
uid: Microsoft.Quantum.Canon.ControlledOnBitString
title: ControlledOnBitString 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnBitString
qsharp.summary: Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.
ms.openlocfilehash: ca5a6e116eff187060f7a160e42836b170f0362d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716444"
---
# <a name="controlledonbitstring-function"></a><span data-ttu-id="ac9c9-102">ControlledOnBitString 함수</span><span class="sxs-lookup"><span data-stu-id="ac9c9-102">ControlledOnBitString function</span></span>

<span data-ttu-id="ac9c9-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ac9c9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ac9c9-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ac9c9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ac9c9-105">컨트롤 레지스터 상태가 지정 된 비트 마스크에 해당 하는 경우 대상 레지스터에 oracle을 적용 하는 단일 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac9c9-105">Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.</span></span>

```qsharp
function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="description"></a><span data-ttu-id="ac9c9-106">Description</span><span class="sxs-lookup"><span data-stu-id="ac9c9-106">Description</span></span>

<span data-ttu-id="ac9c9-107">이 함수의 출력은 \begin{align} U \ket{b_0 b_1 \cdots b_ {n-1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_ {n-1}}와 같이 단일 변환 $U $로 나타낼 수 있는 작업입니다. \cdots \begin{cases} V \ket{\psi} & \t extrm{if} (b_0 b_1 \cdots b_ {n-1}) = \texttt{bits} \\ \\ \ket{\psi} & \textrm{otherwise} \end{cases}, \end{align} where $V $은 작업 동작을 나타내는 단일 변환입니다 `oracle` .</span><span class="sxs-lookup"><span data-stu-id="ac9c9-107">The output of this function is an operation that can be represented by a unitary transformation $U$ such that \begin{align} U \ket{b_0 b_1 \cdots b_{n - 1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_{n-1}} \otimes \begin{cases} V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_{n - 1}) = \texttt{bits} \\\\ \ket{\psi} & \textrm{otherwise} \end{cases}, \end{align} where $V$ is a unitary transformation that represents the action of the `oracle` operation.</span></span>

## <a name="input"></a><span data-ttu-id="ac9c9-108">입력</span><span class="sxs-lookup"><span data-stu-id="ac9c9-108">Input</span></span>

### <a name="bits--bool"></a><span data-ttu-id="ac9c9-109">bits: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="ac9c9-109">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="ac9c9-110">지정 된 단일 작업을 제어 하는 비트 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="ac9c9-110">The bit string to control the given unitary operation on.</span></span>


### <a name="oracle--t--unit-adj--ctl"></a><span data-ttu-id="ac9c9-111">oracle: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="ac9c9-111">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="ac9c9-112">대상 레지스터에 적용 될 단일 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="ac9c9-112">The unitary operation to be applied on the target register.</span></span>



## <a name="output--qubitt--unit-adj--ctl"></a><span data-ttu-id="ac9c9-113">출력: ([Adj []](xref:microsoft.quantum.lang-ref.qubit), ' t) => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="ac9c9-113">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="ac9c9-114">`oracle`컨트롤 레지스터 상태가 비트 마스크에 해당 하는 경우 대상 레지스터에 적용 되는 단일 작업입니다 `bits` .</span><span class="sxs-lookup"><span data-stu-id="ac9c9-114">A unitary operation that applies `oracle` on the target register if the control register state corresponds to the bit mask `bits`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ac9c9-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ac9c9-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ac9c9-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="ac9c9-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="ac9c9-117">설명</span><span class="sxs-lookup"><span data-stu-id="ac9c9-117">Remarks</span></span>

<span data-ttu-id="ac9c9-118">에 지정 된 패턴은 `bits` 보다 짧을 수 있습니다 `controlRegister` .이 경우 추가 컨트롤의 비트는 무시 됩니다. 즉, $ \ket {0} $ 또는 $ \ket $에서 제어 되지 않습니다 {1} .</span><span class="sxs-lookup"><span data-stu-id="ac9c9-118">The pattern given by `bits` may be shorter than `controlRegister`, in which case additional control qubits are ignored (that is, neither controlled on $\ket{0}$ nor $\ket{1}$).</span></span>
<span data-ttu-id="ac9c9-119">`bits`가 보다 길면 `controlRegister` 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac9c9-119">If `bits` is longer than `controlRegister`, an error is raised.</span></span>

<span data-ttu-id="ac9c9-120">부울 배열과 `bits` 단일 연산이 제공 되는 경우 `oracle` 이 함수의 출력은 다음 단계를 수행 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="ac9c9-120">Given a Boolean array `bits` and a unitary operation `oracle`, the output of this function is an operation that performs the following steps:</span></span>

* <span data-ttu-id="ac9c9-121">`X`의 요소에 해당 하는 컨트롤 레지스터의 각 요소에 작업을 적용 `false` 합니다 `bits` .</span><span class="sxs-lookup"><span data-stu-id="ac9c9-121">apply an `X` operation to each qubit of the control register that corresponds to `false` element of the `bits`;</span></span>
* <span data-ttu-id="ac9c9-122">`Controlled oracle`컨트롤 및 대상 레지스터에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac9c9-122">apply `Controlled oracle` to the control and target registers;</span></span>
* <span data-ttu-id="ac9c9-123">`X`의 요소에 해당 하는 컨트롤 레지스터의 각 요소에 작업을 적용 하 여 `false` `bits` 컨트롤을 원래 상태로 되돌립니다.</span><span class="sxs-lookup"><span data-stu-id="ac9c9-123">apply an `X` operation to each qubit of the control register that corresponds to `false` element of the `bits` again to return the control register to the original state.</span></span>

<span data-ttu-id="ac9c9-124">함수 출력은 `Controlled` `ControlledOnBitString` `bits` 가와 같은 특수 한 경우입니다 `[true, ..., true]` .</span><span class="sxs-lookup"><span data-stu-id="ac9c9-124">The output of the `Controlled` functor is a special case of `ControlledOnBitString` where `bits` is equal to `[true, ..., true]`.</span></span>