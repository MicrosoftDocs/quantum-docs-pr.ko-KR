---
uid: Microsoft.Quantum.Math.SquaredNorm
title: SquaredNorm 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: 72ae8266492bef64eaec34cd70c5fe725ee1e8c9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848206"
---
# <a name="squarednorm-function"></a><span data-ttu-id="15664-102">SquaredNorm 함수</span><span class="sxs-lookup"><span data-stu-id="15664-102">SquaredNorm function</span></span>

<span data-ttu-id="15664-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="15664-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="15664-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="15664-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="15664-105">벡터의 2 차 제곱을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="15664-105">Returns the squared 2-norm of a vector.</span></span>

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a><span data-ttu-id="15664-106">설명</span><span class="sxs-lookup"><span data-stu-id="15664-106">Description</span></span>

<span data-ttu-id="15664-107">벡터의 2 차 제곱을 반환 합니다. 즉, 입력 $ \vec{x} $가 지정 된 경우 $ \ sum_i x_i ^ 2 $를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="15664-107">Returns the squared 2-norm of a vector; that is, given an input $\vec{x}$, returns $\sum_i x_i^2$.</span></span>

## <a name="input"></a><span data-ttu-id="15664-108">입력</span><span class="sxs-lookup"><span data-stu-id="15664-108">Input</span></span>

### <a name="array--double"></a><span data-ttu-id="15664-109">array: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="15664-109">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="15664-110">제곱 2-표준을 반환 하는 벡터입니다.</span><span class="sxs-lookup"><span data-stu-id="15664-110">The vector whose squared 2-norm is to be returned.</span></span>



## <a name="output--double"></a><span data-ttu-id="15664-111">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="15664-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="15664-112">의 2 차 제곱입니다 `array` .</span><span class="sxs-lookup"><span data-stu-id="15664-112">The squared 2-norm of `array`.</span></span>