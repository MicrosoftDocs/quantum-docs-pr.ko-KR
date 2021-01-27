---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromStatePreparation
title: AmplitudeAmplificationFromStatePreparation 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromStatePreparation
qsharp.summary: Amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: e64ad5ad4e975483f20f92c0b070dd6788ef296b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847449"
---
# <a name="amplitudeamplificationfromstatepreparation-function"></a><span data-ttu-id="82029-102">AmplitudeAmplificationFromStatePreparation 함수</span><span class="sxs-lookup"><span data-stu-id="82029-102">AmplitudeAmplificationFromStatePreparation function</span></span>

<span data-ttu-id="82029-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="82029-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="82029-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="82029-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="82029-105">부분 반사를 위해 oracles에 의해 진폭 증폭</span><span class="sxs-lookup"><span data-stu-id="82029-105">Amplitude amplification by oracles for partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="82029-106">입력</span><span class="sxs-lookup"><span data-stu-id="82029-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="82029-107">단계: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="82029-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="82029-108">부분 반사의 단계</span><span class="sxs-lookup"><span data-stu-id="82029-108">Phases of partial reflections</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="82029-109">stateOracle: [Stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="82029-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="82029-110">시작 상태를 준비 하는 단일 oracle $A $</span><span class="sxs-lookup"><span data-stu-id="82029-110">Unitary oracle $A$ that prepares start state</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="82029-111">Idx플래그 [](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="82029-111">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="82029-112">플래그에 대 한 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="82029-112">Index to flag qubit</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="82029-113">출력:가 중 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Adj + Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="82029-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="82029-114">부분 반사에 의해 구현 되는 oracles에 의해 진폭 증폭을 구현 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="82029-114">An operation that implements amplitude amplification by oracles that are implemented by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="82029-115">설명</span><span class="sxs-lookup"><span data-stu-id="82029-115">Remarks</span></span>

<span data-ttu-id="82029-116">이를 통해 보다는 시작 및 대상 상태의 형태에 보다 엄격한 조건을 적용 `AmpAmpByReflectionPhases` 합니다.</span><span class="sxs-lookup"><span data-stu-id="82029-116">This imposes stricter conditions on form of the start and target states than in `AmpAmpByReflectionPhases`.</span></span>
<span data-ttu-id="82029-117">대상 상태가 $ \ket f $로 표시 되어 있다고 가정 합니다 {1} \_ .</span><span class="sxs-lookup"><span data-stu-id="82029-117">It is assumed that the target state is marked by $\ket{1}\_f$.</span></span>
<span data-ttu-id="82029-118">{0} \_ 대부분의 경우 \begin{align} A\ket {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ text {target}} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\citn, \end{align}가 `flagQubit` `auxiliaryRegister` $ \ket {0} \_ {f} \ket s $ 상태에서 초기화 된다고 가정 {0} \_ 합니다.</span><span class="sxs-lookup"><span data-stu-id="82029-118">It is assumed that \begin{align} A\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\text{target}}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} In most cases, `flagQubit` and `auxiliaryRegister` are initialized in the state $\ket{0}\_{f}\ket{0}\_s$.</span></span>