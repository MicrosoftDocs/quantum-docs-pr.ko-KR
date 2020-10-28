---
uid: Microsoft.Quantum.Canon.ApplyToEachC
title: ApplyToEachC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachC
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: dfa18b6eb7a2c42fa2982994a2fc92170b52599c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717564"
---
# <a name="applytoeachc-operation"></a><span data-ttu-id="f0244-102">ApplyToEachC 작업</span><span class="sxs-lookup"><span data-stu-id="f0244-102">ApplyToEachC operation</span></span>

<span data-ttu-id="f0244-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f0244-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f0244-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f0244-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f0244-105">레지스터의 각 요소에 단일 수준 비트 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0244-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="f0244-106">한정자는 `C` 단일 비트 작업을 제어할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f0244-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachC<'T> (singleElementOperation : ('T => Unit is Ctl), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="f0244-107">입력</span><span class="sxs-lookup"><span data-stu-id="f0244-107">Input</span></span>

### <a name="singleelementoperation--t--unit-ctl"></a><span data-ttu-id="f0244-108">singleElementOperation: ' ' => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="f0244-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="f0244-109">각 고 비트에 적용할 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="f0244-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="f0244-110">등록: ' t []</span><span class="sxs-lookup"><span data-stu-id="f0244-110">register : 'T[]</span></span>

<span data-ttu-id="f0244-111">지정 된 작업을 적용할 대상 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f0244-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f0244-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f0244-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f0244-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f0244-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f0244-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="f0244-114">'T</span></span>

<span data-ttu-id="f0244-115">작업이 수행 되는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="f0244-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0244-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f0244-116">See Also</span></span>

- [<span data-ttu-id="f0244-117">각각의 Microsoft 양자</span><span class="sxs-lookup"><span data-stu-id="f0244-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)