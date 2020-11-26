---
uid: Microsoft.Quantum.Bitwise.RightShiftedL
title: RightShiftedL 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedL
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 3d941e1a0bcd96fe54ab01019293d883f11547a1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219518"
---
# <a name="rightshiftedl-function"></a><span data-ttu-id="303ce-102">RightShiftedL 함수</span><span class="sxs-lookup"><span data-stu-id="303ce-102">RightShiftedL function</span></span>

<span data-ttu-id="303ce-103">네임 스페이스: [Microsoft. 양자 비트](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="303ce-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="303ce-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="303ce-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="303ce-105">숫자의 비트 표현을 지정 된 비트 수 만큼 오른쪽으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="303ce-106">입력</span><span class="sxs-lookup"><span data-stu-id="303ce-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="303ce-107">값: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="303ce-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="303ce-108">비트 표현이 오른쪽으로 이동 하는 숫자 (낮음)입니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="303ce-109">amount: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="303ce-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="303ce-110">를 `value` 오른쪽으로 이동할 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="303ce-111">출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="303ce-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="303ce-112">`value`비트 단위로 오른쪽으로 이동 하는의 값입니다 `amount` .</span><span class="sxs-lookup"><span data-stu-id="303ce-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="303ce-113">설명</span><span class="sxs-lookup"><span data-stu-id="303ce-113">Remarks</span></span>

<span data-ttu-id="303ce-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-114">The following are equivalent:</span></span>

```Q#
let c = a >>> b;
let c = RightShiftedL(a, b);
```