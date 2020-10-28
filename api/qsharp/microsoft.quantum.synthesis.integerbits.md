---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: IntegerBits 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: ab459cd841cdac116cf0e98c094834f628b6a2d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719845"
---
# <a name="integerbits-function"></a><span data-ttu-id="81606-102">IntegerBits 함수</span><span class="sxs-lookup"><span data-stu-id="81606-102">IntegerBits function</span></span>

<span data-ttu-id="81606-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="81606-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="81606-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="81606-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="81606-105">정수의 비트가 설정 된 모든 위치를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="81606-105">Returns all positions in which bits of an integer are set.</span></span>

```qsharp
function IntegerBits (value : Int, length : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="81606-106">입력</span><span class="sxs-lookup"><span data-stu-id="81606-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="81606-107">값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="81606-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="81606-108">음수가 아닌 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="81606-108">A nonnegative number.</span></span>


### <a name="length--int"></a><span data-ttu-id="81606-109">길이: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="81606-109">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="81606-110">의 이진 확장의 비트 수입니다 `value` .</span><span class="sxs-lookup"><span data-stu-id="81606-110">The number of bits in the binary expansion of `value`.</span></span>



## <a name="output--int"></a><span data-ttu-id="81606-111">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="81606-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="81606-112">모든 비트의 `value` 위치를 고려 하는 이진 확장의 1 인 모든 비트 위치 (0부터 시작)를 포함 하는 배열입니다 `length - 1` .</span><span class="sxs-lookup"><span data-stu-id="81606-112">An array containing all bit positions (starting from 0) that are 1 in the binary expansion of `value` considering all bits up to position `length - 1`.</span></span>  <span data-ttu-id="81606-113">모든 위치는 배열에서 오름차순으로 정렬 됩니다.</span><span class="sxs-lookup"><span data-stu-id="81606-113">All positions are ordered in the array by position in an increasing order.</span></span>