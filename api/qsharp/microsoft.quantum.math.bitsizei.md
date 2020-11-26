---
uid: Microsoft.Quantum.Math.BitSizeI
title: BitSizeI 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeI
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: 561450ef43144aa4d7820e1f15d9300018104acd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195854"
---
# <a name="bitsizei-function"></a><span data-ttu-id="43e72-102">BitSizeI 함수</span><span class="sxs-lookup"><span data-stu-id="43e72-102">BitSizeI function</span></span>

<span data-ttu-id="43e72-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="43e72-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="43e72-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="43e72-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="43e72-105">음수가 아닌 정수의 경우 `a` 를 나타내는 데 필요한 비트 수를 반환 `a` 합니다.</span><span class="sxs-lookup"><span data-stu-id="43e72-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="43e72-106">즉, $a < 2 ^ n $와 같은 가장 작은 $n $를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="43e72-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeI (a : Int) : Int
```


## <a name="input"></a><span data-ttu-id="43e72-107">입력</span><span class="sxs-lookup"><span data-stu-id="43e72-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="43e72-108">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="43e72-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="43e72-109">비트 크기를 계산할 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="43e72-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="43e72-110">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="43e72-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="43e72-111">의 비트 크기 `a` 입니다.</span><span class="sxs-lookup"><span data-stu-id="43e72-111">The bit-size of `a`.</span></span>