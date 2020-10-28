---
uid: Microsoft.Quantum.Arithmetic.SquareI
title: SquareI 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareI
qsharp.summary: Computes the square of the integer `xs` into `result`, which must be zero initially.
ms.openlocfilehash: d7334d50f245ba358624e6e2eee94b63d9ed7569
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719540"
---
# <a name="squarei-operation"></a><span data-ttu-id="1f073-102">SquareI 작업</span><span class="sxs-lookup"><span data-stu-id="1f073-102">SquareI operation</span></span>

<span data-ttu-id="1f073-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="1f073-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="1f073-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1f073-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1f073-105">에서 정수의 제곱을 계산 하 `xs` 여 `result` 처음에 0 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f073-105">Computes the square of the integer `xs` into `result`, which must be zero initially.</span></span>

```qsharp
operation SquareI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="1f073-106">입력</span><span class="sxs-lookup"><span data-stu-id="1f073-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="1f073-107">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1f073-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="1f073-108">$n $ bit number to square (LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1f073-108">$n$-bit number to square (LittleEndian)</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="1f073-109">결과: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1f073-109">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="1f073-110">$2n $-bit result (LittleEndian)는 $ \ket $ 상태 여야 합니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="1f073-110">$2n$-bit result (LittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1f073-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1f073-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="1f073-112">설명</span><span class="sxs-lookup"><span data-stu-id="1f073-112">Remarks</span></span>

<span data-ttu-id="1f073-113">표준 시프트 및 추가 방법을 사용 하 여 사각형을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f073-113">Uses a standard shift-and-add approach to compute the square.</span></span> <span data-ttu-id="1f073-114">일반 승수를 적용 하기 전에 먼저 xs를 복사 하 고 복사 작업을 실행 취소 하는 단순 전방 솔루션과 비교 하 여 $n-$1의 비트를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f073-114">Saves $n-1$ qubits compared to the straight-forward solution which first copies out xs before applying a regular multiplier and then undoing the copy operation.</span></span>