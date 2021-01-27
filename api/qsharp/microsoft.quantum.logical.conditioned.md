---
uid: Microsoft.Quantum.Logical.Conditioned
title: 조건 화 된 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: ea3b8eba960acceb6540978c6fccd9f796b0f67d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817297"
---
# <a name="conditioned-function"></a><span data-ttu-id="66efa-102">조건 화 된 함수</span><span class="sxs-lookup"><span data-stu-id="66efa-102">Conditioned function</span></span>

<span data-ttu-id="66efa-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="66efa-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="66efa-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="66efa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="66efa-105">부울 조건 값에 따라 두 값 중 하나를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="66efa-105">Returns one of two values, depending on the value of a Boolean condition.</span></span>

```qsharp
function Conditioned<'T> (condition : Bool, ifTrue : 'T, ifFalse : 'T) : 'T
```


## <a name="input"></a><span data-ttu-id="66efa-106">입력</span><span class="sxs-lookup"><span data-stu-id="66efa-106">Input</span></span>

### <a name="condition--bool"></a><span data-ttu-id="66efa-107">조건: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="66efa-107">condition : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="66efa-108">반환 되는 입력을 제어 하는 데 사용 되는 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="66efa-108">A condition used to control which input is returned.</span></span>


### <a name="iftrue--t"></a><span data-ttu-id="66efa-109">ifTrue: ' '</span><span class="sxs-lookup"><span data-stu-id="66efa-109">ifTrue : 'T</span></span>

<span data-ttu-id="66efa-110">가 인 경우 반환 될 값 `condition` 입니다 `true` .</span><span class="sxs-lookup"><span data-stu-id="66efa-110">The value to be returned when `condition` is `true`.</span></span>


### <a name="iffalse--t"></a><span data-ttu-id="66efa-111">ifFalse: ' '</span><span class="sxs-lookup"><span data-stu-id="66efa-111">ifFalse : 'T</span></span>

<span data-ttu-id="66efa-112">가 인 경우 반환 될 값 `condition` 입니다 `false` .</span><span class="sxs-lookup"><span data-stu-id="66efa-112">The value to be returned when `condition` is `false`.</span></span>



## <a name="output--t"></a><span data-ttu-id="66efa-113">출력: ' '</span><span class="sxs-lookup"><span data-stu-id="66efa-113">Output : 'T</span></span>

<span data-ttu-id="66efa-114">`ifTrue``condition`가 이면이 `true` 고, `ifFalse` 그렇지 않으면입니다.</span><span class="sxs-lookup"><span data-stu-id="66efa-114">`ifTrue` if `condition` is `true`, and `ifFalse` otherwise.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="66efa-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="66efa-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="66efa-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="66efa-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="66efa-117">설명</span><span class="sxs-lookup"><span data-stu-id="66efa-117">Remarks</span></span>

<span data-ttu-id="66efa-118">연산자와 달리 `?|` 이 함수는 두 입력이 모두 완전히 계산 되도록 하는 짧은 회로는 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="66efa-118">Unlike the `?|` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="66efa-119">단기 동작으로, 다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="66efa-119">Up to short-circuiting behavior, the following are equivalent:</span></span>

```qsharp
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```