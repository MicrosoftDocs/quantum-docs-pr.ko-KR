---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: 각 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: 61dda69751989ef8a98fa8fb01d832014ec4ad35
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844635"
---
# <a name="applytoeach-operation"></a><span data-ttu-id="51c3d-102">각 작업</span><span class="sxs-lookup"><span data-stu-id="51c3d-102">ApplyToEach operation</span></span>

<span data-ttu-id="51c3d-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="51c3d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="51c3d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="51c3d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="51c3d-105">레지스터의 각 요소에 단일 수준 비트 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="51c3d-105">Applies a single-qubit operation to each element in a register.</span></span>

```qsharp
operation ApplyToEach<'T> (singleElementOperation : ('T => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="51c3d-106">입력</span><span class="sxs-lookup"><span data-stu-id="51c3d-106">Input</span></span>

### <a name="singleelementoperation--t--unit"></a><span data-ttu-id="51c3d-107">singleElementOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="51c3d-107">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="51c3d-108">각 고 비트에 적용할 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="51c3d-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="51c3d-109">등록: ' t []</span><span class="sxs-lookup"><span data-stu-id="51c3d-109">register : 'T[]</span></span>

<span data-ttu-id="51c3d-110">지정 된 작업을 적용할 대상 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="51c3d-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="51c3d-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="51c3d-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="51c3d-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="51c3d-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="51c3d-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="51c3d-113">'T</span></span>

<span data-ttu-id="51c3d-114">작업이 수행 되는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="51c3d-114">The target on which the operation acts.</span></span>

## <a name="example"></a><span data-ttu-id="51c3d-115">예</span><span class="sxs-lookup"><span data-stu-id="51c3d-115">Example</span></span>

<span data-ttu-id="51c3d-116">3-이상 비트 $ \ket{+} $ 상태 준비:</span><span class="sxs-lookup"><span data-stu-id="51c3d-116">Prepare a three-qubit $\ket{+}$ state:</span></span>

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a><span data-ttu-id="51c3d-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="51c3d-117">See Also</span></span>

- [<span data-ttu-id="51c3d-118">Microsoft. 양자. ApplyToEachC</span><span class="sxs-lookup"><span data-stu-id="51c3d-118">Microsoft.Quantum.Canon.ApplyToEachC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [<span data-ttu-id="51c3d-119">ApplyToEachA입니다.</span><span class="sxs-lookup"><span data-stu-id="51c3d-119">Microsoft.Quantum.Canon.ApplyToEachA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [<span data-ttu-id="51c3d-120">Microsoft. 양자. ApplyToEachCA</span><span class="sxs-lookup"><span data-stu-id="51c3d-120">Microsoft.Quantum.Canon.ApplyToEachCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachCA)