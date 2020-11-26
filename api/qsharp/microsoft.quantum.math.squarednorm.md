---
uid: Microsoft.Quantum.Math.SquaredNorm
title: SquaredNorm 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: ecbc66a8851f23187e0c0ea53ce121442323733b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227304"
---
# <a name="squarednorm-function"></a><span data-ttu-id="70978-102">SquaredNorm 함수</span><span class="sxs-lookup"><span data-stu-id="70978-102">SquaredNorm function</span></span>

<span data-ttu-id="70978-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="70978-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="70978-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="70978-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="70978-105">벡터의 2 차 제곱을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="70978-105">Returns the squared 2-norm of a vector.</span></span>

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a><span data-ttu-id="70978-106">Description</span><span class="sxs-lookup"><span data-stu-id="70978-106">Description</span></span>

<span data-ttu-id="70978-107">벡터의 2 차 제곱을 반환 합니다. 즉, 입력 $ \vec{x} $가 지정 된 경우 $ \ sum_i x_i ^ 2 $를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="70978-107">Returns the squared 2-norm of a vector; that is, given an input $\vec{x}$, returns $\sum_i x_i^2$.</span></span>

## <a name="input"></a><span data-ttu-id="70978-108">입력</span><span class="sxs-lookup"><span data-stu-id="70978-108">Input</span></span>

### <a name="array--double"></a><span data-ttu-id="70978-109">array: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="70978-109">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="70978-110">제곱 2-표준을 반환 하는 벡터입니다.</span><span class="sxs-lookup"><span data-stu-id="70978-110">The vector whose squared 2-norm is to be returned.</span></span>



## <a name="output--double"></a><span data-ttu-id="70978-111">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="70978-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="70978-112">의 2 차 제곱입니다 `array` .</span><span class="sxs-lookup"><span data-stu-id="70978-112">The squared 2-norm of `array`.</span></span>