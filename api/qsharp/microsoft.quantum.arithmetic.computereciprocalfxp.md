---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalFxP
title: ComputeReciprocalFxP 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalFxP
qsharp.summary: Computes $1/x$ for a fixed-point number $x$.
ms.openlocfilehash: e8f31d82fc69a3d7f4b571c4a679255dffc28b7f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721249"
---
# <a name="computereciprocalfxp-operation"></a><span data-ttu-id="2d210-102">ComputeReciprocalFxP 작업</span><span class="sxs-lookup"><span data-stu-id="2d210-102">ComputeReciprocalFxP operation</span></span>

<span data-ttu-id="2d210-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="2d210-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="2d210-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2d210-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2d210-105">고정 소수점 숫자 $x $에 대해 $1/x $를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d210-105">Computes $1/x$ for a fixed-point number $x$.</span></span>

```qsharp
operation ComputeReciprocalFxP (x : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="2d210-106">입력</span><span class="sxs-lookup"><span data-stu-id="2d210-106">Input</span></span>

### <a name="x--fixedpoint"></a><span data-ttu-id="2d210-107">x: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="2d210-107">x : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="2d210-108">반전 시킬 고정 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="2d210-108">Fixed-point number to be inverted.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="2d210-109">결과: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="2d210-109">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="2d210-110">결과를 보관할 고정 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="2d210-110">Fixed-point number that will hold the result.</span></span> <span data-ttu-id="2d210-111">$ \Ket{0.0} $로 초기화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d210-111">Must be initialized to $\ket{0.0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2d210-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2d210-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

