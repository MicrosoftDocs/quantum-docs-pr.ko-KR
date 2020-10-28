---
uid: Microsoft.Quantum.Arithmetic.CompareGTSI
title: CompareGTSI 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTSI
qsharp.summary: 'Wrapper for signed integer comparison: `result = xs > ys`.'
ms.openlocfilehash: 735ae21168d8efb3e626a8f1ea36e97f5cdf8760
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721280"
---
# <a name="comparegtsi-operation"></a><span data-ttu-id="c2d3a-102">CompareGTSI 작업</span><span class="sxs-lookup"><span data-stu-id="c2d3a-102">CompareGTSI operation</span></span>

<span data-ttu-id="c2d3a-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="c2d3a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="c2d3a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c2d3a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c2d3a-105">부호 있는 정수 비교를 위한 `result = xs > ys` 래퍼입니다.</span><span class="sxs-lookup"><span data-stu-id="c2d3a-105">Wrapper for signed integer comparison: `result = xs > ys`.</span></span>

```qsharp
operation CompareGTSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="c2d3a-106">입력</span><span class="sxs-lookup"><span data-stu-id="c2d3a-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="c2d3a-107">xs: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c2d3a-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="c2d3a-108">첫 번째 $n $ 비트 숫자</span><span class="sxs-lookup"><span data-stu-id="c2d3a-108">First $n$-bit number</span></span>


### <a name="ys--signedlittleendian"></a><span data-ttu-id="c2d3a-109">작업: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c2d3a-109">ys : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="c2d3a-110">두 번째 $n $ 비트 숫자</span><span class="sxs-lookup"><span data-stu-id="c2d3a-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="c2d3a-111">결과: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c2d3a-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c2d3a-112">$Xs > 되 면 대칭 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2d3a-112">Will be flipped if $xs > ys$</span></span>



## <a name="output--unit"></a><span data-ttu-id="c2d3a-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c2d3a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

