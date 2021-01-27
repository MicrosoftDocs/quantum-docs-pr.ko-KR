---
uid: Microsoft.Quantum.Canon.ApplyToEachA
title: ApplyToEachA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: da901db2bb3c70186bfe0c8812b5710198d1dff3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844612"
---
# <a name="applytoeacha-operation"></a><span data-ttu-id="e1655-102">ApplyToEachA 작업</span><span class="sxs-lookup"><span data-stu-id="e1655-102">ApplyToEachA operation</span></span>

<span data-ttu-id="e1655-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e1655-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e1655-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e1655-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e1655-105">레지스터의 각 요소에 단일 수준 비트 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1655-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="e1655-106">한정자는 `A` 단일의 비트 연산이 adjointable을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e1655-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachA<'T> (singleElementOperation : ('T => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="e1655-107">입력</span><span class="sxs-lookup"><span data-stu-id="e1655-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-adj"></a><span data-ttu-id="e1655-108">singleElementOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="e1655-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e1655-109">각 고 비트에 적용할 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="e1655-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="e1655-110">등록: ' t []</span><span class="sxs-lookup"><span data-stu-id="e1655-110">register : 'T[]</span></span>

<span data-ttu-id="e1655-111">지정 된 작업을 적용할 대상 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="e1655-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e1655-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e1655-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e1655-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e1655-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e1655-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="e1655-114">'T</span></span>

<span data-ttu-id="e1655-115">작업이 수행 되는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="e1655-115">The target on which the operation acts.</span></span>

## <a name="example"></a><span data-ttu-id="e1655-116">예</span><span class="sxs-lookup"><span data-stu-id="e1655-116">Example</span></span>

<span data-ttu-id="e1655-117">3-이상 비트 $ \ket{+} $ 상태 준비:</span><span class="sxs-lookup"><span data-stu-id="e1655-117">Prepare a three-qubit $\ket{+}$ state:</span></span>

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a><span data-ttu-id="e1655-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e1655-118">See Also</span></span>

- [<span data-ttu-id="e1655-119">각각의 Microsoft 양자</span><span class="sxs-lookup"><span data-stu-id="e1655-119">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)