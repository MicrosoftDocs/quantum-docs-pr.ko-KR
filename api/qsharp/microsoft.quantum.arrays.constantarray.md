---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: ConstantArray 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: 848f18944829d08a10ec602dcb5d99c100c81f76
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719413"
---
# <a name="constantarray-function"></a><span data-ttu-id="8e084-102">ConstantArray 함수</span><span class="sxs-lookup"><span data-stu-id="8e084-102">ConstantArray function</span></span>

<span data-ttu-id="8e084-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8e084-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8e084-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8e084-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8e084-105">모든 요소가 지정 된 값과 같은 지정 된 길이의 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8e084-105">Creates an array of given length with all elements equal to given value.</span></span>

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a><span data-ttu-id="8e084-106">입력</span><span class="sxs-lookup"><span data-stu-id="8e084-106">Input</span></span>

### <a name="length--int"></a><span data-ttu-id="8e084-107">길이: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8e084-107">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8e084-108">새 배열의 길이입니다.</span><span class="sxs-lookup"><span data-stu-id="8e084-108">Length of the new array.</span></span>


### <a name="value--t"></a><span data-ttu-id="8e084-109">값: ' '</span><span class="sxs-lookup"><span data-stu-id="8e084-109">value : 'T</span></span>

<span data-ttu-id="8e084-110">새 배열의 각 요소에 대 한 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8e084-110">The value of each element of the new array.</span></span>



## <a name="output--t"></a><span data-ttu-id="8e084-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="8e084-111">Output : 'T[]</span></span>

<span data-ttu-id="8e084-112">모든 요소가 인 새 길이 배열입니다 `length` `value` .</span><span class="sxs-lookup"><span data-stu-id="8e084-112">A new array of length `length`, such that every element is `value`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8e084-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8e084-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8e084-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="8e084-114">'T</span></span>

