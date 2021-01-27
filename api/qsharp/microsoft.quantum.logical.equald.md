---
uid: Microsoft.Quantum.Logical.EqualD
title: EqualD 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualD
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: f8a24d7bfb9b4f7b8b0e1f68a94bfb341716b024
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98816860"
---
# <a name="equald-function"></a><span data-ttu-id="7bb1c-102">EqualD 함수</span><span class="sxs-lookup"><span data-stu-id="7bb1c-102">EqualD function</span></span>

<span data-ttu-id="7bb1c-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="7bb1c-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="7bb1c-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7bb1c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7bb1c-105">두 입력이 같으면 true를 반환 하 고,</span><span class="sxs-lookup"><span data-stu-id="7bb1c-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="7bb1c-106">입력</span><span class="sxs-lookup"><span data-stu-id="7bb1c-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="7bb1c-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7bb1c-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7bb1c-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="7bb1c-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="7bb1c-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7bb1c-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7bb1c-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="7bb1c-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="7bb1c-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="7bb1c-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7bb1c-112">`true` 가와 같으면이 고, 그렇지 않으면입니다 `a` `b` .</span><span class="sxs-lookup"><span data-stu-id="7bb1c-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bb1c-113">설명</span><span class="sxs-lookup"><span data-stu-id="7bb1c-113">Remarks</span></span>

<span data-ttu-id="7bb1c-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb1c-114">The following are equivalent:</span></span>

```qsharp
let cond = a == b;
let cond = EqualD(a, b);
```