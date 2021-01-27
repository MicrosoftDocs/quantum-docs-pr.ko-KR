---
uid: Microsoft.Quantum.Logical.Not
title: Not 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: bf09cac8d126371df6218b7e92d68a881b732dc8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849084"
---
# <a name="not-function"></a><span data-ttu-id="55436-102">Not 함수</span><span class="sxs-lookup"><span data-stu-id="55436-102">Not function</span></span>

<span data-ttu-id="55436-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="55436-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="55436-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="55436-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="55436-105">값의 부울 부정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="55436-105">Returns the Boolean negation of a value.</span></span>

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="55436-106">입력</span><span class="sxs-lookup"><span data-stu-id="55436-106">Input</span></span>

### <a name="value--bool"></a><span data-ttu-id="55436-107">값: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="55436-107">value : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="55436-108">부정할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="55436-108">The value to be negated.</span></span>



## <a name="output--bool"></a><span data-ttu-id="55436-109">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="55436-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="55436-110">`true` 가 이면이 고, 그렇지 않으면 `value` `false` 입니다.</span><span class="sxs-lookup"><span data-stu-id="55436-110">`true` if and only if `value` is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="55436-111">설명</span><span class="sxs-lookup"><span data-stu-id="55436-111">Remarks</span></span>

<span data-ttu-id="55436-112">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="55436-112">The following are equivalent:</span></span>

```qsharp
let x = not value;
let x = Not(value);
```