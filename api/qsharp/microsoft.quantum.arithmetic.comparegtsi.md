---
uid: Microsoft.Quantum.Arithmetic.CompareGTSI
title: CompareGTSI 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTSI
qsharp.summary: 'Wrapper for signed integer comparison: `result = xs > ys`.'
ms.openlocfilehash: f725bdbaa945a4f87e90fc71930c37642113c21a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846703"
---
# <a name="comparegtsi-operation"></a><span data-ttu-id="24b0a-102">CompareGTSI 작업</span><span class="sxs-lookup"><span data-stu-id="24b0a-102">CompareGTSI operation</span></span>

<span data-ttu-id="24b0a-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="24b0a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="24b0a-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="24b0a-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="24b0a-105">부호 있는 정수 비교를 위한 `result = xs > ys` 래퍼입니다.</span><span class="sxs-lookup"><span data-stu-id="24b0a-105">Wrapper for signed integer comparison: `result = xs > ys`.</span></span>

```qsharp
operation CompareGTSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="24b0a-106">입력</span><span class="sxs-lookup"><span data-stu-id="24b0a-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="24b0a-107">xs: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="24b0a-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="24b0a-108">첫 번째 $n $ 비트 숫자</span><span class="sxs-lookup"><span data-stu-id="24b0a-108">First $n$-bit number</span></span>


### <a name="ys--signedlittleendian"></a><span data-ttu-id="24b0a-109">작업: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="24b0a-109">ys : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="24b0a-110">두 번째 $n $ 비트 숫자</span><span class="sxs-lookup"><span data-stu-id="24b0a-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="24b0a-111">결과: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="24b0a-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="24b0a-112">$Xs > 되 면 대칭 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24b0a-112">Will be flipped if $xs > ys$</span></span>



## <a name="output--unit"></a><span data-ttu-id="24b0a-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="24b0a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

