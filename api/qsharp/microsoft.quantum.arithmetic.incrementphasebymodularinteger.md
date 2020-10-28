---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger
title: IncrementPhaseByModularInteger 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 52309c056a3eae25ffdfbfa848f94bf744c71132
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721057"
---
# <a name="incrementphasebymodularinteger-operation"></a><span data-ttu-id="a7921-102">IncrementPhaseByModularInteger 작업</span><span class="sxs-lookup"><span data-stu-id="a7921-102">IncrementPhaseByModularInteger operation</span></span>

<span data-ttu-id="a7921-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a7921-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a7921-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a7921-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a7921-105">정수 상수를 기준으로 하는 이상 비트 레지스터의 모듈식 증분을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7921-105">Performs a modular increment of a qubit register by an integer constant.</span></span>

```qsharp
operation IncrementPhaseByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="a7921-106">Description</span><span class="sxs-lookup"><span data-stu-id="a7921-106">Description</span></span>

<span data-ttu-id="a7921-107">`increment`$A $, `modulus` $N $ 및 $y $로 인코딩된 정수를 사용 하 여 나타냅니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="a7921-107">Let us denote `increment` by $a$, `modulus` by $N$ and integer encoded in `target` by $y$.</span></span>
<span data-ttu-id="a7921-108">그런 다음이 작업은 다음 변환을 수행 합니다. \begin{align} \ket{y} \maps\ket{(y + a) \operatorname{mod} N} \end{align} 정수는 QFT로 거의 endian 형식으로 인코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7921-108">Then the operation performs the following transformation: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} Integers are encoded in little-endian format in QFT basis.</span></span>

## <a name="input"></a><span data-ttu-id="a7921-109">입력</span><span class="sxs-lookup"><span data-stu-id="a7921-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="a7921-110">증가값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a7921-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a7921-111">$Y $에 더할 정수 증가값 $a $입니다.</span><span class="sxs-lookup"><span data-stu-id="a7921-111">Integer increment $a$ to be added to $y$.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="a7921-112">모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a7921-112">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a7921-113">Mods $y + a $의 정수 $N $입니다.</span><span class="sxs-lookup"><span data-stu-id="a7921-113">Integer $N$ that mods $y + a$.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="a7921-114">대상: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a7921-114">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="a7921-115">$A $가에 추가 되는 단계 인코딩된 작은 endian 형식의 정수 $y $입니다 `increment` .</span><span class="sxs-lookup"><span data-stu-id="a7921-115">Integer $y$ in phase-encoded little-endian format that `increment` $a$ is added to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a7921-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a7921-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a7921-117">설명</span><span class="sxs-lookup"><span data-stu-id="a7921-117">Remarks</span></span>

<span data-ttu-id="a7921-118">에 `target` 가장 높은 비트가 0으로 설정 된 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7921-118">Assumes that `target` has the highest bit set to 0.</span></span>
<span data-ttu-id="a7921-119">또한은 대상의 값이 $ $N 미만 이라고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7921-119">Also assumes that the value of target is less than $N$.</span></span>

<span data-ttu-id="a7921-120">회로 다이어그램 및 설명은 [arXiv: vant-ph/0205095v3의 5 페이지](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=5)에서 그림 5를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a7921-120">For the circuit diagram and explanation see Figure 5 on [Page 5 of arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=5).</span></span>

## <a name="see-also"></a><span data-ttu-id="a7921-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a7921-121">See Also</span></span>

- [<span data-ttu-id="a7921-122">IncrementByModularInteger.</span><span class="sxs-lookup"><span data-stu-id="a7921-122">Microsoft.Quantum.Arithmetic.IncrementByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementByModularInteger)