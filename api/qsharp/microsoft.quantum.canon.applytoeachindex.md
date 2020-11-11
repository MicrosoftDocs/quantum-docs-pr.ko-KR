---
uid: Microsoft.Quantum.Canon.ApplyToEachIndex
title: ApplyToEachIndex 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndex
qsharp.summary: Applies a single-qubit operation to each indexed element in a register.
ms.openlocfilehash: 4ce184b34add9238e26f9b35b40ec0bddb23ccf9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717543"
---
# <a name="applytoeachindex-operation"></a><span data-ttu-id="e5e95-102">ApplyToEachIndex 작업</span><span class="sxs-lookup"><span data-stu-id="e5e95-102">ApplyToEachIndex operation</span></span>

<span data-ttu-id="e5e95-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e5e95-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e5e95-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e5e95-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e5e95-105">레지스터의 인덱싱된 각 요소에 단일 수준 비트 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5e95-105">Applies a single-qubit operation to each indexed element in a register.</span></span>

```qsharp
operation ApplyToEachIndex<'T> (singleElementOperation : ((Int, 'T) => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e5e95-106">입력</span><span class="sxs-lookup"><span data-stu-id="e5e95-106">Input</span></span>

### <a name="singleelementoperation--intt--unit"></a><span data-ttu-id="e5e95-107">singleElementOperation: ([Int](xref:microsoft.quantum.lang-ref.int), t) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e5e95-107">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="e5e95-108">각 고 비트에 적용할 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="e5e95-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="e5e95-109">등록: ' t []</span><span class="sxs-lookup"><span data-stu-id="e5e95-109">register : 'T[]</span></span>

<span data-ttu-id="e5e95-110">지정 된 작업을 적용할 대상 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="e5e95-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e5e95-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e5e95-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e5e95-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e5e95-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e5e95-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="e5e95-113">'T</span></span>

<span data-ttu-id="e5e95-114">각 작업의 역할을 하는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="e5e95-114">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5e95-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e5e95-115">See Also</span></span>

- [<span data-ttu-id="e5e95-116">각각의 Microsoft 양자</span><span class="sxs-lookup"><span data-stu-id="e5e95-116">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)
- [<span data-ttu-id="e5e95-117">ApplyToEachIndexA입니다.</span><span class="sxs-lookup"><span data-stu-id="e5e95-117">Microsoft.Quantum.Canon.ApplyToEachIndexA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexA)
- [<span data-ttu-id="e5e95-118">Microsoft. 양자. ApplyToEachIndexC</span><span class="sxs-lookup"><span data-stu-id="e5e95-118">Microsoft.Quantum.Canon.ApplyToEachIndexC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexC)
- [<span data-ttu-id="e5e95-119">Microsoft. 양자. ApplyToEachIndexCA</span><span class="sxs-lookup"><span data-stu-id="e5e95-119">Microsoft.Quantum.Canon.ApplyToEachIndexCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexCA)