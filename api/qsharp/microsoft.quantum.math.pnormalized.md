---
uid: Microsoft.Quantum.Math.PNormalized
title: PNormalized 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: ea6a88d07d3b246f666b793f0b10ab6598ea4ff6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854844"
---
# <a name="pnormalized-function"></a><span data-ttu-id="42145-102">PNormalized 함수</span><span class="sxs-lookup"><span data-stu-id="42145-102">PNormalized function</span></span>

<span data-ttu-id="42145-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="42145-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="42145-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="42145-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="42145-105">일반에서의 벡터를 정규화 `Double` `L(p)` 합니다.</span><span class="sxs-lookup"><span data-stu-id="42145-105">Normalizes a vector of `Double`s in the `L(p)` norm.</span></span>

<span data-ttu-id="42145-106">즉, 형식의 $x $ 배열이 지정 된 경우 `Double[]` 모든 요소가 $-일반 $ x _p $ $p으로 나뉘는 배열을 반환 \| \| 합니다.</span><span class="sxs-lookup"><span data-stu-id="42145-106">That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.</span></span>

```qsharp
function PNormalized (p : Double, array : Double[]) : Double[]
```


## <a name="input"></a><span data-ttu-id="42145-107">입력</span><span class="sxs-lookup"><span data-stu-id="42145-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="42145-108">p: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="42145-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="42145-109">$P $-일반의 지 수 $p입니다.</span><span class="sxs-lookup"><span data-stu-id="42145-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="42145-110">array: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="42145-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="42145-111">Output: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="42145-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="42145-112">$P $-일반 $ x _p $로 정규화 된 $ $x 배열 \| \| 입니다.</span><span class="sxs-lookup"><span data-stu-id="42145-112">The array $x$ normalized by the $p$-norm $\|x\|_p$.</span></span>

## <a name="see-also"></a><span data-ttu-id="42145-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="42145-113">See Also</span></span>

- [<span data-ttu-id="42145-114">Microsoft 양자.</span><span class="sxs-lookup"><span data-stu-id="42145-114">Microsoft.Quantum.Math.PNorm</span></span>](xref:Microsoft.Quantum.Math.PNorm)