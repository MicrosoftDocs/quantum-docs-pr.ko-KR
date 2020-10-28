---
uid: Microsoft.Quantum.Arithmetic.IncrementByInteger
title: IncrementByInteger 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: 363d48d697e3b2dad4d4896e6b1e701864649d9b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721112"
---
# <a name="incrementbyinteger-operation"></a><span data-ttu-id="7f756-102">IncrementByInteger 작업</span><span class="sxs-lookup"><span data-stu-id="7f756-102">IncrementByInteger operation</span></span>

<span data-ttu-id="7f756-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="7f756-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="7f756-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7f756-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7f756-105">단계 회전을 사용 하 여, 부호 없는 퀀텀 레지스터를 고전 정수로 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="7f756-105">Increments an unsigned quantum register by a classical integer, using phase rotations.</span></span>

```qsharp
operation IncrementByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="7f756-106">Description</span><span class="sxs-lookup"><span data-stu-id="7f756-106">Description</span></span>

<span data-ttu-id="7f756-107">가 `target` $x 부호 없는 정수를 작은 endian 인코딩으로 인코딩하고 $a $와 같은 경우를 가정 `increment` 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f756-107">Suppose that `target` encodes an unsigned integer $x$ in a little-endian encoding and that `increment` is equal to $a$.</span></span>
<span data-ttu-id="7f756-108">그런 다음이 작업을 수행 하면 단일 $ \ket{x} \maps\ket{x + a} $이 구현 됩니다. 여기서 더하기는 모듈로 $2 ^ n $, 여기서 $n = \texttt{Length (target!)}입니다. $.</span><span class="sxs-lookup"><span data-stu-id="7f756-108">Then, this operation implements the unitary $\ket{x} \mapsto \ket{x + a}$, where the addition is performed modulo $2^n$, where $n = \texttt{Length(target!)}$.</span></span>

## <a name="input"></a><span data-ttu-id="7f756-109">입력</span><span class="sxs-lookup"><span data-stu-id="7f756-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="7f756-110">증가값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7f756-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7f756-111">가 증가 하는 정수 `target` 입니다.</span><span class="sxs-lookup"><span data-stu-id="7f756-111">The integer by which the `target` is incremented by.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="7f756-112">대상: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7f756-112">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7f756-113">퀀텀 레지스터는 작은 endian 인코딩을 사용 하 여 부호 없는 정수를 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="7f756-113">A quantum register encoding an unsigned integer using little-endian encoding.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7f756-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7f756-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

