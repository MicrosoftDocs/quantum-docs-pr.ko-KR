---
uid: Microsoft.Quantum.Logical.Not
title: Not 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: 3a688aac0178a2f4127496c1009fe7d5ee7ae198
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709864"
---
# <a name="not-function"></a><span data-ttu-id="d9d64-102">Not 함수</span><span class="sxs-lookup"><span data-stu-id="d9d64-102">Not function</span></span>

<span data-ttu-id="d9d64-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="d9d64-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="d9d64-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d9d64-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d9d64-105">값의 부울 부정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d64-105">Returns the Boolean negation of a value.</span></span>

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="d9d64-106">입력</span><span class="sxs-lookup"><span data-stu-id="d9d64-106">Input</span></span>

### <a name="value--bool"></a><span data-ttu-id="d9d64-107">값: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d9d64-107">value : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d9d64-108">부정할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d9d64-108">The value to be negated.</span></span>



## <a name="output--bool"></a><span data-ttu-id="d9d64-109">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d9d64-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d9d64-110">`true` 가 이면이 고, 그렇지 않으면 `value` `false` 입니다.</span><span class="sxs-lookup"><span data-stu-id="d9d64-110">`true` if and only if `value` is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9d64-111">설명</span><span class="sxs-lookup"><span data-stu-id="d9d64-111">Remarks</span></span>

<span data-ttu-id="d9d64-112">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d64-112">The following are equivalent:</span></span>

```Q#
let x = not value;
let x = Not(value);
```