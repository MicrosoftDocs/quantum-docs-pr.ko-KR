---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: ConstantArray 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: a3ad8a18856888a0ca6f9dd691242156b0c044d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846239"
---
# <a name="constantarray-function"></a><span data-ttu-id="f0b0b-102">ConstantArray 함수</span><span class="sxs-lookup"><span data-stu-id="f0b0b-102">ConstantArray function</span></span>

<span data-ttu-id="f0b0b-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f0b0b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f0b0b-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f0b0b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f0b0b-105">모든 요소가 지정 된 값과 같은 지정 된 길이의 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-105">Creates an array of given length with all elements equal to given value.</span></span>

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a><span data-ttu-id="f0b0b-106">입력</span><span class="sxs-lookup"><span data-stu-id="f0b0b-106">Input</span></span>

### <a name="length--int"></a><span data-ttu-id="f0b0b-107">길이: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f0b0b-107">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f0b0b-108">새 배열의 길이입니다.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-108">Length of the new array.</span></span>


### <a name="value--t"></a><span data-ttu-id="f0b0b-109">값: ' '</span><span class="sxs-lookup"><span data-stu-id="f0b0b-109">value : 'T</span></span>

<span data-ttu-id="f0b0b-110">새 배열의 각 요소에 대 한 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-110">The value of each element of the new array.</span></span>



## <a name="output--t"></a><span data-ttu-id="f0b0b-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="f0b0b-111">Output : 'T[]</span></span>

<span data-ttu-id="f0b0b-112">모든 요소가 인 새 길이 배열입니다 `length` `value` .</span><span class="sxs-lookup"><span data-stu-id="f0b0b-112">A new array of length `length`, such that every element is `value`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f0b0b-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f0b0b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f0b0b-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="f0b0b-114">'T</span></span>



## <a name="example"></a><span data-ttu-id="f0b0b-115">예</span><span class="sxs-lookup"><span data-stu-id="f0b0b-115">Example</span></span>

<span data-ttu-id="f0b0b-116">다음 코드는 각각와 같은 3 개의 부울 값 배열을 만듭니다 `true` .</span><span class="sxs-lookup"><span data-stu-id="f0b0b-116">The following code creates an array of 3 Boolean values, each equal to `true`:</span></span>

```qsharp
let array = ConstantArray(3, true);
```