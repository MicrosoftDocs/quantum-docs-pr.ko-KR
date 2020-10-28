---
uid: Microsoft.Quantum.Math.SquaredNorm
title: SquaredNorm 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: 4165a761753f336cb7b94ad36b11ac324ad4e5c6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725023"
---
# <a name="squarednorm-function"></a><span data-ttu-id="9f99d-102">SquaredNorm 함수</span><span class="sxs-lookup"><span data-stu-id="9f99d-102">SquaredNorm function</span></span>

<span data-ttu-id="9f99d-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="9f99d-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="9f99d-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9f99d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9f99d-105">벡터의 2 차 제곱을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f99d-105">Returns the squared 2-norm of a vector.</span></span>

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a><span data-ttu-id="9f99d-106">Description</span><span class="sxs-lookup"><span data-stu-id="9f99d-106">Description</span></span>

<span data-ttu-id="9f99d-107">벡터의 2 차 제곱을 반환 합니다. 즉, 입력 $ \vec{x} $가 지정 된 경우 $ \ sum_i x_i ^ 2 $를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f99d-107">Returns the squared 2-norm of a vector; that is, given an input $\vec{x}$, returns $\sum_i x_i^2$.</span></span>

## <a name="input"></a><span data-ttu-id="9f99d-108">입력</span><span class="sxs-lookup"><span data-stu-id="9f99d-108">Input</span></span>

### <a name="array--double"></a><span data-ttu-id="9f99d-109">array: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="9f99d-109">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="9f99d-110">제곱 2-표준을 반환 하는 벡터입니다.</span><span class="sxs-lookup"><span data-stu-id="9f99d-110">The vector whose squared 2-norm is to be returned.</span></span>



## <a name="output--double"></a><span data-ttu-id="9f99d-111">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9f99d-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9f99d-112">의 2 차 제곱입니다 `array` .</span><span class="sxs-lookup"><span data-stu-id="9f99d-112">The squared 2-norm of `array`.</span></span>