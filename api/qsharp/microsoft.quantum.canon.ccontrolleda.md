---
uid: Microsoft.Quantum.Canon.CControlledA
title: CControlledA 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: cb72ca5b3dab99b9ee8a994ba9fde46e0eae5594
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207516"
---
# <a name="ccontrolleda-function"></a><span data-ttu-id="e8d9c-102">CControlledA 함수</span><span class="sxs-lookup"><span data-stu-id="e8d9c-102">CControlledA function</span></span>

<span data-ttu-id="e8d9c-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e8d9c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e8d9c-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e8d9c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e8d9c-105">작업 op가 지정 된 경우 기존 컨트롤 비트가 true 이면 op를 적용 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d9c-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="e8d9c-106">이면 `false` 아무 작업도 수행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8d9c-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="e8d9c-107">한정자는 `A` 작업이 adjointable를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e8d9c-107">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
function CControlledA<'T> (op : ('T => Unit is Adj)) : ((Bool, 'T) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="e8d9c-108">입력</span><span class="sxs-lookup"><span data-stu-id="e8d9c-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="e8d9c-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="e8d9c-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e8d9c-110">조건부로 적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="e8d9c-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit--is-adj"></a><span data-ttu-id="e8d9c-111">출력: ([Bool](xref:microsoft.quantum.lang-ref.bool), t) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="e8d9c-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e8d9c-112">클래식 컨트롤 비트가 true 인 경우 op 인 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="e8d9c-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e8d9c-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e8d9c-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e8d9c-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="e8d9c-114">'T</span></span>

<span data-ttu-id="e8d9c-115">조건부로 적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e8d9c-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8d9c-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e8d9c-116">See Also</span></span>

- [<span data-ttu-id="e8d9c-117">Microsoft. 양자 제어</span><span class="sxs-lookup"><span data-stu-id="e8d9c-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)