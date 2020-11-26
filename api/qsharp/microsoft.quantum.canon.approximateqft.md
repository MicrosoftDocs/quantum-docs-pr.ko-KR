---
uid: Microsoft.Quantum.Canon.ApproximateQFT
title: ApproximateQFT 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximateQFT
qsharp.summary: Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.
ms.openlocfilehash: 97a410133e80cc5bffc810e9d6455baaee32364b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207703"
---
# <a name="approximateqft-operation"></a><span data-ttu-id="ef115-102">ApproximateQFT 작업</span><span class="sxs-lookup"><span data-stu-id="ef115-102">ApproximateQFT operation</span></span>

<span data-ttu-id="ef115-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ef115-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ef115-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ef115-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ef115-105">퀀텀 레지스터에 AQFT (대략적인 퀀텀 푸리에 변환)을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef115-105">Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.</span></span>

```qsharp
operation ApproximateQFT (a : Int, qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="ef115-106">입력</span><span class="sxs-lookup"><span data-stu-id="ef115-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="ef115-107">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ef115-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ef115-108">QFT 회로에서 발생 하는 제어 된 Z 회전이 정리 되는 수준을 결정 하는 근사값 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="ef115-108">approximation parameter which determines at which level the controlled Z-rotations that occur in the QFT circuit are pruned.</span></span>

<span data-ttu-id="ef115-109">근사값 매개 변수 a는 Z 회전의 정리 수준을 결정 합니다. 즉, ∈ {0. n}과 (와) 모든 Z 회전 2π/2k를 결정 합니다. 여기서 k>a는 QFT 회로에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef115-109">The approximation parameter a determines the pruning level of the Z-rotations, i.e., a ∈ {0..n} and all Z-rotations 2π/2ᵏ where k>a are removed from the QFT circuit.</span></span> <span data-ttu-id="ef115-110">K >= log ₂ (n) + log ₂ (1/ε) + 3을 바인딩할 수 있는 것으로 알려져 있습니다. | | QFT-AQFT | | Ε를<합니다.</span><span class="sxs-lookup"><span data-stu-id="ef115-110">It is known that for k >= log₂(n)+log₂(1/ε)+3 one can bound ||QFT-AQFT||<ε.</span></span>


### <a name="qs--bigendian"></a><span data-ttu-id="ef115-111">qs:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="ef115-111">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="ef115-112">대략적인 퀀텀 푸리에 변환이 적용 되는 n 개의 퀀텀 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="ef115-112">quantum register of n qubits to which the Approximate Quantum Fourier Transform is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ef115-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ef115-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ef115-114">설명</span><span class="sxs-lookup"><span data-stu-id="ef115-114">Remarks</span></span>

<span data-ttu-id="ef115-115">AQFT에는 2π/2k 및 Hadamard 게이트 형식의 Z-회전 게이트가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef115-115">AQFT requires Z-rotation gates of the form 2π/2ᵏ and Hadamard gates.</span></span>

<span data-ttu-id="ef115-116">입력 및 출력은 big endian 인코딩으로 인코딩된 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef115-116">The input and output are assumed to be encoded in big endian encoding.</span></span>

## <a name="references"></a><span data-ttu-id="ef115-117">참조 항목</span><span class="sxs-lookup"><span data-stu-id="ef115-117">References</span></span>

- [<span data-ttu-id="ef115-118">대 수 Eng. Commun에 대 한 자세한 *내용은* 입니다. 컴퓨터. 19 (3): 177-193 (2008)</span><span class="sxs-lookup"><span data-stu-id="ef115-118"> *M. Roetteler, Th. Beth*, Appl. Algebra Eng. Commun. Comput. 19(3): 177-193 (2008) </span></span>](http://doi.org/10.1007/s00200-008-0072-2)
- [<span data-ttu-id="ef115-119">*D. Coppersmith* arxiv:/0201067v1</span><span class="sxs-lookup"><span data-stu-id="ef115-119"> *D. Coppersmith* arXiv:quant-ph/0201067v1 </span></span>](https://arxiv.org/abs/quant-ph/0201067)