---
uid: Microsoft.Quantum.Arithmetic.DivideI
title: DivideI 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: DivideI
qsharp.summary: Divides two quantum integers.
ms.openlocfilehash: 0cc16dddc27a000dbc30de6ae27976a01fd9f4ed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721220"
---
# <a name="dividei-operation"></a><span data-ttu-id="39917-102">DivideI 작업</span><span class="sxs-lookup"><span data-stu-id="39917-102">DivideI operation</span></span>

<span data-ttu-id="39917-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="39917-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="39917-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="39917-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="39917-105">두 퀀텀 정수를 나눕니다.</span><span class="sxs-lookup"><span data-stu-id="39917-105">Divides two quantum integers.</span></span>

```qsharp
operation DivideI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="39917-106">Description</span><span class="sxs-lookup"><span data-stu-id="39917-106">Description</span></span>

<span data-ttu-id="39917-107">`xs` 는 나머지를 보유 `xs - floor(xs/ys) * ys` 하 고는를 `result` 보유 `floor(xs/ys)` 합니다.</span><span class="sxs-lookup"><span data-stu-id="39917-107">`xs` will hold the remainder `xs - floor(xs/ys) * ys` and `result` will hold `floor(xs/ys)`.</span></span>

## <a name="input"></a><span data-ttu-id="39917-108">입력</span><span class="sxs-lookup"><span data-stu-id="39917-108">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="39917-109">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="39917-109">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="39917-110">$n $ 비트 피제수는 나머지로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="39917-110">$n$-bit dividend, will be replaced by the remainder.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="39917-111">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="39917-111">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="39917-112">$n $ 비트 제 들</span><span class="sxs-lookup"><span data-stu-id="39917-112">$n$-bit divisor</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="39917-113">결과: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="39917-113">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="39917-114">$ 비트 결과 $n $ \ket $ 상태 여야 하며 {0} 정수 나누기의 결과로 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39917-114">$n$-bit result, must be in state $\ket{0}$ initially and will be replaced by the result of the integer division.</span></span>



## <a name="output--unit"></a><span data-ttu-id="39917-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="39917-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="39917-116">설명</span><span class="sxs-lookup"><span data-stu-id="39917-116">Remarks</span></span>

<span data-ttu-id="39917-117">는 표준 시프트 및 빼기 방법을 사용 하 여 나누기를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="39917-117">Uses a standard shift-and-subtract approach to implement the division.</span></span>
<span data-ttu-id="39917-118">제어 되는 버전은 빼기로 추가 컨트롤이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39917-118">The controlled version is specialized such the subtraction does not require additional controls.</span></span>