---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: IncrementByModularInteger 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 8a02d22facce8f58180752b6d063ac55d75ca537
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222952"
---
# <a name="incrementbymodularinteger-operation"></a><span data-ttu-id="c936e-102">IncrementByModularInteger 작업</span><span class="sxs-lookup"><span data-stu-id="c936e-102">IncrementByModularInteger operation</span></span>

<span data-ttu-id="c936e-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="c936e-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="c936e-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c936e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c936e-105">정수 상수를 기준으로 하는 이상 비트 레지스터의 모듈식 증분을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c936e-105">Performs a modular increment of a qubit register by an integer constant.</span></span>

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="c936e-106">Description</span><span class="sxs-lookup"><span data-stu-id="c936e-106">Description</span></span>

<span data-ttu-id="c936e-107">`increment`$A $, `modulus` $N $ 및 $y $로 인코딩된 정수를 사용 하 여 나타냅니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="c936e-107">Let us denote `increment` by $a$, `modulus` by $N$ and integer encoded in `target` by $y$.</span></span>
<span data-ttu-id="c936e-108">그런 다음이 작업은 다음 변환을 수행 합니다. \begin{align} \ket{y} \maps\ket{(y + a) \operatorname{mod} N} \end{align} 정수는 작은 endian 형식으로 인코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="c936e-108">Then the operation performs the following transformation: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} Integers are encoded in little-endian format.</span></span>

## <a name="input"></a><span data-ttu-id="c936e-109">입력</span><span class="sxs-lookup"><span data-stu-id="c936e-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="c936e-110">증가값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c936e-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c936e-111">$Y $에 더할 정수 증가값 $a $입니다.</span><span class="sxs-lookup"><span data-stu-id="c936e-111">Integer increment $a$ to be added to $y$.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="c936e-112">모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c936e-112">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c936e-113">Mods $y + a $의 정수 $N $입니다.</span><span class="sxs-lookup"><span data-stu-id="c936e-113">Integer $N$ that mods $y + a$.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="c936e-114">대상: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c936e-114">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c936e-115">`LittleEndian` `increment` $A $가에 추가 되는 형식의 정수 $y $입니다.</span><span class="sxs-lookup"><span data-stu-id="c936e-115">Integer $y$ in `LittleEndian` format that `increment` $a$ is added to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c936e-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c936e-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c936e-117">설명</span><span class="sxs-lookup"><span data-stu-id="c936e-117">Remarks</span></span>

<span data-ttu-id="c936e-118">Target의 초기 값이 $ $N 보다 작고 증분 $a $가 $N $ 보다 작은 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c936e-118">Assumes that the initial value of target is less than $N$ and that the increment $a$ is less than $N$.</span></span>
<span data-ttu-id="c936e-119">에서는 <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> 동일한 작업을 기준으로 구현 합니다 `PhaseLittleEndian` .</span><span class="sxs-lookup"><span data-stu-id="c936e-119">Note that <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> implements the same operation in the `PhaseLittleEndian` basis.</span></span>

## <a name="see-also"></a><span data-ttu-id="c936e-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c936e-120">See Also</span></span>

- [<span data-ttu-id="c936e-121">IncrementPhaseByModularInteger.</span><span class="sxs-lookup"><span data-stu-id="c936e-121">Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger)