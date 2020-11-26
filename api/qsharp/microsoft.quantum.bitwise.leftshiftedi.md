---
uid: Microsoft.Quantum.Bitwise.LeftShiftedI
title: LeftShiftedI 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedI
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 3a7220489bfa241e2337df14291bafb1d6e0e19e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209862"
---
# <a name="leftshiftedi-function"></a><span data-ttu-id="b8f7f-102">LeftShiftedI 함수</span><span class="sxs-lookup"><span data-stu-id="b8f7f-102">LeftShiftedI function</span></span>

<span data-ttu-id="b8f7f-103">네임 스페이스: [Microsoft. 양자 비트](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="b8f7f-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="b8f7f-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b8f7f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b8f7f-105">지정 된 비트 수 만큼 왼쪽에 있는 숫자의 비트 표현을 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8f7f-105">Shifts the bitwise representation of a number left by a given number of bits.</span></span>

```qsharp
function LeftShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="b8f7f-106">입력</span><span class="sxs-lookup"><span data-stu-id="b8f7f-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="b8f7f-107">값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b8f7f-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b8f7f-108">비트 표현이 왼쪽으로 이동 하는 숫자 (더 중요)입니다.</span><span class="sxs-lookup"><span data-stu-id="b8f7f-108">The number whose bitwise representation is to be shifted to the left (more significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="b8f7f-109">amount: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b8f7f-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b8f7f-110">`value`가 왼쪽으로 이동할 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b8f7f-110">The number of bits by which `value` is to be shifted to the left.</span></span>



## <a name="output--int"></a><span data-ttu-id="b8f7f-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b8f7f-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b8f7f-112">의 값으로 `value` , 왼쪽으로 비트를 이동 `amount` 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8f7f-112">The value of `value`, shifted left by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8f7f-113">설명</span><span class="sxs-lookup"><span data-stu-id="b8f7f-113">Remarks</span></span>

<span data-ttu-id="b8f7f-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8f7f-114">The following are equivalent:</span></span>

```Q#
let c = a <<< b;
let c = LeftShiftedI(a, b);
```