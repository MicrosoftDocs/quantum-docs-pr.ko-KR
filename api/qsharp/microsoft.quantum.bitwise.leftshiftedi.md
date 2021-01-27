---
uid: Microsoft.Quantum.Bitwise.LeftShiftedI
title: LeftShiftedI 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedI
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 3f551bdba5c8e2a1456838769e4cee0660d0f969
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845301"
---
# <a name="leftshiftedi-function"></a><span data-ttu-id="49225-102">LeftShiftedI 함수</span><span class="sxs-lookup"><span data-stu-id="49225-102">LeftShiftedI function</span></span>

<span data-ttu-id="49225-103">네임 스페이스: [Microsoft. 양자 비트](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="49225-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="49225-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="49225-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="49225-105">지정 된 비트 수 만큼 왼쪽에 있는 숫자의 비트 표현을 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="49225-105">Shifts the bitwise representation of a number left by a given number of bits.</span></span>

```qsharp
function LeftShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="49225-106">입력</span><span class="sxs-lookup"><span data-stu-id="49225-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="49225-107">값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="49225-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="49225-108">비트 표현이 왼쪽으로 이동 하는 숫자 (더 중요)입니다.</span><span class="sxs-lookup"><span data-stu-id="49225-108">The number whose bitwise representation is to be shifted to the left (more significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="49225-109">amount: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="49225-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="49225-110">`value`가 왼쪽으로 이동할 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="49225-110">The number of bits by which `value` is to be shifted to the left.</span></span>



## <a name="output--int"></a><span data-ttu-id="49225-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="49225-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="49225-112">의 값으로 `value` , 왼쪽으로 비트를 이동 `amount` 합니다.</span><span class="sxs-lookup"><span data-stu-id="49225-112">The value of `value`, shifted left by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="49225-113">설명</span><span class="sxs-lookup"><span data-stu-id="49225-113">Remarks</span></span>

<span data-ttu-id="49225-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="49225-114">The following are equivalent:</span></span>

```qsharp
let c = a <<< b;
let c = LeftShiftedI(a, b);
```