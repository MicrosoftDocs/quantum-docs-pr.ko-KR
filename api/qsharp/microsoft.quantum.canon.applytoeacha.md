---
uid: Microsoft.Quantum.Canon.ApplyToEachA
title: ApplyToEachA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: 9485c6549ed4e1a6fb3abdfa3f85ba35579d8b0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717578"
---
# <a name="applytoeacha-operation"></a><span data-ttu-id="c4501-102">ApplyToEachA 작업</span><span class="sxs-lookup"><span data-stu-id="c4501-102">ApplyToEachA operation</span></span>

<span data-ttu-id="c4501-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c4501-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c4501-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c4501-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c4501-105">레지스터의 각 요소에 단일 수준 비트 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4501-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="c4501-106">한정자는 `A` 단일의 비트 연산이 adjointable을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c4501-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachA<'T> (singleElementOperation : ('T => Unit is Adj), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="c4501-107">입력</span><span class="sxs-lookup"><span data-stu-id="c4501-107">Input</span></span>

### <a name="singleelementoperation--t--unit-adj"></a><span data-ttu-id="c4501-108">singleElementOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="c4501-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="c4501-109">각 고 비트에 적용할 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="c4501-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="c4501-110">등록: ' t []</span><span class="sxs-lookup"><span data-stu-id="c4501-110">register : 'T[]</span></span>

<span data-ttu-id="c4501-111">지정 된 작업을 적용할 대상 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="c4501-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c4501-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c4501-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c4501-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c4501-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c4501-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="c4501-114">'T</span></span>

<span data-ttu-id="c4501-115">작업이 수행 되는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="c4501-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4501-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c4501-116">See Also</span></span>

- [<span data-ttu-id="c4501-117">각각의 Microsoft 양자</span><span class="sxs-lookup"><span data-stu-id="c4501-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)