---
uid: Microsoft.Quantum.Canon.CControlledA
title: CControlledA 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 30b5e3408fa6e5a79b2f3d63cccc11899c0405ef
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716584"
---
# <a name="ccontrolleda-function"></a><span data-ttu-id="8be15-102">CControlledA 함수</span><span class="sxs-lookup"><span data-stu-id="8be15-102">CControlledA function</span></span>

<span data-ttu-id="8be15-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8be15-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8be15-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8be15-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8be15-105">작업 op가 지정 된 경우 기존 컨트롤 비트가 true 이면 op를 적용 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8be15-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="8be15-106">이면 `false` 아무 작업도 수행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8be15-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="8be15-107">한정자는 `A` 작업이 adjointable를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8be15-107">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
function CControlledA<'T> (op : ('T => Unit is Adj)) : ((Bool, 'T) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="8be15-108">입력</span><span class="sxs-lookup"><span data-stu-id="8be15-108">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="8be15-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="8be15-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="8be15-110">조건부로 적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="8be15-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit-adj"></a><span data-ttu-id="8be15-111">출력: ([Bool](xref:microsoft.quantum.lang-ref.bool), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="8be15-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="8be15-112">클래식 컨트롤 비트가 true 인 경우 op 인 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="8be15-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8be15-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8be15-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8be15-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="8be15-114">'T</span></span>

<span data-ttu-id="8be15-115">조건부로 적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8be15-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="8be15-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="8be15-116">See Also</span></span>

- [<span data-ttu-id="8be15-117">Microsoft. 양자 제어</span><span class="sxs-lookup"><span data-stu-id="8be15-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)