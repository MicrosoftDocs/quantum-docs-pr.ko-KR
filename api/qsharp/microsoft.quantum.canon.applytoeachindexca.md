---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexCA
title: ApplyToEachIndexCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexCA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.
ms.openlocfilehash: c5bb61aadbdaab9c74a3dcd418088c532b495ff5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717515"
---
# <a name="applytoeachindexca-operation"></a><span data-ttu-id="e1b3b-102">ApplyToEachIndexCA 작업</span><span class="sxs-lookup"><span data-stu-id="e1b3b-102">ApplyToEachIndexCA operation</span></span>

<span data-ttu-id="e1b3b-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e1b3b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e1b3b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e1b3b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e1b3b-105">레지스터의 인덱싱된 각 요소에 단일 수준 비트 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1b3b-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="e1b3b-106">한정자는 `CA` 단일의 비트 연산이 adjointable 및 제어 가능 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e1b3b-106">The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.</span></span>

```qsharp
operation ApplyToEachIndexCA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj + Ctl), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e1b3b-107">입력</span><span class="sxs-lookup"><span data-stu-id="e1b3b-107">Input</span></span>

### <a name="singleelementoperation--intt--unit-adj--ctl"></a><span data-ttu-id="e1b3b-108">singleElementOperation: ([Int](xref:microsoft.quantum.lang-ref.int), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="e1b3b-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="e1b3b-109">각 고 비트에 적용할 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b3b-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="e1b3b-110">등록: ' t []</span><span class="sxs-lookup"><span data-stu-id="e1b3b-110">register : 'T[]</span></span>

<span data-ttu-id="e1b3b-111">지정 된 작업을 적용할 대상 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b3b-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e1b3b-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e1b3b-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e1b3b-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e1b3b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e1b3b-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="e1b3b-114">'T</span></span>

<span data-ttu-id="e1b3b-115">각 작업의 역할을 하는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b3b-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1b3b-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e1b3b-116">See Also</span></span>

- [<span data-ttu-id="e1b3b-117">Microsoft. 양자. ApplyToEachIndex</span><span class="sxs-lookup"><span data-stu-id="e1b3b-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)