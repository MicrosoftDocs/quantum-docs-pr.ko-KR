---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: 각 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: e1625829e2e9efd9d39fe0692f01c1cbbffc651c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717592"
---
# <a name="applytoeach-operation"></a><span data-ttu-id="eb367-102">각 작업</span><span class="sxs-lookup"><span data-stu-id="eb367-102">ApplyToEach operation</span></span>

<span data-ttu-id="eb367-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="eb367-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="eb367-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="eb367-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="eb367-105">레지스터의 각 요소에 단일 수준 비트 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb367-105">Applies a single-qubit operation to each element in a register.</span></span>

```qsharp
operation ApplyToEach<'T> (singleElementOperation : ('T => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="eb367-106">입력</span><span class="sxs-lookup"><span data-stu-id="eb367-106">Input</span></span>

### <a name="singleelementoperation--t--unit"></a><span data-ttu-id="eb367-107">singleElementOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eb367-107">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="eb367-108">각 고 비트에 적용할 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="eb367-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="eb367-109">등록: ' t []</span><span class="sxs-lookup"><span data-stu-id="eb367-109">register : 'T[]</span></span>

<span data-ttu-id="eb367-110">지정 된 작업을 적용할 대상 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="eb367-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eb367-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eb367-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="eb367-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="eb367-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="eb367-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="eb367-113">'T</span></span>

<span data-ttu-id="eb367-114">작업이 수행 되는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="eb367-114">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb367-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="eb367-115">See Also</span></span>

- [<span data-ttu-id="eb367-116">Microsoft. 양자. ApplyToEachC</span><span class="sxs-lookup"><span data-stu-id="eb367-116">Microsoft.Quantum.Canon.ApplyToEachC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [<span data-ttu-id="eb367-117">ApplyToEachA입니다.</span><span class="sxs-lookup"><span data-stu-id="eb367-117">Microsoft.Quantum.Canon.ApplyToEachA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [<span data-ttu-id="eb367-118">Microsoft. 양자. ApplyToEachCA</span><span class="sxs-lookup"><span data-stu-id="eb367-118">Microsoft.Quantum.Canon.ApplyToEachCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachCA)