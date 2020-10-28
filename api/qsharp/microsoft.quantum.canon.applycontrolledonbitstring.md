---
uid: Microsoft.Quantum.Canon.ApplyControlledOnBitString
title: ApplyControlledOnBitString 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnBitString
qsharp.summary: Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.
ms.openlocfilehash: 7a054511bacff574e6f7e889ace048c78886cf91
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718357"
---
# <a name="applycontrolledonbitstring-operation"></a><span data-ttu-id="7ed4b-102">ApplyControlledOnBitString 작업</span><span class="sxs-lookup"><span data-stu-id="7ed4b-102">ApplyControlledOnBitString operation</span></span>

<span data-ttu-id="7ed4b-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7ed4b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7ed4b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7ed4b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7ed4b-105">지정 된 비트 마스크로 지정 된 상태에 의해 제어 되는 단일 작업을 대상 레지스터에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ed4b-105">Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.</span></span>

```qsharp
operation ApplyControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="7ed4b-106">입력</span><span class="sxs-lookup"><span data-stu-id="7ed4b-106">Input</span></span>

### <a name="bits--bool"></a><span data-ttu-id="7ed4b-107">bits: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="7ed4b-107">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="7ed4b-108">지정 된 단일 작업을 제어 하는 비트 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="7ed4b-108">The bit string to control the given unitary operation on.</span></span>


### <a name="oracle--t--unit-adj--ctl"></a><span data-ttu-id="7ed4b-109">oracle: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="7ed4b-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="7ed4b-110">대상 레지스터에 적용 될 단일 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="7ed4b-110">The unitary operation to be applied on the target register.</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="7ed4b-111">controlRegister: [bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7ed4b-111">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7ed4b-112">의 응용 프로그램을 제어 하는 퀀텀 레지스터입니다 `oracle` .</span><span class="sxs-lookup"><span data-stu-id="7ed4b-112">A quantum register that controls application of `oracle`.</span></span>


### <a name="targetregister--t"></a><span data-ttu-id="7ed4b-113">targetRegister: ' t</span><span class="sxs-lookup"><span data-stu-id="7ed4b-113">targetRegister : 'T</span></span>

<span data-ttu-id="7ed4b-114">입력으로에 전달 되는 대상 레지스터 `oracle` 입니다.</span><span class="sxs-lookup"><span data-stu-id="7ed4b-114">The target register to be passed to `oracle` as an input.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7ed4b-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7ed4b-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7ed4b-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7ed4b-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7ed4b-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="7ed4b-117">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="7ed4b-118">설명</span><span class="sxs-lookup"><span data-stu-id="7ed4b-118">Remarks</span></span>

<span data-ttu-id="7ed4b-119">에 지정 된 패턴은 `bits` 보다 짧을 수 있습니다 `controlRegister` .이 경우 추가 컨트롤의 비트는 무시 됩니다. 즉, $ \ket {0} $ 또는 $ \ket $에서 제어 되지 않습니다 {1} .</span><span class="sxs-lookup"><span data-stu-id="7ed4b-119">The pattern given by `bits` may be shorter than `controlRegister`, in which case additional control qubits are ignored (that is, neither controlled on $\ket{0}$ nor $\ket{1}$).</span></span>
<span data-ttu-id="7ed4b-120">`bits`가 보다 길면 `controlRegister` 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ed4b-120">If `bits` is longer than `controlRegister`, an error is raised.</span></span>

<span data-ttu-id="7ed4b-121">예를 들어는 `bits = [0,1,0,0,1]` `oracle` `controlRegister` 가 $ \ket {0} \ket {1} \ket {0} \ket {0} \ket {1} $ 상태에 있는 경우에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ed4b-121">For example, `bits = [0,1,0,0,1]` means that `oracle` is applied if and only if `controlRegister` is in the state $\ket{0}\ket{1}\ket{0}\ket{0}\ket{1}$.</span></span>