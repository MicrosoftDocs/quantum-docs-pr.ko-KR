---
uid: Microsoft.Quantum.Canon.ApplyIfCA
title: ApplyIfCA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfCA
qsharp.summary: Applies a unitary operation conditioned on a classical bit.
ms.openlocfilehash: b9d5e2c6868dc7b876917abf28f68bb5d0d0f2f7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844996"
---
# <a name="applyifca-operation"></a><span data-ttu-id="a2e7e-102">ApplyIfCA 작업</span><span class="sxs-lookup"><span data-stu-id="a2e7e-102">ApplyIfCA operation</span></span>

<span data-ttu-id="a2e7e-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a2e7e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a2e7e-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a2e7e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a2e7e-105">단일 작업 조건 화 된를 기존 비트에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e7e-105">Applies a unitary operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfCA<'T> (op : ('T => Unit is Ctl + Adj), bit : Bool, target : 'T) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="a2e7e-106">설명</span><span class="sxs-lookup"><span data-stu-id="a2e7e-106">Description</span></span>

<span data-ttu-id="a2e7e-107">작업 `op` 및 비트 값이 지정 된 `bit` `op` `target` 경우가 인 경우에 적용 됩니다 `bit` `true` .</span><span class="sxs-lookup"><span data-stu-id="a2e7e-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="a2e7e-108">이면이 `false` 발생 하지 않습니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="a2e7e-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="a2e7e-109">접미사는 `CA` 적용 될 작업이 단일 (제어 가능 및 adjointable) 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a2e7e-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="a2e7e-110">입력</span><span class="sxs-lookup"><span data-stu-id="a2e7e-110">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="a2e7e-111">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="a2e7e-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a2e7e-112">조건부로 적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a2e7e-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="a2e7e-113">bit: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a2e7e-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a2e7e-114">op가 적용 되는지 여부를 제어 하는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="a2e7e-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="a2e7e-115">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="a2e7e-115">target : 'T</span></span>

<span data-ttu-id="a2e7e-116">작업이 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="a2e7e-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a2e7e-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a2e7e-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a2e7e-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a2e7e-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a2e7e-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="a2e7e-119">'T</span></span>

<span data-ttu-id="a2e7e-120">조건부로 적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a2e7e-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="example"></a><span data-ttu-id="a2e7e-121">예</span><span class="sxs-lookup"><span data-stu-id="a2e7e-121">Example</span></span>

<span data-ttu-id="a2e7e-122">다음은 값의 배열로 지정 된 기존 비트 문자열로 표현 되는 계산 기준 상태로 값의 레지스터를 준비 합니다 `Bool` .</span><span class="sxs-lookup"><span data-stu-id="a2e7e-122">The following prepares a register of qubits into a computational basis state represented by a classical bit string given as an array of `Bool` values:</span></span>

```qsharp
let bitstring = [true, false, true];
using (register = Qubit(3)) {
    ApplyToEach(ApplyIf(X, _, _), Zipped(bitstring, register));
    // register should now be in the state |101⟩.
    ...
}
```

## <a name="see-also"></a><span data-ttu-id="a2e7e-123">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a2e7e-123">See Also</span></span>

- [<span data-ttu-id="a2e7e-124">Microsoft. 양자. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="a2e7e-124">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="a2e7e-125">Microsoft. 양자. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="a2e7e-125">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="a2e7e-126">Microsoft 양자. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="a2e7e-126">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)