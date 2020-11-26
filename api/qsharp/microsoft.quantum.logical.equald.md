---
uid: Microsoft.Quantum.Logical.EqualD
title: EqualD 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualD
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: d6731b293ba402f5cd43591d3c2bcd258e8ebe32
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198149"
---
# <a name="equald-function"></a><span data-ttu-id="49330-102">EqualD 함수</span><span class="sxs-lookup"><span data-stu-id="49330-102">EqualD function</span></span>

<span data-ttu-id="49330-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="49330-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="49330-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="49330-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="49330-105">두 입력이 같으면 true를 반환 하 고,</span><span class="sxs-lookup"><span data-stu-id="49330-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="49330-106">입력</span><span class="sxs-lookup"><span data-stu-id="49330-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="49330-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="49330-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="49330-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="49330-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="49330-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="49330-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="49330-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="49330-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="49330-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="49330-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="49330-112">`true` 가와 같으면이 고, 그렇지 않으면입니다 `a` `b` .</span><span class="sxs-lookup"><span data-stu-id="49330-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="49330-113">설명</span><span class="sxs-lookup"><span data-stu-id="49330-113">Remarks</span></span>

<span data-ttu-id="49330-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="49330-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualD(a, b);
```