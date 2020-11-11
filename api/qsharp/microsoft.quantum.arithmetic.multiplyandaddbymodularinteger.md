---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger
title: MultiplyAndAddByModularInteger 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddByModularInteger
qsharp.summary: Performs a modular multiply-and-add by integer constants on a qubit register.
ms.openlocfilehash: 3f85f6aaea1d6f8095709c6f387322df7a5e047c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719809"
---
# <a name="multiplyandaddbymodularinteger-operation"></a><span data-ttu-id="74d03-102">MultiplyAndAddByModularInteger 작업</span><span class="sxs-lookup"><span data-stu-id="74d03-102">MultiplyAndAddByModularInteger operation</span></span>

<span data-ttu-id="74d03-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="74d03-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="74d03-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="74d03-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="74d03-105">은 (는) 정수 계열 레지스터에서 모듈식 곱하기 및 추가 정수 상수를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="74d03-105">Performs a modular multiply-and-add by integer constants on a qubit register.</span></span>

```qsharp
operation MultiplyAndAddByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, summand : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="74d03-106">Description</span><span class="sxs-lookup"><span data-stu-id="74d03-106">Description</span></span>

<span data-ttu-id="74d03-107">지정 된 모듈러스 $N $, 상수 승수 $a $ 및 \ket{$y $에 대해 $ $ \begin{align} \ket{x} \ket{b} \maps\ket{x} \operatorname{mod} (b + a \mapsto x) \end{align} N} summand $ $ 맵을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="74d03-107">Implements the map $$ \begin{align} \ket{x} \ket{b} \mapsto \ket{x} \ket{(b + a \cdot x) \operatorname{mod} N} \end{align} $$ for a given modulus $N$, constant multiplier $a$, and summand $y$.</span></span>

## <a name="input"></a><span data-ttu-id="74d03-108">입력</span><span class="sxs-lookup"><span data-stu-id="74d03-108">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="74d03-109">constMultiplier: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="74d03-109">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="74d03-110">각 기본 상태 레이블에 추가할 정수 $a $입니다.</span><span class="sxs-lookup"><span data-stu-id="74d03-110">An integer $a$ to be added to each basis state label.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="74d03-111">모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="74d03-111">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="74d03-112">와 관련 하 여 더하기 및 곱하기를 수행 하는 모듈러스 $N $입니다.</span><span class="sxs-lookup"><span data-stu-id="74d03-112">The modulus $N$ which addition and multiplication is taken with respect to.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="74d03-113">승수: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="74d03-113">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="74d03-114">값이의 각 기본 상태 레이블에 추가 될 부호 없는 정수를 나타내는 퀀텀 레지스터입니다 `summand` .</span><span class="sxs-lookup"><span data-stu-id="74d03-114">A quantum register representing an unsigned integer whose value is to be added to each basis state label of `summand`.</span></span>


### <a name="summand--littleendian"></a><span data-ttu-id="74d03-115">summand: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="74d03-115">summand : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="74d03-116">이 작업의 대상으로 사용할 부호 없는 정수를 나타내는 퀀텀 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="74d03-116">A quantum register representing an unsigned integer to use as the target for this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="74d03-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="74d03-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="74d03-118">설명</span><span class="sxs-lookup"><span data-stu-id="74d03-118">Remarks</span></span>

- <span data-ttu-id="74d03-119">회로 다이어그램 및 설명의 경우 그림 6 [(arXiv: 5ant-ph/0205095v3 페이지](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7) )을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="74d03-119">For the circuit diagram and explanation see Figure 6 on [Page 7 of arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7)</span></span>
- <span data-ttu-id="74d03-120">이 작업은 [Arxiv: CMULT/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf) 의 (a) MOD (N)에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="74d03-120">This operation corresponds to CMULT(a)MOD(N) in [arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span></span>

## <a name="see-also"></a><span data-ttu-id="74d03-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="74d03-121">See Also</span></span>

- [<span data-ttu-id="74d03-122">MultiplyAndAddPhaseByModularInteger.</span><span class="sxs-lookup"><span data-stu-id="74d03-122">Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger)