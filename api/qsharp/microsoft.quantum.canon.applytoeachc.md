---
uid: Microsoft.Quantum.Canon.ApplyToEachC
title: ApplyToEachC 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachC
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: 535f815503e20b5cee35f3f273a714203a4baf12
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217784"
---
# <a name="applytoeachc-operation"></a><span data-ttu-id="be882-102">ApplyToEachC 작업</span><span class="sxs-lookup"><span data-stu-id="be882-102">ApplyToEachC operation</span></span>

<span data-ttu-id="be882-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="be882-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="be882-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="be882-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="be882-105">레지스터의 각 요소에 단일 수준 비트 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="be882-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="be882-106">한정자는 `C` 단일 비트 작업을 제어할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="be882-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachC<'T> (singleElementOperation : ('T => Unit is Ctl), register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="be882-107">입력</span><span class="sxs-lookup"><span data-stu-id="be882-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-ctl"></a><span data-ttu-id="be882-108">singleElementOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="be882-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="be882-109">각 고 비트에 적용할 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="be882-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="be882-110">등록: ' t []</span><span class="sxs-lookup"><span data-stu-id="be882-110">register : 'T[]</span></span>

<span data-ttu-id="be882-111">지정 된 작업을 적용할 대상 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="be882-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="be882-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="be882-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="be882-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="be882-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="be882-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="be882-114">'T</span></span>

<span data-ttu-id="be882-115">작업이 수행 되는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="be882-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="be882-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="be882-116">See Also</span></span>

- [<span data-ttu-id="be882-117">각각의 Microsoft 양자</span><span class="sxs-lookup"><span data-stu-id="be882-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)