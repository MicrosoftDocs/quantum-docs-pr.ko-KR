---
uid: Microsoft.Quantum.Logical.Conditioned
title: 조건 화 된 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: 8aabe8b018129ddee3b934c207d0a62e59fb6f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720788"
---
# <a name="conditioned-function"></a><span data-ttu-id="a4a22-102">조건 화 된 함수</span><span class="sxs-lookup"><span data-stu-id="a4a22-102">Conditioned function</span></span>

<span data-ttu-id="a4a22-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a4a22-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a4a22-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a4a22-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a4a22-105">부울 조건 값에 따라 두 값 중 하나를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a22-105">Returns one of two values, depending on the value of a Boolean condition.</span></span>

```qsharp
function Conditioned<'T> (condition : Bool, ifTrue : 'T, ifFalse : 'T) : 'T
```


## <a name="input"></a><span data-ttu-id="a4a22-106">입력</span><span class="sxs-lookup"><span data-stu-id="a4a22-106">Input</span></span>

### <a name="condition--bool"></a><span data-ttu-id="a4a22-107">조건: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a4a22-107">condition : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a4a22-108">반환 되는 입력을 제어 하는 데 사용 되는 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="a4a22-108">A condition used to control which input is returned.</span></span>


### <a name="iftrue--t"></a><span data-ttu-id="a4a22-109">ifTrue: ' '</span><span class="sxs-lookup"><span data-stu-id="a4a22-109">ifTrue : 'T</span></span>

<span data-ttu-id="a4a22-110">가 인 경우 반환 될 값 `condition` 입니다 `true` .</span><span class="sxs-lookup"><span data-stu-id="a4a22-110">The value to be returned when `condition` is `true`.</span></span>


### <a name="iffalse--t"></a><span data-ttu-id="a4a22-111">ifFalse: ' '</span><span class="sxs-lookup"><span data-stu-id="a4a22-111">ifFalse : 'T</span></span>

<span data-ttu-id="a4a22-112">가 인 경우 반환 될 값 `condition` 입니다 `false` .</span><span class="sxs-lookup"><span data-stu-id="a4a22-112">The value to be returned when `condition` is `false`.</span></span>



## <a name="output--t"></a><span data-ttu-id="a4a22-113">출력: ' '</span><span class="sxs-lookup"><span data-stu-id="a4a22-113">Output : 'T</span></span>

<span data-ttu-id="a4a22-114">`ifTrue``condition`가 이면이 `true` 고, `ifFalse` 그렇지 않으면입니다.</span><span class="sxs-lookup"><span data-stu-id="a4a22-114">`ifTrue` if `condition` is `true`, and `ifFalse` otherwise.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a4a22-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a4a22-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a4a22-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="a4a22-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="a4a22-117">설명</span><span class="sxs-lookup"><span data-stu-id="a4a22-117">Remarks</span></span>

<span data-ttu-id="a4a22-118">연산자와 달리 `?|` 이 함수는 두 입력이 모두 완전히 계산 되도록 하는 짧은 회로는 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="a4a22-118">Unlike the `?|` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="a4a22-119">단기 동작으로, 다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a22-119">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```