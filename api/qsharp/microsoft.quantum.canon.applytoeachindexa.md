---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexA
title: ApplyToEachIndexA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: e3ff812f14181e676fddf436af8a14f9a58271ec
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217597"
---
# <a name="applytoeachindexa-operation"></a><span data-ttu-id="f7c85-102">ApplyToEachIndexA 작업</span><span class="sxs-lookup"><span data-stu-id="f7c85-102">ApplyToEachIndexA operation</span></span>

<span data-ttu-id="f7c85-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f7c85-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f7c85-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f7c85-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f7c85-105">레지스터의 인덱싱된 각 요소에 단일 수준 비트 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7c85-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="f7c85-106">한정자는 `A` 단일의 비트 연산이 adjointable을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f7c85-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachIndexA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="f7c85-107">입력</span><span class="sxs-lookup"><span data-stu-id="f7c85-107">Input</span></span>

### <a name="singleelementoperation--intt--unit--is-adj"></a><span data-ttu-id="f7c85-108">singleElementOperation: ([Int](xref:microsoft.quantum.lang-ref.int), t) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="f7c85-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="f7c85-109">각 고 비트에 적용할 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="f7c85-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="f7c85-110">등록: ' t []</span><span class="sxs-lookup"><span data-stu-id="f7c85-110">register : 'T[]</span></span>

<span data-ttu-id="f7c85-111">지정 된 작업을 적용할 대상 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f7c85-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f7c85-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f7c85-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f7c85-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f7c85-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f7c85-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="f7c85-114">'T</span></span>

<span data-ttu-id="f7c85-115">각 작업의 역할을 하는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="f7c85-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7c85-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f7c85-116">See Also</span></span>

- [<span data-ttu-id="f7c85-117">Microsoft. 양자. ApplyToEachIndex</span><span class="sxs-lookup"><span data-stu-id="f7c85-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)