---
uid: Microsoft.Quantum.Arithmetic.AddFxP
title: AddFxP 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddFxP
qsharp.summary: Adds two fixed-point numbers stored in quantum registers.
ms.openlocfilehash: 36a5d585a493f0e6f33f74b1686aaa01cca7ac0b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191043"
---
# <a name="addfxp-operation"></a><span data-ttu-id="d681b-102">AddFxP 작업</span><span class="sxs-lookup"><span data-stu-id="d681b-102">AddFxP operation</span></span>

<span data-ttu-id="d681b-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="d681b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="d681b-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="d681b-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="d681b-105">퀀텀 레지스터에 저장 된 두 개의 고정 소수점 숫자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d681b-105">Adds two fixed-point numbers stored in quantum registers.</span></span>

```qsharp
operation AddFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="d681b-106">Description</span><span class="sxs-lookup"><span data-stu-id="d681b-106">Description</span></span>

<span data-ttu-id="d681b-107">각각 $ \ket{f_1} $ 및 $ \ket{f_2} $ 상태에서 두 개의 고정 소수점 레지스터가 지정 된 경우, 작업 $ \ket{f_1} \ket{f_2} \maps\ket{f_1} \ket{f_1 + f_2} $를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d681b-107">Given two fixed-point registers respectively in states $\ket{f_1}$ and $\ket{f_2}$, performs the operation $\ket{f_1} \ket{f_2} \mapsto \ket{f_1} \ket{f_1 + f_2}$.</span></span>

## <a name="input"></a><span data-ttu-id="d681b-108">입력</span><span class="sxs-lookup"><span data-stu-id="d681b-108">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="d681b-109">fp1: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="d681b-109">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="d681b-110">첫 번째 고정 소수점 숫자</span><span class="sxs-lookup"><span data-stu-id="d681b-110">First fixed-point number</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="d681b-111">fp2: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="d681b-111">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="d681b-112">두 번째 고정 소수점 숫자는 두 입력의 합계를 포함 하도록 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d681b-112">Second fixed-point number, will be updated to contain the sum of the two inputs.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d681b-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d681b-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d681b-114">설명</span><span class="sxs-lookup"><span data-stu-id="d681b-114">Remarks</span></span>

<span data-ttu-id="d681b-115">현재 구현에서는 두 개의 고정 소수점 숫자가 최하위 비트에서 동일한 점 위치를 계산 해야 합니다. 즉, $n _i $ 및 $p _i $가 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d681b-115">The current implementation requires the two fixed-point numbers to have the same point position counting from the least-significant bit, i.e., $n_i$ and $p_i$ must be equal.</span></span>