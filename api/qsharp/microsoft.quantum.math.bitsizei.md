---
uid: Microsoft.Quantum.Math.BitSizeI
title: BitSizeI 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeI
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: e7cfe03908a8a394fc8ceb1c9facbf02f3db2d48
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723196"
---
# <a name="bitsizei-function"></a><span data-ttu-id="f46fa-102">BitSizeI 함수</span><span class="sxs-lookup"><span data-stu-id="f46fa-102">BitSizeI function</span></span>

<span data-ttu-id="f46fa-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="f46fa-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="f46fa-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f46fa-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f46fa-105">음수가 아닌 정수의 경우 `a` 를 나타내는 데 필요한 비트 수를 반환 `a` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f46fa-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="f46fa-106">즉, $a < 2 ^ n $와 같은 가장 작은 $n $를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f46fa-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeI (a : Int) : Int
```


## <a name="input"></a><span data-ttu-id="f46fa-107">입력</span><span class="sxs-lookup"><span data-stu-id="f46fa-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="f46fa-108">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f46fa-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f46fa-109">비트 크기를 계산할 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="f46fa-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="f46fa-110">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f46fa-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f46fa-111">의 비트 크기 `a` 입니다.</span><span class="sxs-lookup"><span data-stu-id="f46fa-111">The bit-size of `a`.</span></span>