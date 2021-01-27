---
uid: Microsoft.Quantum.Arithmetic.DivideI
title: DivideI 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: DivideI
qsharp.summary: Divides two quantum integers.
ms.openlocfilehash: 73c4e394ca38b8089b2990f8a8b6a3ee50f644d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846676"
---
# <a name="dividei-operation"></a><span data-ttu-id="551cb-102">DivideI 작업</span><span class="sxs-lookup"><span data-stu-id="551cb-102">DivideI operation</span></span>

<span data-ttu-id="551cb-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="551cb-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="551cb-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="551cb-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="551cb-105">두 퀀텀 정수를 나눕니다.</span><span class="sxs-lookup"><span data-stu-id="551cb-105">Divides two quantum integers.</span></span>

```qsharp
operation DivideI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="551cb-106">설명</span><span class="sxs-lookup"><span data-stu-id="551cb-106">Description</span></span>

<span data-ttu-id="551cb-107">`xs` 는 나머지를 보유 `xs - floor(xs/ys) * ys` 하 고는를 `result` 보유 `floor(xs/ys)` 합니다.</span><span class="sxs-lookup"><span data-stu-id="551cb-107">`xs` will hold the remainder `xs - floor(xs/ys) * ys` and `result` will hold `floor(xs/ys)`.</span></span>

## <a name="input"></a><span data-ttu-id="551cb-108">입력</span><span class="sxs-lookup"><span data-stu-id="551cb-108">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="551cb-109">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="551cb-109">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="551cb-110">$n $ 비트 피제수는 나머지로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="551cb-110">$n$-bit dividend, will be replaced by the remainder.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="551cb-111">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="551cb-111">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="551cb-112">$n $ 비트 제 들</span><span class="sxs-lookup"><span data-stu-id="551cb-112">$n$-bit divisor</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="551cb-113">결과: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="551cb-113">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="551cb-114">$ 비트 결과 $n $ \ket $ 상태 여야 하며 {0} 정수 나누기의 결과로 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="551cb-114">$n$-bit result, must be in state $\ket{0}$ initially and will be replaced by the result of the integer division.</span></span>



## <a name="output--unit"></a><span data-ttu-id="551cb-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="551cb-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="551cb-116">설명</span><span class="sxs-lookup"><span data-stu-id="551cb-116">Remarks</span></span>

<span data-ttu-id="551cb-117">는 표준 시프트 및 빼기 방법을 사용 하 여 나누기를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="551cb-117">Uses a standard shift-and-subtract approach to implement the division.</span></span>
<span data-ttu-id="551cb-118">제어 되는 버전은 빼기로 추가 컨트롤이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="551cb-118">The controlled version is specialized such the subtraction does not require additional controls.</span></span>