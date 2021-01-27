---
uid: Microsoft.Quantum.Arithmetic.CompareGTI
title: CompareGTI 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTI
qsharp.summary: 'Wrapper for integer comparison: `result = x > y`.'
ms.openlocfilehash: e9c245fb7c0cf3a6b1b98eb01cd582c325917602
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843310"
---
# <a name="comparegti-operation"></a><span data-ttu-id="6625e-102">CompareGTI 작업</span><span class="sxs-lookup"><span data-stu-id="6625e-102">CompareGTI operation</span></span>

<span data-ttu-id="6625e-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="6625e-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="6625e-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="6625e-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="6625e-105">정수 비교를 위한 래퍼입니다 `result = x > y` .</span><span class="sxs-lookup"><span data-stu-id="6625e-105">Wrapper for integer comparison: `result = x > y`.</span></span>

```qsharp
operation CompareGTI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="6625e-106">입력</span><span class="sxs-lookup"><span data-stu-id="6625e-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="6625e-107">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6625e-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="6625e-108">첫 번째 $n $ 비트 숫자</span><span class="sxs-lookup"><span data-stu-id="6625e-108">First $n$-bit number</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="6625e-109">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6625e-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="6625e-110">두 번째 $n $ 비트 숫자</span><span class="sxs-lookup"><span data-stu-id="6625e-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="6625e-111">결과: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="6625e-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="6625e-112">$X > y $ 인 경우 대칭 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6625e-112">Will be flipped if $x > y$</span></span>



## <a name="output--unit"></a><span data-ttu-id="6625e-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6625e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

