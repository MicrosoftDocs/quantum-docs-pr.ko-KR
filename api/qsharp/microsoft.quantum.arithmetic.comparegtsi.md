---
uid: Microsoft.Quantum.Arithmetic.CompareGTSI
title: CompareGTSI 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTSI
qsharp.summary: 'Wrapper for signed integer comparison: `result = xs > ys`.'
ms.openlocfilehash: a0e8ef66f1e1a62d4f6a78364135376810507534
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223496"
---
# <a name="comparegtsi-operation"></a><span data-ttu-id="9a427-102">CompareGTSI 작업</span><span class="sxs-lookup"><span data-stu-id="9a427-102">CompareGTSI operation</span></span>

<span data-ttu-id="9a427-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9a427-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9a427-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="9a427-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="9a427-105">부호 있는 정수 비교를 위한 `result = xs > ys` 래퍼입니다.</span><span class="sxs-lookup"><span data-stu-id="9a427-105">Wrapper for signed integer comparison: `result = xs > ys`.</span></span>

```qsharp
operation CompareGTSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9a427-106">입력</span><span class="sxs-lookup"><span data-stu-id="9a427-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="9a427-107">xs: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9a427-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="9a427-108">첫 번째 $n $ 비트 숫자</span><span class="sxs-lookup"><span data-stu-id="9a427-108">First $n$-bit number</span></span>


### <a name="ys--signedlittleendian"></a><span data-ttu-id="9a427-109">작업: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9a427-109">ys : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="9a427-110">두 번째 $n $ 비트 숫자</span><span class="sxs-lookup"><span data-stu-id="9a427-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="9a427-111">결과: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9a427-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9a427-112">$Xs > 되 면 대칭 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a427-112">Will be flipped if $xs > ys$</span></span>



## <a name="output--unit"></a><span data-ttu-id="9a427-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9a427-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

