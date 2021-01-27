---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: IntAsBoolArray 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a non-negative integer, using the little-endian representation for the returned array.
ms.openlocfilehash: 8b3d230605cc756a5da01e45e47f91c5b8e9f541
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98833315"
---
# <a name="intasboolarray-function"></a><span data-ttu-id="8b825-102">IntAsBoolArray 함수</span><span class="sxs-lookup"><span data-stu-id="8b825-102">IntAsBoolArray function</span></span>

<span data-ttu-id="8b825-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="8b825-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="8b825-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8b825-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8b825-105">반환 된 배열에 대 한 작은 endian 표현을 사용 하 여 음수가 아닌 정수의 이진 표현을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b825-105">Produces a binary representation of a non-negative integer, using the little-endian representation for the returned array.</span></span>

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="8b825-106">입력</span><span class="sxs-lookup"><span data-stu-id="8b825-106">Input</span></span>

### <a name="number--int"></a><span data-ttu-id="8b825-107">number: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8b825-107">number : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8b825-108">부울 값 배열로 변환 될 음수가 아닌 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="8b825-108">A non-negative integer to be converted to an array of boolean values.</span></span>


### <a name="bits--int"></a><span data-ttu-id="8b825-109">비트: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8b825-109">bits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8b825-110">의 이진 표현에서 비트 수입니다 `number` .</span><span class="sxs-lookup"><span data-stu-id="8b825-110">The number of bits in the binary representation of `number`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="8b825-111">Output: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="8b825-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="8b825-112">를 나타내는 부울 값의 배열입니다 `number` .</span><span class="sxs-lookup"><span data-stu-id="8b825-112">An array of boolean values representing `number`.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b825-113">설명</span><span class="sxs-lookup"><span data-stu-id="8b825-113">Remarks</span></span>

<span data-ttu-id="8b825-114">입력은 `bits` 0에서 63 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b825-114">The input `bits` must be between 0 and 63.</span></span>
<span data-ttu-id="8b825-115">입력은 `number` 0에서 $2 ^ {\texttt{bits}}-$1 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b825-115">The input `number` must be between 0 and $2^{\texttt{bits}} - 1$.</span></span>