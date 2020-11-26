---
uid: Microsoft.Quantum.Arithmetic.IncrementByInteger
title: IncrementByInteger 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: fa5e75e91206aa5f33233c8a54d6e9e7ac2950e3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222969"
---
# <a name="incrementbyinteger-operation"></a><span data-ttu-id="09341-102">IncrementByInteger 작업</span><span class="sxs-lookup"><span data-stu-id="09341-102">IncrementByInteger operation</span></span>

<span data-ttu-id="09341-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="09341-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="09341-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="09341-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="09341-105">단계 회전을 사용 하 여, 부호 없는 퀀텀 레지스터를 고전 정수로 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="09341-105">Increments an unsigned quantum register by a classical integer, using phase rotations.</span></span>

```qsharp
operation IncrementByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="09341-106">Description</span><span class="sxs-lookup"><span data-stu-id="09341-106">Description</span></span>

<span data-ttu-id="09341-107">가 `target` $x 부호 없는 정수를 작은 endian 인코딩으로 인코딩하고 $a $와 같은 경우를 가정 `increment` 합니다.</span><span class="sxs-lookup"><span data-stu-id="09341-107">Suppose that `target` encodes an unsigned integer $x$ in a little-endian encoding and that `increment` is equal to $a$.</span></span>
<span data-ttu-id="09341-108">그런 다음이 작업을 수행 하면 단일 $ \ket{x} \maps\ket{x + a} $이 구현 됩니다. 여기서 더하기는 모듈로 $2 ^ n $, 여기서 $n = \texttt{Length (target!)}입니다. $.</span><span class="sxs-lookup"><span data-stu-id="09341-108">Then, this operation implements the unitary $\ket{x} \mapsto \ket{x + a}$, where the addition is performed modulo $2^n$, where $n = \texttt{Length(target!)}$.</span></span>

## <a name="input"></a><span data-ttu-id="09341-109">입력</span><span class="sxs-lookup"><span data-stu-id="09341-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="09341-110">증가값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="09341-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="09341-111">가 증가 하는 정수 `target` 입니다.</span><span class="sxs-lookup"><span data-stu-id="09341-111">The integer by which the `target` is incremented by.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="09341-112">대상: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="09341-112">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="09341-113">퀀텀 레지스터는 작은 endian 인코딩을 사용 하 여 부호 없는 정수를 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="09341-113">A quantum register encoding an unsigned integer using little-endian encoding.</span></span>



## <a name="output--unit"></a><span data-ttu-id="09341-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="09341-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

