---
uid: Microsoft.Quantum.Arithmetic.PrepareFxP
title: PrepareFxP 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PrepareFxP
qsharp.summary: Initialize a quantum fixed-point number to a classical constant.
ms.openlocfilehash: 31ed1a170a47c77c21aa8b5c291860e422af2e3d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845807"
---
# <a name="preparefxp-operation"></a><span data-ttu-id="0d97e-102">PrepareFxP 작업</span><span class="sxs-lookup"><span data-stu-id="0d97e-102">PrepareFxP operation</span></span>

<span data-ttu-id="0d97e-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0d97e-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0d97e-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="0d97e-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="0d97e-105">퀀텀 고정 소수점 수를 기존 상수로 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d97e-105">Initialize a quantum fixed-point number to a classical constant.</span></span>

```qsharp
operation PrepareFxP (constant : Double, fp : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="0d97e-106">입력</span><span class="sxs-lookup"><span data-stu-id="0d97e-106">Input</span></span>

### <a name="constant--double"></a><span data-ttu-id="0d97e-107">상수: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0d97e-107">constant : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0d97e-108">퀀텀 고정 소수점 수를 초기화할 상수입니다.</span><span class="sxs-lookup"><span data-stu-id="0d97e-108">Constant to which to initialize the quantum fixed-point number.</span></span>


### <a name="fp--fixedpoint"></a><span data-ttu-id="0d97e-109">fp: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="0d97e-109">fp : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="0d97e-110">초기화할 고정 소수점 숫자 (FixedPoint 형식)입니다.</span><span class="sxs-lookup"><span data-stu-id="0d97e-110">Fixed-point number (of type FixedPoint) to initialize.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0d97e-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0d97e-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

