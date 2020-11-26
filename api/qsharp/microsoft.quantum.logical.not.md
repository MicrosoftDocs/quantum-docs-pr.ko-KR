---
uid: Microsoft.Quantum.Logical.Not
title: Not 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: f2db43f4a2ce83d8cad1d60aa8c481a33b0c7d44
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197452"
---
# <a name="not-function"></a><span data-ttu-id="6796c-102">Not 함수</span><span class="sxs-lookup"><span data-stu-id="6796c-102">Not function</span></span>

<span data-ttu-id="6796c-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="6796c-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="6796c-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6796c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6796c-105">값의 부울 부정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6796c-105">Returns the Boolean negation of a value.</span></span>

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="6796c-106">입력</span><span class="sxs-lookup"><span data-stu-id="6796c-106">Input</span></span>

### <a name="value--bool"></a><span data-ttu-id="6796c-107">값: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6796c-107">value : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6796c-108">부정할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="6796c-108">The value to be negated.</span></span>



## <a name="output--bool"></a><span data-ttu-id="6796c-109">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6796c-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6796c-110">`true` 가 이면이 고, 그렇지 않으면 `value` `false` 입니다.</span><span class="sxs-lookup"><span data-stu-id="6796c-110">`true` if and only if `value` is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="6796c-111">설명</span><span class="sxs-lookup"><span data-stu-id="6796c-111">Remarks</span></span>

<span data-ttu-id="6796c-112">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="6796c-112">The following are equivalent:</span></span>

```Q#
let x = not value;
let x = Not(value);
```