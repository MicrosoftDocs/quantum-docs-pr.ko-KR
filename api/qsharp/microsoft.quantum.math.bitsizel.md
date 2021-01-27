---
uid: Microsoft.Quantum.Math.BitSizeL
title: BitSizeL 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeL
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: c94d873d7117fd2ee66226fab6d4bfc5b33bc46d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848905"
---
# <a name="bitsizel-function"></a><span data-ttu-id="d9a0b-102">BitSizeL 함수</span><span class="sxs-lookup"><span data-stu-id="d9a0b-102">BitSizeL function</span></span>

<span data-ttu-id="d9a0b-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="d9a0b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="d9a0b-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d9a0b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d9a0b-105">음수가 아닌 정수의 경우 `a` 를 나타내는 데 필요한 비트 수를 반환 `a` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="d9a0b-106">즉, $a < 2 ^ n $와 같은 가장 작은 $n $를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeL (a : BigInt) : Int
```


## <a name="input"></a><span data-ttu-id="d9a0b-107">입력</span><span class="sxs-lookup"><span data-stu-id="d9a0b-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="d9a0b-108">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d9a0b-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d9a0b-109">비트 크기를 계산할 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="d9a0b-110">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d9a0b-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d9a0b-111">의 비트 크기 `a` 입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-111">The bit-size of `a`.</span></span>