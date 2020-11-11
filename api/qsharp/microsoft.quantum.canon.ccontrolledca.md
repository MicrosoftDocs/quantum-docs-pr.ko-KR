---
uid: Microsoft.Quantum.Canon.CControlledCA
title: CControlledCA 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledCA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 20a8c9ccf931261f7bc6e347ccc144c92f0d0545
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716570"
---
# <a name="ccontrolledca-function"></a><span data-ttu-id="dcc04-102">CControlledCA 함수</span><span class="sxs-lookup"><span data-stu-id="dcc04-102">CControlledCA function</span></span>

<span data-ttu-id="dcc04-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="dcc04-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="dcc04-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dcc04-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dcc04-105">작업 op가 지정 된 경우 기존 컨트롤 비트가 true 이면 op를 적용 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcc04-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="dcc04-106">이면 `false` 아무 작업도 수행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcc04-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="dcc04-107">한정자는 `CA` 작업을 제어 하 고 adjointable 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dcc04-107">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
function CControlledCA<'T> (op : ('T => Unit is Ctl + Adj)) : ((Bool, 'T) => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="dcc04-108">입력</span><span class="sxs-lookup"><span data-stu-id="dcc04-108">Input</span></span>

### <a name="op--t--unit-ctl--adj"></a><span data-ttu-id="dcc04-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span><span class="sxs-lookup"><span data-stu-id="dcc04-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="dcc04-110">조건부로 적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="dcc04-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit-ctl--adj"></a><span data-ttu-id="dcc04-111">출력: ([Bool](xref:microsoft.quantum.lang-ref.bool), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span><span class="sxs-lookup"><span data-stu-id="dcc04-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="dcc04-112">클래식 컨트롤 비트가 true 인 경우 op 인 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="dcc04-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="dcc04-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="dcc04-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dcc04-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="dcc04-114">'T</span></span>

<span data-ttu-id="dcc04-115">조건부로 적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="dcc04-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="dcc04-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="dcc04-116">See Also</span></span>

- [<span data-ttu-id="dcc04-117">Microsoft. 양자 제어</span><span class="sxs-lookup"><span data-stu-id="dcc04-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)