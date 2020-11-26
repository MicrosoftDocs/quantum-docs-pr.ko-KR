---
uid: Microsoft.Quantum.Math.PNorm
title: PNorm 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNorm
qsharp.summary: >-
  Returns the `L(p)` norm of a vector of `Double`s.

  That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.
ms.openlocfilehash: 3fe029bd893fc4d11aaf351f7ea566256cac5a9e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194732"
---
# <a name="pnorm-function"></a><span data-ttu-id="81a10-102">PNorm 함수</span><span class="sxs-lookup"><span data-stu-id="81a10-102">PNorm function</span></span>

<span data-ttu-id="81a10-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="81a10-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="81a10-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="81a10-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="81a10-105">`L(p)`S 벡터의 표준을 반환 합니다 `Double` .</span><span class="sxs-lookup"><span data-stu-id="81a10-105">Returns the `L(p)` norm of a vector of `Double`s.</span></span>

<span data-ttu-id="81a10-106">즉, 형식의 $x $ 배열을 지정 하면 `Double[]` $-ad$ \| x \| \_ p = (\ sum_ {j} | x_j | ^ {p}) ^ {1/p} $ $p 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-106">That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.</span></span>

```qsharp
function PNorm (p : Double, array : Double[]) : Double
```


## <a name="input"></a><span data-ttu-id="81a10-107">입력</span><span class="sxs-lookup"><span data-stu-id="81a10-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="81a10-108">p: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="81a10-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="81a10-109">$P $-일반의 지 수 $p입니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="81a10-110">array: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="81a10-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="81a10-111">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="81a10-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="81a10-112">$P $-일반 $ \| x \| _p $입니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-112">The $p$-norm $\|x\|_p$.</span></span>