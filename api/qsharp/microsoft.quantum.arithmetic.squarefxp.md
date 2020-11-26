---
uid: Microsoft.Quantum.Arithmetic.SquareFxP
title: SquareFxP 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareFxP
qsharp.summary: Squares a fixed-point number.
ms.openlocfilehash: 8d08cb51e3a7ae892b23be0adbb7cdf3ee0f4de5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221881"
---
# <a name="squarefxp-operation"></a><span data-ttu-id="1d519-102">SquareFxP 작업</span><span class="sxs-lookup"><span data-stu-id="1d519-102">SquareFxP operation</span></span>

<span data-ttu-id="1d519-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="1d519-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="1d519-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="1d519-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="1d519-105">고정 소수점 수를 제곱 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d519-105">Squares a fixed-point number.</span></span>

```qsharp
operation SquareFxP (fp : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="1d519-106">입력</span><span class="sxs-lookup"><span data-stu-id="1d519-106">Input</span></span>

### <a name="fp--fixedpoint"></a><span data-ttu-id="1d519-107">fp: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="1d519-107">fp : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="1d519-108">고정 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="1d519-108">Fixed-point number.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="1d519-109">결과: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="1d519-109">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="1d519-110">결과 고정 소수점 수는 처음에는 state $ \ket $ 여야 합니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="1d519-110">Result fixed-point number, must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1d519-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1d519-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

