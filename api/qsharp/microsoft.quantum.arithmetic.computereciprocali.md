---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalI
title: ComputeReciprocalI 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalI
qsharp.summary: Computes the reciprocal 1/x for an unsigned integer x using integer division. The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.
ms.openlocfilehash: c28027f7a2533885102a54a028bec37eb608f2b4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846716"
---
# <a name="computereciprocali-operation"></a><span data-ttu-id="853b3-102">ComputeReciprocalI 작업</span><span class="sxs-lookup"><span data-stu-id="853b3-102">ComputeReciprocalI operation</span></span>

<span data-ttu-id="853b3-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="853b3-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="853b3-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="853b3-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="853b3-105">정수 나누기를 사용 하 여 부호 없는 정수 x에 대해 역 1/x를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="853b3-105">Computes the reciprocal 1/x for an unsigned integer x using integer division.</span></span> <span data-ttu-id="853b3-106">정수로 해석 된 결과는가 됩니다 `floor(2^(2*n-1) / x)` .</span><span class="sxs-lookup"><span data-stu-id="853b3-106">The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.</span></span>

```qsharp
operation ComputeReciprocalI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="853b3-107">입력</span><span class="sxs-lookup"><span data-stu-id="853b3-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="853b3-108">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="853b3-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="853b3-109">n 비트 부호 없는 정수</span><span class="sxs-lookup"><span data-stu-id="853b3-109">n-bit unsigned integer</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="853b3-110">결과: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="853b3-110">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="853b3-111">2n 비트 출력은 $ \ket $에 처음에와 야 합니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="853b3-111">2n-bit output, must be in $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="853b3-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="853b3-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="853b3-113">설명</span><span class="sxs-lookup"><span data-stu-id="853b3-113">Remarks</span></span>

<span data-ttu-id="853b3-114">입력 x = 0에 대 한 출력은 모두-1입니다.</span><span class="sxs-lookup"><span data-stu-id="853b3-114">For the input x=0, the output will be all-ones.</span></span>