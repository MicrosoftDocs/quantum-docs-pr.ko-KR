---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger
title: MultiplyAndAddPhaseByModularInteger 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddPhaseByModularInteger
qsharp.summary: The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.
ms.openlocfilehash: be7df50f040697329c2fe8bbc319c8cebb8b2687
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719804"
---
# <a name="multiplyandaddphasebymodularinteger-operation"></a><span data-ttu-id="c5476-102">MultiplyAndAddPhaseByModularInteger 작업</span><span class="sxs-lookup"><span data-stu-id="c5476-102">MultiplyAndAddPhaseByModularInteger operation</span></span>

<span data-ttu-id="c5476-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="c5476-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="c5476-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c5476-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c5476-105">MultiplyAndAddByModularInteger와 동일 하지만 summand가 QFT로 정수를 인코딩하는 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5476-105">The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.</span></span>

```qsharp
operation MultiplyAndAddPhaseByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, phaseSummand : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="c5476-106">입력</span><span class="sxs-lookup"><span data-stu-id="c5476-106">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="c5476-107">constMultiplier: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c5476-107">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c5476-108">각 기본 상태 레이블에 추가할 정수 $a $입니다.</span><span class="sxs-lookup"><span data-stu-id="c5476-108">An integer $a$ to be added to each basis state label.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="c5476-109">모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c5476-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c5476-110">와 관련 하 여 더하기 및 곱하기를 수행 하는 모듈러스 $N $입니다.</span><span class="sxs-lookup"><span data-stu-id="c5476-110">The modulus $N$ which addition and multiplication is taken with respect to.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="c5476-111">승수: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c5476-111">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c5476-112">값이의 각 기본 상태 레이블에 추가 될 부호 없는 정수를 나타내는 퀀텀 레지스터입니다 `summand` .</span><span class="sxs-lookup"><span data-stu-id="c5476-112">A quantum register representing an unsigned integer whose value is to be added to each basis state label of `summand`.</span></span>


### <a name="phasesummand--phaselittleendian"></a><span data-ttu-id="c5476-113">phaseSummand: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c5476-113">phaseSummand : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="c5476-114">이 작업의 대상으로 사용할 부호 없는 정수를 나타내는 퀀텀 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="c5476-114">A quantum register representing an unsigned integer to use as the target for this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c5476-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c5476-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c5476-116">설명</span><span class="sxs-lookup"><span data-stu-id="c5476-116">Remarks</span></span>

<span data-ttu-id="c5476-117">에 `phaseSummand` 가장 높은 비트가 0으로 설정 된 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5476-117">Assumes that `phaseSummand` has the highest bit set to 0.</span></span>
<span data-ttu-id="c5476-118">또한은 값 `phaseSummand` 이 $ $N 미만 이라고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5476-118">Also assumes that the value of `phaseSummand` is less than $N$.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5476-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c5476-119">See Also</span></span>

- [<span data-ttu-id="c5476-120">MultiplyAndAddByModularInteger.</span><span class="sxs-lookup"><span data-stu-id="c5476-120">Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger)