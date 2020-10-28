---
uid: Microsoft.Quantum.Canon.ApplyControlledOnInt
title: ApplyControlledOnInt 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnInt
qsharp.summary: Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: c8ea76946143967de4b6ac65986a1c4407ecb633
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718352"
---
# <a name="applycontrolledonint-operation"></a><span data-ttu-id="f70eb-102">ApplyControlledOnInt 작업</span><span class="sxs-lookup"><span data-stu-id="f70eb-102">ApplyControlledOnInt operation</span></span>

<span data-ttu-id="f70eb-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f70eb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f70eb-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f70eb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f70eb-105">컨트롤 레지스터 상태가 지정 된 양의 정수에 해당 하는 경우 대상 레지스터에 단일 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70eb-105">Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
operation ApplyControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="f70eb-106">입력</span><span class="sxs-lookup"><span data-stu-id="f70eb-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="f70eb-107">번호 상태: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f70eb-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f70eb-108">작업을 제어 해야 하는 음수가 아닌 정수 `oracle` 입니다.</span><span class="sxs-lookup"><span data-stu-id="f70eb-108">A nonnegative integer on which the operation `oracle` should be controlled.</span></span>


### <a name="oracle--t--unit-adj--ctl"></a><span data-ttu-id="f70eb-109">oracle: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="f70eb-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="f70eb-110">제어할 단일 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="f70eb-110">A unitary operation to be controlled.</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="f70eb-111">controlRegister: [bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f70eb-111">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f70eb-112">의 응용 프로그램을 제어 하는 퀀텀 레지스터입니다 `oracle` .</span><span class="sxs-lookup"><span data-stu-id="f70eb-112">A quantum register that controls application of `oracle`.</span></span>


### <a name="targetregister--t"></a><span data-ttu-id="f70eb-113">targetRegister: ' t</span><span class="sxs-lookup"><span data-stu-id="f70eb-113">targetRegister : 'T</span></span>

<span data-ttu-id="f70eb-114">적용할 레지스터 `oracle` 입니다.</span><span class="sxs-lookup"><span data-stu-id="f70eb-114">A register on which to apply `oracle`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f70eb-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f70eb-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f70eb-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f70eb-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f70eb-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="f70eb-117">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="f70eb-118">설명</span><span class="sxs-lookup"><span data-stu-id="f70eb-118">Remarks</span></span>

<span data-ttu-id="f70eb-119">의 값은 `numberState` 작은 endian 인코딩을 사용 하 여 해석 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f70eb-119">The value of `numberState` is interpreted using a little-endian encoding.</span></span>

<span data-ttu-id="f70eb-120">`numberState` 최대 $2 ^ \texttt{Length (controlRegister)}-$1 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70eb-120">`numberState` must be at most $2^\texttt{Length(controlRegister)} - 1$.</span></span>
<span data-ttu-id="f70eb-121">예를 들어는 `numberState = 537` `oracle` `controlRegister` 가 $ \ket $ 상태에 있는 경우에만이 적용 됨을 의미 합니다 {537} .</span><span class="sxs-lookup"><span data-stu-id="f70eb-121">For example, `numberState = 537` means that `oracle` is applied if and only if `controlRegister` is in the state $\ket{537}$.</span></span>