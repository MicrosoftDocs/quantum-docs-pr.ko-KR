---
uid: Microsoft.Quantum.Canon.CControlled
title: CControlled 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlled
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens.
ms.openlocfilehash: 76e663e9a4b53c7ed74a1b70da516fb07958923b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216899"
---
# <a name="ccontrolled-function"></a><span data-ttu-id="b7ce6-102">CControlled 함수</span><span class="sxs-lookup"><span data-stu-id="b7ce6-102">CControlled function</span></span>

<span data-ttu-id="b7ce6-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b7ce6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b7ce6-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b7ce6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b7ce6-105">작업 op가 지정 된 경우 기존 컨트롤 비트가 true 이면 op를 적용 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ce6-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="b7ce6-106">이면 `false` 아무 작업도 수행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7ce6-106">If `false`, nothing happens.</span></span>

```qsharp
function CControlled<'T> (op : ('T => Unit)) : ((Bool, 'T) => Unit)
```


## <a name="input"></a><span data-ttu-id="b7ce6-107">입력</span><span class="sxs-lookup"><span data-stu-id="b7ce6-107">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="b7ce6-108">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b7ce6-108">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b7ce6-109">조건부로 적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="b7ce6-109">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit"></a><span data-ttu-id="b7ce6-110">출력: ([Bool](xref:microsoft.quantum.lang-ref.bool), t) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b7ce6-110">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b7ce6-111">클래식 컨트롤 비트가 true 인 경우 op 인 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="b7ce6-111">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b7ce6-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b7ce6-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b7ce6-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="b7ce6-113">'T</span></span>

<span data-ttu-id="b7ce6-114">조건부로 적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="b7ce6-114">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7ce6-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b7ce6-115">See Also</span></span>

- [<span data-ttu-id="b7ce6-116">Microsoft. 양자. CControlledC</span><span class="sxs-lookup"><span data-stu-id="b7ce6-116">Microsoft.Quantum.Canon.CControlledC</span></span>](xref:Microsoft.Quantum.Canon.CControlledC)
- [<span data-ttu-id="b7ce6-117">Microsoft. 양자. CControlledA</span><span class="sxs-lookup"><span data-stu-id="b7ce6-117">Microsoft.Quantum.Canon.CControlledA</span></span>](xref:Microsoft.Quantum.Canon.CControlledA)
- [<span data-ttu-id="b7ce6-118">CControlledCA입니다.</span><span class="sxs-lookup"><span data-stu-id="b7ce6-118">Microsoft.Quantum.Canon.CControlledCA</span></span>](xref:Microsoft.Quantum.Canon.CControlledCA)