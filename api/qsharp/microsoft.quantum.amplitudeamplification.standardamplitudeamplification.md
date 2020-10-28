---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardAmplitudeAmplification
title: StandardAmplitudeAmplification 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardAmplitudeAmplification
qsharp.summary: Standard Amplitude Amplification algorithm
ms.openlocfilehash: 18228d45c4df280b004c595a7b0f1e2a607b8b2c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721747"
---
# <a name="standardamplitudeamplification-function"></a><span data-ttu-id="7fbeb-102">StandardAmplitudeAmplification 함수</span><span class="sxs-lookup"><span data-stu-id="7fbeb-102">StandardAmplitudeAmplification function</span></span>

<span data-ttu-id="7fbeb-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="7fbeb-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="7fbeb-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7fbeb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7fbeb-105">표준 진폭 증폭 알고리즘</span><span class="sxs-lookup"><span data-stu-id="7fbeb-105">Standard Amplitude Amplification algorithm</span></span>

```qsharp
function StandardAmplitudeAmplification (nIterations : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="7fbeb-106">입력</span><span class="sxs-lookup"><span data-stu-id="7fbeb-106">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="7fbeb-107">nIterations: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7fbeb-107">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7fbeb-108">진폭 증폭의 $ $n 반복 횟수</span><span class="sxs-lookup"><span data-stu-id="7fbeb-108">Number of iterations $n$ of amplitude amplification</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="7fbeb-109">stateOracle: [Stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="7fbeb-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="7fbeb-110">시작 상태를 준비 하는 단일 oracle $A $</span><span class="sxs-lookup"><span data-stu-id="7fbeb-110">Unitary oracle $A$ that prepares start state</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="7fbeb-111">Idx플래그 [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7fbeb-111">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7fbeb-112">플래그에 대 한 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-112">Index to flag qubit</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="7fbeb-113">출력: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="7fbeb-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="7fbeb-114">표준 진폭 증폭 퀀텀 알고리즘을 구현 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-114">An operation that implements the standard amplitude amplification quantum algorithm</span></span>

## <a name="remarks"></a><span data-ttu-id="7fbeb-115">설명</span><span class="sxs-lookup"><span data-stu-id="7fbeb-115">Remarks</span></span>

<span data-ttu-id="7fbeb-116">이는 `AmpAmpPhasesStandard` \Begin{align} A\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ text {target}} s + \sqrt{1-| \lambda | ^ 2} \ket f\cdots로 가정 하 여 계산 된 리플렉션 단계 중에서 가져온 표준 진폭 증폭 알고리즘입니다. \_ {0} \_ 이 작업을 \end{align} 대부분의 경우 \begin{align} \operatorname{AmpAmpByOracle}\ket {0} \_ {f} \ket {0} \_ s = \lambda ((2n + 1) \lambda ^ {-1} (\lambda)) \ket {1} \_ f\ket {\ text {target}} \_ s + \cdots\ket {0} \_ f \end{align}을 준비 `flagQubit` 하 고, `auxiliaryRegister` 상태 $ \ket {0} \_ f\ket {0} \_ a $에서 초기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-116">This is the standard amplitude amplification algorithm obtained by a choice of reflection phases computed by `AmpAmpPhasesStandard` Assuming that \begin{align} A\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\text{target}}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} this operation prepares the state \begin{align} \operatorname{AmpAmpByOracle}\ket{0}\_{f}\ket{0}\_s= \sin((2n+1)\sin^{-1}(\lambda))\ket{1}\_f\ket{\text{target}}\_s + \cdots\ket{0}\_f \end{align} In most cases, `flagQubit` and `auxiliaryRegister` is initialized in the state $\ket{0}\_f\ket{0}\_a$.</span></span>

## <a name="references"></a><span data-ttu-id="7fbeb-117">참조</span><span class="sxs-lookup"><span data-stu-id="7fbeb-117">References</span></span>

- [<span data-ttu-id="7fbeb-118">*G. Brtis, Hoyer, M. Mosca, .Ttapp*</span><span class="sxs-lookup"><span data-stu-id="7fbeb-118"> *G. Brassard, P. Hoyer, M. Mosca, A. Tapp* </span></span>](https://arxiv.org/abs/quant-ph/0005055)