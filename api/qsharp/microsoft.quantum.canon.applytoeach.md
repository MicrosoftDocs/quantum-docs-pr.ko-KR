---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: 각 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: 11f9363feb38676df3f805496c74036aa96160c1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217869"
---
# <a name="applytoeach-operation"></a><span data-ttu-id="4d3da-102">각 작업</span><span class="sxs-lookup"><span data-stu-id="4d3da-102">ApplyToEach operation</span></span>

<span data-ttu-id="4d3da-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4d3da-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4d3da-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4d3da-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4d3da-105">레지스터의 각 요소에 단일 수준 비트 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3da-105">Applies a single-qubit operation to each element in a register.</span></span>

```qsharp
operation ApplyToEach<'T> (singleElementOperation : ('T => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="4d3da-106">입력</span><span class="sxs-lookup"><span data-stu-id="4d3da-106">Input</span></span>

### <a name="singleelementoperation--t--unit"></a><span data-ttu-id="4d3da-107">singleElementOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4d3da-107">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="4d3da-108">각 고 비트에 적용할 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="4d3da-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="4d3da-109">등록: ' t []</span><span class="sxs-lookup"><span data-stu-id="4d3da-109">register : 'T[]</span></span>

<span data-ttu-id="4d3da-110">지정 된 작업을 적용할 대상 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="4d3da-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4d3da-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4d3da-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4d3da-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4d3da-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4d3da-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="4d3da-113">'T</span></span>

<span data-ttu-id="4d3da-114">작업이 수행 되는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="4d3da-114">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="4d3da-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4d3da-115">See Also</span></span>

- [<span data-ttu-id="4d3da-116">Microsoft. 양자. ApplyToEachC</span><span class="sxs-lookup"><span data-stu-id="4d3da-116">Microsoft.Quantum.Canon.ApplyToEachC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [<span data-ttu-id="4d3da-117">ApplyToEachA입니다.</span><span class="sxs-lookup"><span data-stu-id="4d3da-117">Microsoft.Quantum.Canon.ApplyToEachA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [<span data-ttu-id="4d3da-118">Microsoft. 양자. ApplyToEachCA</span><span class="sxs-lookup"><span data-stu-id="4d3da-118">Microsoft.Quantum.Canon.ApplyToEachCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachCA)