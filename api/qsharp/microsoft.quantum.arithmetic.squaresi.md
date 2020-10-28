---
uid: Microsoft.Quantum.Arithmetic.SquareSI
title: SquareSI 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareSI
qsharp.summary: Square signed integer `xs` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: c8c4e3cca001aa6d7ce1b9df106ce77f74524301
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719533"
---
# <a name="squaresi-operation"></a><span data-ttu-id="835df-102">SquareSI 작업</span><span class="sxs-lookup"><span data-stu-id="835df-102">SquareSI operation</span></span>

<span data-ttu-id="835df-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="835df-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="835df-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="835df-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="835df-105">부호 있는 사각형 `xs` 의 정수 이며 처음에 0 이어야 하는에 결과를 저장 합니다 `result` .</span><span class="sxs-lookup"><span data-stu-id="835df-105">Square signed integer `xs` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation SquareSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="835df-106">입력</span><span class="sxs-lookup"><span data-stu-id="835df-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="835df-107">xs: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="835df-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="835df-108">n 비트 정수-제곱 (SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="835df-108">n-bit integer to square (SignedLittleEndian)</span></span>


### <a name="result--signedlittleendian"></a><span data-ttu-id="835df-109">결과: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="835df-109">result : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="835df-110">2n-bit result (SignedLittleEndian)는 $ \ket $ 상태 여야 합니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="835df-110">2n-bit result (SignedLittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="835df-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="835df-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="835df-112">설명</span><span class="sxs-lookup"><span data-stu-id="835df-112">Remarks</span></span>

<span data-ttu-id="835df-113">구현은 IntegerSquare에 의존 합니다.</span><span class="sxs-lookup"><span data-stu-id="835df-113">The implementation relies on IntegerSquare.</span></span>