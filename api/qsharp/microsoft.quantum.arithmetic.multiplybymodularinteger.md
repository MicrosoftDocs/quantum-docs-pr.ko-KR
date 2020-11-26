---
uid: Microsoft.Quantum.Arithmetic.MultiplyByModularInteger
title: MultiplyByModularInteger 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyByModularInteger
qsharp.summary: Performs modular multiplication by an integer constant on a qubit register.
ms.openlocfilehash: 080414d208a2a0c114857db8e93efb4cd74a4d8d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222578"
---
# <a name="multiplybymodularinteger-operation"></a><span data-ttu-id="64480-102">MultiplyByModularInteger 작업</span><span class="sxs-lookup"><span data-stu-id="64480-102">MultiplyByModularInteger operation</span></span>

<span data-ttu-id="64480-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="64480-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="64480-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="64480-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="64480-105">이상 비트 레지스터에서 정수 상수로 모듈식 곱하기를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="64480-105">Performs modular multiplication by an integer constant on a qubit register.</span></span>

```qsharp
operation MultiplyByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="64480-106">Description</span><span class="sxs-lookup"><span data-stu-id="64480-106">Description</span></span>

<span data-ttu-id="64480-107">`modulus`$N $ 및 $a $를 사용 하 여 나타냅니다 `constMultiplier` .</span><span class="sxs-lookup"><span data-stu-id="64480-107">Let us denote `modulus` by $N$ and `constMultiplier` by $a$.</span></span>
<span data-ttu-id="64480-108">그런 다음이 작업은 계산 단위로 정의 된 단일 작업을 구현 합니다. $ $ \begin{align} \ket{y} \maps\ket{(a \mapsto y) \operatorname{mod} N} \end{align} $ $ (모든 $y $ between $0 $N $-$1)</span><span class="sxs-lookup"><span data-stu-id="64480-108">Then this operation implements a unitary operation defined by the following map on the computational basis: $$ \begin{align} \ket{y} \mapsto \ket{(a \cdot y) \operatorname{mod} N} \end{align} $$ for all $y$ between $0$ and $N - 1$.</span></span>

## <a name="input"></a><span data-ttu-id="64480-109">입력</span><span class="sxs-lookup"><span data-stu-id="64480-109">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="64480-110">constMultiplier: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="64480-110">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="64480-111">승수를 곱할 때 기준이 되는 상수입니다.</span><span class="sxs-lookup"><span data-stu-id="64480-111">Constant by which multiplier is being multiplied.</span></span> <span data-ttu-id="64480-112">모듈러스 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64480-112">Must be co-prime to modulus.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="64480-113">모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="64480-113">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="64480-114">곱하기 연산은 모듈로 수행 됩니다 `modulus` .</span><span class="sxs-lookup"><span data-stu-id="64480-114">The multiplication operation is performed modulo `modulus`.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="64480-115">승수: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="64480-115">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="64480-116">상수로 곱할 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="64480-116">The number being multiplied by a constant.</span></span>
<span data-ttu-id="64480-117">이는 작은 endian 형식의 정수를 인코딩 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="64480-117">This is an array of qubits encoding an integer in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="64480-118">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="64480-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="64480-119">설명</span><span class="sxs-lookup"><span data-stu-id="64480-119">Remarks</span></span>

- <span data-ttu-id="64480-120">회로 다이어그램 및 설명의 경우 [8 페이지의 arXiv: daant-ph/0205095v3 페이지](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8) 에서 그림 7을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64480-120">For the circuit diagram and explanation see Figure 7 on [Page 8 of arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8)</span></span>
- <span data-ttu-id="64480-121">이 작업은 [Arxiv: ₐ/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf) 의 u에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="64480-121">This operation corresponds to Uₐ in [arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span></span>