---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentL
title: ContinuedFractionConvergentL 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentL
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: a02b38fedb5b0025f04e7bba86f2f998493206b3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723826"
---
# <a name="continuedfractionconvergentl-function"></a><span data-ttu-id="e55d4-102">ContinuedFractionConvergentL 함수</span><span class="sxs-lookup"><span data-stu-id="e55d4-102">ContinuedFractionConvergentL function</span></span>

<span data-ttu-id="e55d4-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="e55d4-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="e55d4-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e55d4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e55d4-105">일치에 가장 가까운 연속 분수를 찾습니다. `fraction``denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="e55d4-105">Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>

```qsharp
function ContinuedFractionConvergentL (fraction : Microsoft.Quantum.Math.BigFraction, denominatorBound : BigInt) : Microsoft.Quantum.Math.BigFraction
```


## <a name="input"></a><span data-ttu-id="e55d4-106">입력</span><span class="sxs-lookup"><span data-stu-id="e55d4-106">Input</span></span>

### <a name="fraction--bigfraction"></a><span data-ttu-id="e55d4-107">분수:가 중 [분수](xref:Microsoft.Quantum.Math.BigFraction)</span><span class="sxs-lookup"><span data-stu-id="e55d4-107">fraction : [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)</span></span>




### <a name="denominatorbound--bigint"></a><span data-ttu-id="e55d4-108">denominatorBound: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="e55d4-108">denominatorBound : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigfraction"></a><span data-ttu-id="e55d4-109">출력:가 중 [분수](xref:Microsoft.Quantum.Math.BigFraction)</span><span class="sxs-lookup"><span data-stu-id="e55d4-109">Output : [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)</span></span>

<span data-ttu-id="e55d4-110">분모와 작거나 같은에 가장 가까운 연속 분수 `fraction``denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="e55d4-110">Continued fraction closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>