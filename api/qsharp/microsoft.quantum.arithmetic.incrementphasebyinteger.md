---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByInteger
title: IncrementPhaseByInteger 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: 54b83b3d4460c05478543c51f8f9c0b0e7f5b1fa
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222918"
---
# <a name="incrementphasebyinteger-operation"></a><span data-ttu-id="f9e81-102">IncrementPhaseByInteger 작업</span><span class="sxs-lookup"><span data-stu-id="f9e81-102">IncrementPhaseByInteger operation</span></span>

<span data-ttu-id="f9e81-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="f9e81-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="f9e81-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f9e81-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f9e81-105">단계 회전을 사용 하 여, 부호 없는 퀀텀 레지스터를 고전 정수로 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="f9e81-105">Increments an unsigned quantum register by a classical integer, using phase rotations.</span></span>

```qsharp
operation IncrementPhaseByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="f9e81-106">설명</span><span class="sxs-lookup"><span data-stu-id="f9e81-106">Description</span></span>

<span data-ttu-id="f9e81-107">가 `target` $x 부호 없는 정수를 작은 endian 인코딩으로 인코딩하고 $a $와 같은 경우를 가정 `increment` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9e81-107">Suppose that `target` encodes an unsigned integer $x$ in a little-endian encoding and that `increment` is equal to $a$.</span></span>
<span data-ttu-id="f9e81-108">그런 다음이 작업을 수행 하면 단일 $ \ket{x} \maps\ket{x + a} $이 구현 됩니다. 여기서 더하기는 모듈로 $2 ^ n $, 여기서 $n = \texttt{Length (target!)}입니다. $.</span><span class="sxs-lookup"><span data-stu-id="f9e81-108">Then, this operation implements the unitary $\ket{x} \mapsto \ket{x + a}$, where the addition is performed modulo $2^n$, where $n = \texttt{Length(target!)}$.</span></span>

## <a name="input"></a><span data-ttu-id="f9e81-109">입력</span><span class="sxs-lookup"><span data-stu-id="f9e81-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="f9e81-110">증가값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f9e81-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f9e81-111">가 증가 하는 정수 `target` 입니다.</span><span class="sxs-lookup"><span data-stu-id="f9e81-111">The integer by which the `target` is incremented by.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="f9e81-112">대상: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f9e81-112">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="f9e81-113">퀀텀 레지스터는 이중 (QFT) 기반의 작은 endian 인코딩을 사용 하 여 부호 없는 정수를 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="f9e81-113">A quantum register encoding an unsigned integer using little-endian encoding in the dual (QFT) basis.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f9e81-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f9e81-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f9e81-115">설명</span><span class="sxs-lookup"><span data-stu-id="f9e81-115">Remarks</span></span>

<span data-ttu-id="f9e81-116">증분은 퀀텀 레지스터가 아닌 기존 상수 이므로 회로가 간소화 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9e81-116">Note that we have simplified the circuit because the increment is a classical constant, not a quantum register.</span></span>

<span data-ttu-id="f9e81-117">회로 다이어그램 및 설명은 [ arXiv: 10-ant-ph/0008033v1의 6 페이지 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) 에 있는 그림을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f9e81-117">See the figure on [ Page 6 of arXiv:quant-ph/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) for the circuit diagram and explanation.</span></span>

## <a name="references"></a><span data-ttu-id="f9e81-118">참조 항목</span><span class="sxs-lookup"><span data-stu-id="f9e81-118">References</span></span>

- [<span data-ttu-id="f9e81-119">*Thomas G. Draper*, arxiv: mant-ph/0008033</span><span class="sxs-lookup"><span data-stu-id="f9e81-119"> *Thomas G. Draper*, arXiv:quant-ph/0008033</span></span>](https://arxiv.org/pdf/quant-ph/0008033v1.pdf)

## <a name="see-also"></a><span data-ttu-id="f9e81-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f9e81-120">See Also</span></span>

- [<span data-ttu-id="f9e81-121">IncrementByInteger.</span><span class="sxs-lookup"><span data-stu-id="f9e81-121">Microsoft.Quantum.Arithmetic.IncrementByInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementByInteger)