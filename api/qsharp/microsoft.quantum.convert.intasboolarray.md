---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: IntAsBoolArray 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a positive integer, using the little-endian representation for the returned array.
ms.openlocfilehash: 9783a49a77bdc39ffe8c7725196eb620f4cd0100
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713455"
---
# <a name="intasboolarray-function"></a><span data-ttu-id="b8d73-102">IntAsBoolArray 함수</span><span class="sxs-lookup"><span data-stu-id="b8d73-102">IntAsBoolArray function</span></span>

<span data-ttu-id="b8d73-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="b8d73-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="b8d73-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b8d73-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b8d73-105">반환 된 배열에 대 한 작은 endian 표현을 사용 하 여 양의 정수의 이진 표현을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d73-105">Produces a binary representation of a positive integer, using the little-endian representation for the returned array.</span></span>

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="b8d73-106">입력</span><span class="sxs-lookup"><span data-stu-id="b8d73-106">Input</span></span>

### <a name="number--int"></a><span data-ttu-id="b8d73-107">number: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b8d73-107">number : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b8d73-108">부울 값의 배열로 변환할 양의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d73-108">A positive integer to be converted to an array of boolean values.</span></span>


### <a name="bits--int"></a><span data-ttu-id="b8d73-109">비트: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b8d73-109">bits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b8d73-110">의 이진 표현에서 비트 수입니다 `number` .</span><span class="sxs-lookup"><span data-stu-id="b8d73-110">The number of bits in the binary representation of `number`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="b8d73-111">Output: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="b8d73-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="b8d73-112">를 나타내는 부울 값의 배열입니다 `number` .</span><span class="sxs-lookup"><span data-stu-id="b8d73-112">An array of boolean values representing `number`.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8d73-113">설명</span><span class="sxs-lookup"><span data-stu-id="b8d73-113">Remarks</span></span>

<span data-ttu-id="b8d73-114">입력은 `bits` 0에서 63 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d73-114">The input `bits` must be between 0 and 63.</span></span>
<span data-ttu-id="b8d73-115">입력은 `number` 0에서 $2 ^ {\texttt{bits}}-$1 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d73-115">The input `number` must be between 0 and $2^{\texttt{bits}} - 1$.</span></span>