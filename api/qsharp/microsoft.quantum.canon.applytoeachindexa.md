---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexA
title: ApplyToEachIndexA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: 0fe0697e6f1d9441c2d2ad2c7396f6da8daa0e1e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717536"
---
# <a name="applytoeachindexa-operation"></a><span data-ttu-id="19928-102">ApplyToEachIndexA 작업</span><span class="sxs-lookup"><span data-stu-id="19928-102">ApplyToEachIndexA operation</span></span>

<span data-ttu-id="19928-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="19928-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="19928-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="19928-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="19928-105">레지스터의 인덱싱된 각 요소에 단일 수준 비트 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="19928-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="19928-106">한정자는 `A` 단일의 비트 연산이 adjointable을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="19928-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachIndexA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="19928-107">입력</span><span class="sxs-lookup"><span data-stu-id="19928-107">Input</span></span>

### <a name="singleelementoperation--intt--unit-adj"></a><span data-ttu-id="19928-108">singleElementOperation: ([Int](xref:microsoft.quantum.lang-ref.int), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="19928-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="19928-109">각 고 비트에 적용할 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="19928-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="19928-110">등록: ' t []</span><span class="sxs-lookup"><span data-stu-id="19928-110">register : 'T[]</span></span>

<span data-ttu-id="19928-111">지정 된 작업을 적용할 대상 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="19928-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="19928-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="19928-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="19928-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="19928-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="19928-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="19928-114">'T</span></span>

<span data-ttu-id="19928-115">각 작업의 역할을 하는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="19928-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="19928-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="19928-116">See Also</span></span>

- [<span data-ttu-id="19928-117">Microsoft. 양자. ApplyToEachIndex</span><span class="sxs-lookup"><span data-stu-id="19928-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)