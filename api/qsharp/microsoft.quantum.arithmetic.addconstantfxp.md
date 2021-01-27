---
uid: Microsoft.Quantum.Arithmetic.AddConstantFxP
title: AddConstantFxP 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddConstantFxP
qsharp.summary: Adds a classical constant to a quantum fixed-point number.
ms.openlocfilehash: fd985d1112298c3d2bbb0db2ff0d934098566e93
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843880"
---
# <a name="addconstantfxp-operation"></a><span data-ttu-id="82591-102">AddConstantFxP 작업</span><span class="sxs-lookup"><span data-stu-id="82591-102">AddConstantFxP operation</span></span>

<span data-ttu-id="82591-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="82591-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="82591-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="82591-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="82591-105">퀀텀 고정 소수점 숫자에 기존 상수를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="82591-105">Adds a classical constant to a quantum fixed-point number.</span></span>

```qsharp
operation AddConstantFxP (constant : Double, fp : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="82591-106">입력</span><span class="sxs-lookup"><span data-stu-id="82591-106">Input</span></span>

### <a name="constant--double"></a><span data-ttu-id="82591-107">상수: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="82591-107">constant : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="82591-108">퀀텀 고정 소수점 수에 더할 상수입니다.</span><span class="sxs-lookup"><span data-stu-id="82591-108">Constant to add to the quantum fixed-point number.</span></span>


### <a name="fp--fixedpoint"></a><span data-ttu-id="82591-109">fp: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="82591-109">fp : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="82591-110">상수가 추가 되는 고정 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="82591-110">Fixed-point number to which the constant will be added.</span></span>



## <a name="output--unit"></a><span data-ttu-id="82591-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="82591-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

