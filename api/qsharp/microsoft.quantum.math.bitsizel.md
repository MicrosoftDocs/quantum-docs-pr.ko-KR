---
uid: Microsoft.Quantum.Math.BitSizeL
title: BitSizeL 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeL
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: 97068f12050317a9aa17c95f33650ef6f406066d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723189"
---
# <a name="bitsizel-function"></a><span data-ttu-id="966ea-102">BitSizeL 함수</span><span class="sxs-lookup"><span data-stu-id="966ea-102">BitSizeL function</span></span>

<span data-ttu-id="966ea-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="966ea-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="966ea-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="966ea-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="966ea-105">음수가 아닌 정수의 경우 `a` 를 나타내는 데 필요한 비트 수를 반환 `a` 합니다.</span><span class="sxs-lookup"><span data-stu-id="966ea-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="966ea-106">즉, $a < 2 ^ n $와 같은 가장 작은 $n $를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="966ea-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeL (a : BigInt) : Int
```


## <a name="input"></a><span data-ttu-id="966ea-107">입력</span><span class="sxs-lookup"><span data-stu-id="966ea-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="966ea-108">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="966ea-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="966ea-109">비트 크기를 계산할 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="966ea-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="966ea-110">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="966ea-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="966ea-111">의 비트 크기 `a` 입니다.</span><span class="sxs-lookup"><span data-stu-id="966ea-111">The bit-size of `a`.</span></span>