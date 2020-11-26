---
uid: Microsoft.Quantum.Arithmetic.SquareSI
title: SquareSI 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareSI
qsharp.summary: Square signed integer `xs` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 7fe4d27b974a06b019a2b15710fbc51b598027b4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221830"
---
# <a name="squaresi-operation"></a><span data-ttu-id="8f37d-102">SquareSI 작업</span><span class="sxs-lookup"><span data-stu-id="8f37d-102">SquareSI operation</span></span>

<span data-ttu-id="8f37d-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="8f37d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="8f37d-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="8f37d-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="8f37d-105">부호 있는 사각형 `xs` 의 정수 이며 처음에 0 이어야 하는에 결과를 저장 합니다 `result` .</span><span class="sxs-lookup"><span data-stu-id="8f37d-105">Square signed integer `xs` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation SquareSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="8f37d-106">입력</span><span class="sxs-lookup"><span data-stu-id="8f37d-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="8f37d-107">xs: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8f37d-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="8f37d-108">n 비트 정수-제곱 (SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8f37d-108">n-bit integer to square (SignedLittleEndian)</span></span>


### <a name="result--signedlittleendian"></a><span data-ttu-id="8f37d-109">결과: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8f37d-109">result : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="8f37d-110">2n-bit result (SignedLittleEndian)는 $ \ket $ 상태 여야 합니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="8f37d-110">2n-bit result (SignedLittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8f37d-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8f37d-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="8f37d-112">설명</span><span class="sxs-lookup"><span data-stu-id="8f37d-112">Remarks</span></span>

<span data-ttu-id="8f37d-113">구현은 IntegerSquare에 의존 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f37d-113">The implementation relies on IntegerSquare.</span></span>