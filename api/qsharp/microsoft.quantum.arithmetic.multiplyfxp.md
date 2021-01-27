---
uid: Microsoft.Quantum.Arithmetic.MultiplyFxP
title: MultiplyFxP 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyFxP
qsharp.summary: Multiplies two fixed-point numbers in quantum registers.
ms.openlocfilehash: 776ccb7a9e1ba1a34b28da6e1cf3a0aafe9da76b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843045"
---
# <a name="multiplyfxp-operation"></a><span data-ttu-id="9d53e-102">MultiplyFxP 작업</span><span class="sxs-lookup"><span data-stu-id="9d53e-102">MultiplyFxP operation</span></span>

<span data-ttu-id="9d53e-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9d53e-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9d53e-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="9d53e-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="9d53e-105">퀀텀 레지스터의 두 고정 소수점 숫자를 곱합니다.</span><span class="sxs-lookup"><span data-stu-id="9d53e-105">Multiplies two fixed-point numbers in quantum registers.</span></span>

```qsharp
operation MultiplyFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9d53e-106">입력</span><span class="sxs-lookup"><span data-stu-id="9d53e-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="9d53e-107">fp1: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="9d53e-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="9d53e-108">첫 번째 고정 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="9d53e-108">First fixed-point number.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="9d53e-109">fp2: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="9d53e-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="9d53e-110">두 번째 고정 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="9d53e-110">Second fixed-point number.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="9d53e-111">결과: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="9d53e-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="9d53e-112">결과 고정 소수점 수는 처음에는 state $ \ket $ 여야 합니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="9d53e-112">Result fixed-point number, must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9d53e-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9d53e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9d53e-114">설명</span><span class="sxs-lookup"><span data-stu-id="9d53e-114">Remarks</span></span>

<span data-ttu-id="9d53e-115">현재 구현에서는 세 개의 고정 소수점 숫자가 동일한 점 위치와 동일한 수의 값을 갖도록 요구 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d53e-115">The current implementation requires the three fixed-point numbers to have the same point position and the same number of qubits.</span></span>