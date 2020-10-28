---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget
title: ApplyXControlledOnTruthTableWithCleanTarget 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTableWithCleanTarget
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: b43a5351985339bcf7c1f2bbe03ae6dc6dfdd165
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725233"
---
# <a name="applyxcontrolledontruthtablewithcleantarget-operation"></a><span data-ttu-id="87068-102">ApplyXControlledOnTruthTableWithCleanTarget 작업</span><span class="sxs-lookup"><span data-stu-id="87068-102">ApplyXControlledOnTruthTableWithCleanTarget operation</span></span>

<span data-ttu-id="87068-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="87068-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="87068-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="87068-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="87068-105">@"microsoft.quantum.intrinsic.x" `target` `func` 의 기존 할당에 대해 부울 함수가 true로 평가 되는 경우에 작업을 적용 합니다 `controlRegister` .</span><span class="sxs-lookup"><span data-stu-id="87068-105">Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.</span></span>

```qsharp
operation ApplyXControlledOnTruthTableWithCleanTarget (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="87068-106">Description</span><span class="sxs-lookup"><span data-stu-id="87068-106">Description</span></span>

<span data-ttu-id="87068-107">이 작업은 @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" 대상의가 $ \ket $ 상태에 있는 것으로 알려진 특수 한 사례를 구현 {0} 합니다.</span><span class="sxs-lookup"><span data-stu-id="87068-107">This operation implements a special case of @"microsoft.quantum.synthesis.applyxcontrolledontruthtable", in which the target qubit is known to be in the $\ket{0}$ state.</span></span>

<span data-ttu-id="87068-108">구현에서는 @"microsoft.quantum.intrinsic.cnot" 및 게이트를 사용 @"microsoft.quantum.intrinsic.r1" 합니다.</span><span class="sxs-lookup"><span data-stu-id="87068-108">The implementation makes use of @"microsoft.quantum.intrinsic.cnot" and @"microsoft.quantum.intrinsic.r1" gates.</span></span>  <span data-ttu-id="87068-109">Adjoint 작업의 구현은 최적화 되며 측정 기반 비 계산을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="87068-109">The implementation of the adjoint operation is optimized and uses measurement-based uncomputation.</span></span>

## <a name="input"></a><span data-ttu-id="87068-110">입력</span><span class="sxs-lookup"><span data-stu-id="87068-110">Input</span></span>

### <a name="func--bigint"></a><span data-ttu-id="87068-111">func: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="87068-111">func : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="87068-112">큰 정수로 표시 되는 부울 참 테이블</span><span class="sxs-lookup"><span data-stu-id="87068-112">Boolean truth table represented as big integer</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="87068-113">controlRegister: [bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="87068-113">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="87068-114">컨트롤의 등록</span><span class="sxs-lookup"><span data-stu-id="87068-114">Register of control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="87068-115">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="87068-115">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="87068-116">대상 비트 ($ \ket $ 상태 여야 함 {0} )</span><span class="sxs-lookup"><span data-stu-id="87068-116">Target qubit (must be in $\ket{0}$ state)</span></span>



## <a name="output--unit"></a><span data-ttu-id="87068-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="87068-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="87068-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="87068-118">See Also</span></span>

- [<span data-ttu-id="87068-119">ApplyXControlledOnTruthTable.</span><span class="sxs-lookup"><span data-stu-id="87068-119">Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable)