---
uid: Microsoft.Quantum.Canon.CControlledCA
title: CControlledCA 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledCA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: cc1a783dfbf97afae50f4b42e66cba2b2a2ec833
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207431"
---
# <a name="ccontrolledca-function"></a><span data-ttu-id="a8ebc-102">CControlledCA 함수</span><span class="sxs-lookup"><span data-stu-id="a8ebc-102">CControlledCA function</span></span>

<span data-ttu-id="a8ebc-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a8ebc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a8ebc-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a8ebc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a8ebc-105">작업 op가 지정 된 경우 기존 컨트롤 비트가 true 이면 op를 적용 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8ebc-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="a8ebc-106">이면 `false` 아무 작업도 수행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8ebc-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="a8ebc-107">한정자는 `CA` 작업을 제어 하 고 adjointable 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a8ebc-107">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
function CControlledCA<'T> (op : ('T => Unit is Ctl + Adj)) : ((Bool, 'T) => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="a8ebc-108">입력</span><span class="sxs-lookup"><span data-stu-id="a8ebc-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="a8ebc-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="a8ebc-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a8ebc-110">조건부로 적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a8ebc-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit--is-adj--ctl"></a><span data-ttu-id="a8ebc-111">출력: ([Bool](xref:microsoft.quantum.lang-ref.bool), t) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="a8ebc-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a8ebc-112">클래식 컨트롤 비트가 true 인 경우 op 인 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a8ebc-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a8ebc-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a8ebc-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a8ebc-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="a8ebc-114">'T</span></span>

<span data-ttu-id="a8ebc-115">조건부로 적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a8ebc-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="a8ebc-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a8ebc-116">See Also</span></span>

- [<span data-ttu-id="a8ebc-117">Microsoft. 양자 제어</span><span class="sxs-lookup"><span data-stu-id="a8ebc-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)