---
uid: Microsoft.Quantum.Logical.Conditioned
title: 조건 화 된 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: c0f55d4db95ad1f0d2b7f291cbc6ba8ae704cb81
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198489"
---
# <a name="conditioned-function"></a><span data-ttu-id="bbcb0-102">조건 화 된 함수</span><span class="sxs-lookup"><span data-stu-id="bbcb0-102">Conditioned function</span></span>

<span data-ttu-id="bbcb0-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="bbcb0-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="bbcb0-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bbcb0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bbcb0-105">부울 조건 값에 따라 두 값 중 하나를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbcb0-105">Returns one of two values, depending on the value of a Boolean condition.</span></span>

```qsharp
function Conditioned<'T> (condition : Bool, ifTrue : 'T, ifFalse : 'T) : 'T
```


## <a name="input"></a><span data-ttu-id="bbcb0-106">입력</span><span class="sxs-lookup"><span data-stu-id="bbcb0-106">Input</span></span>

### <a name="condition--bool"></a><span data-ttu-id="bbcb0-107">조건: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="bbcb0-107">condition : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="bbcb0-108">반환 되는 입력을 제어 하는 데 사용 되는 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="bbcb0-108">A condition used to control which input is returned.</span></span>


### <a name="iftrue--t"></a><span data-ttu-id="bbcb0-109">ifTrue: ' '</span><span class="sxs-lookup"><span data-stu-id="bbcb0-109">ifTrue : 'T</span></span>

<span data-ttu-id="bbcb0-110">가 인 경우 반환 될 값 `condition` 입니다 `true` .</span><span class="sxs-lookup"><span data-stu-id="bbcb0-110">The value to be returned when `condition` is `true`.</span></span>


### <a name="iffalse--t"></a><span data-ttu-id="bbcb0-111">ifFalse: ' '</span><span class="sxs-lookup"><span data-stu-id="bbcb0-111">ifFalse : 'T</span></span>

<span data-ttu-id="bbcb0-112">가 인 경우 반환 될 값 `condition` 입니다 `false` .</span><span class="sxs-lookup"><span data-stu-id="bbcb0-112">The value to be returned when `condition` is `false`.</span></span>



## <a name="output--t"></a><span data-ttu-id="bbcb0-113">출력: ' '</span><span class="sxs-lookup"><span data-stu-id="bbcb0-113">Output : 'T</span></span>

<span data-ttu-id="bbcb0-114">`ifTrue``condition`가 이면이 `true` 고, `ifFalse` 그렇지 않으면입니다.</span><span class="sxs-lookup"><span data-stu-id="bbcb0-114">`ifTrue` if `condition` is `true`, and `ifFalse` otherwise.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="bbcb0-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="bbcb0-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bbcb0-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="bbcb0-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="bbcb0-117">설명</span><span class="sxs-lookup"><span data-stu-id="bbcb0-117">Remarks</span></span>

<span data-ttu-id="bbcb0-118">연산자와 달리 `?|` 이 함수는 두 입력이 모두 완전히 계산 되도록 하는 짧은 회로는 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="bbcb0-118">Unlike the `?|` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="bbcb0-119">단기 동작으로, 다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbcb0-119">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```