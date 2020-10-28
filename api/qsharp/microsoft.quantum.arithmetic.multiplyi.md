---
uid: Microsoft.Quantum.Arithmetic.MultiplyI
title: MultiplyI 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyI
qsharp.summary: Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 7b44f64fdddfd95f51683c2c3b2f4d37d0cf6841
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719761"
---
# <a name="multiplyi-operation"></a><span data-ttu-id="2762e-102">MultiplyI 작업</span><span class="sxs-lookup"><span data-stu-id="2762e-102">MultiplyI operation</span></span>

<span data-ttu-id="2762e-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="2762e-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="2762e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2762e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2762e-105">정수를 `xs` 정수로 곱하고 `ys` 처음에 0 이어야 하는에 결과를 저장 합니다 `result` .</span><span class="sxs-lookup"><span data-stu-id="2762e-105">Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation MultiplyI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="2762e-106">입력</span><span class="sxs-lookup"><span data-stu-id="2762e-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="2762e-107">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="2762e-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="2762e-108">$n $-bit multiplicand (LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="2762e-108">$n$-bit multiplicand (LittleEndian)</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="2762e-109">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="2762e-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="2762e-110">$n $ 비트 승수 (LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="2762e-110">$n$-bit multiplier (LittleEndian)</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="2762e-111">결과: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="2762e-111">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="2762e-112">$2n $-bit result (LittleEndian)는 $ \ket $ 상태 여야 합니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="2762e-112">$2n$-bit result (LittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2762e-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2762e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="2762e-114">설명</span><span class="sxs-lookup"><span data-stu-id="2762e-114">Remarks</span></span>

<span data-ttu-id="2762e-115">표준 시프트 및 추가 방법을 사용 하 여 곱셈을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="2762e-115">Uses a standard shift-and-add approach to implement the multiplication.</span></span>
<span data-ttu-id="2762e-116">제어 된 버전 $x _i $을 (를) 컨트롤의 ancilla verbit 조건 화 된로 복사 하 고 ancilla verbit에서 더하기를 제어 하 여 향상 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2762e-116">The controlled version was improved by copying out $x_i$ to an ancilla qubit conditioned on the control qubits, and then controlling the addition on the ancilla qubit.</span></span>