---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: IntegerBits 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: d6566716f5a63c090668d9582b7b000c16d1f6a5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231095"
---
# <a name="integerbits-function"></a><span data-ttu-id="f1ac1-102">IntegerBits 함수</span><span class="sxs-lookup"><span data-stu-id="f1ac1-102">IntegerBits function</span></span>

<span data-ttu-id="f1ac1-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="f1ac1-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="f1ac1-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f1ac1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f1ac1-105">정수의 비트가 설정 된 모든 위치를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ac1-105">Returns all positions in which bits of an integer are set.</span></span>

```qsharp
function IntegerBits (value : Int, length : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="f1ac1-106">입력</span><span class="sxs-lookup"><span data-stu-id="f1ac1-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="f1ac1-107">값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f1ac1-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f1ac1-108">음수가 아닌 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="f1ac1-108">A nonnegative number.</span></span>


### <a name="length--int"></a><span data-ttu-id="f1ac1-109">길이: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f1ac1-109">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f1ac1-110">의 이진 확장의 비트 수입니다 `value` .</span><span class="sxs-lookup"><span data-stu-id="f1ac1-110">The number of bits in the binary expansion of `value`.</span></span>



## <a name="output--int"></a><span data-ttu-id="f1ac1-111">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f1ac1-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f1ac1-112">모든 비트의 `value` 위치를 고려 하는 이진 확장의 1 인 모든 비트 위치 (0부터 시작)를 포함 하는 배열입니다 `length - 1` .</span><span class="sxs-lookup"><span data-stu-id="f1ac1-112">An array containing all bit positions (starting from 0) that are 1 in the binary expansion of `value` considering all bits up to position `length - 1`.</span></span>  <span data-ttu-id="f1ac1-113">모든 위치는 배열에서 오름차순으로 정렬 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1ac1-113">All positions are ordered in the array by position in an increasing order.</span></span>