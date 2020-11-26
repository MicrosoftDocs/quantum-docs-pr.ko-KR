---
uid: Microsoft.Quantum.Bitwise.RightShiftedI
title: RightShiftedI 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedI
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: b20a4a8c281a470af9a4828f8a5ca905a7918723
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209777"
---
# <a name="rightshiftedi-function"></a><span data-ttu-id="38e88-102">RightShiftedI 함수</span><span class="sxs-lookup"><span data-stu-id="38e88-102">RightShiftedI function</span></span>

<span data-ttu-id="38e88-103">네임 스페이스: [Microsoft. 양자 비트](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="38e88-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="38e88-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="38e88-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="38e88-105">숫자의 비트 표현을 지정 된 비트 수 만큼 오른쪽으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e88-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="38e88-106">입력</span><span class="sxs-lookup"><span data-stu-id="38e88-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="38e88-107">값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="38e88-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="38e88-108">비트 표현이 오른쪽으로 이동 하는 숫자 (낮음)입니다.</span><span class="sxs-lookup"><span data-stu-id="38e88-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="38e88-109">amount: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="38e88-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="38e88-110">를 `value` 오른쪽으로 이동할 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="38e88-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--int"></a><span data-ttu-id="38e88-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="38e88-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="38e88-112">`value`비트 단위로 오른쪽으로 이동 하는의 값입니다 `amount` .</span><span class="sxs-lookup"><span data-stu-id="38e88-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="38e88-113">설명</span><span class="sxs-lookup"><span data-stu-id="38e88-113">Remarks</span></span>

<span data-ttu-id="38e88-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e88-114">The following are equivalent:</span></span>

```Q#
let c = a >>> b;
let c = RightShiftedI(a, b);
```