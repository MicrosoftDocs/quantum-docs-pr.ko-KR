---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyObliviousAmplitudeAmplification
title: ApplyObliviousAmplitudeAmplification 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyObliviousAmplitudeAmplification
qsharp.summary: Oblivious amplitude amplification by specifying partial reflections.
ms.openlocfilehash: a1bda344b1097c7ab3240bc6d9cd0d8df80b9662
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721880"
---
# <a name="applyobliviousamplitudeamplification-operation"></a><span data-ttu-id="9ccba-102">ApplyObliviousAmplitudeAmplification 작업</span><span class="sxs-lookup"><span data-stu-id="9ccba-102">ApplyObliviousAmplitudeAmplification operation</span></span>

<span data-ttu-id="9ccba-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="9ccba-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="9ccba-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9ccba-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9ccba-105">부분 반사를 지정 하 여 명확한 진폭 증폭</span><span class="sxs-lookup"><span data-stu-id="9ccba-105">Oblivious amplitude amplification by specifying partial reflections.</span></span>

```qsharp
operation ApplyObliviousAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, auxiliaryRegister : Qubit[], systemRegister : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="9ccba-106">입력</span><span class="sxs-lookup"><span data-stu-id="9ccba-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="9ccba-107">단계: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="9ccba-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="9ccba-108">부분 반사의 단계</span><span class="sxs-lookup"><span data-stu-id="9ccba-108">Phases of partial reflections</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="9ccba-109">startStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="9ccba-109">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="9ccba-110">보조 레지스터의 시작 상태에 대 한 리플렉션 연산자</span><span class="sxs-lookup"><span data-stu-id="9ccba-110">Reflection operator about start state of auxiliary register</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="9ccba-111">targetStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="9ccba-111">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="9ccba-112">보조 레지스터의 대상 상태에 대 한 리플렉션 연산자</span><span class="sxs-lookup"><span data-stu-id="9ccba-112">Reflection operator about target state of auxiliary register</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="9ccba-113">signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="9ccba-113">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="9ccba-114">`ObliviousOracle`보조 및 시스템 레지스터에 대해 공동으로 작동 하는 형식의 단일 oracle $O $입니다.</span><span class="sxs-lookup"><span data-stu-id="9ccba-114">Unitary oracle $O$ of type `ObliviousOracle` that acts jointly on the auxiliary and system registers.</span></span>


### <a name="auxiliaryregister--qubit"></a><span data-ttu-id="9ccba-115">auxiliaryRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9ccba-115">auxiliaryRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9ccba-116">보조 레지스터</span><span class="sxs-lookup"><span data-stu-id="9ccba-116">Auxiliary register</span></span>


### <a name="systemregister--qubit"></a><span data-ttu-id="9ccba-117">systemRegister: [Ontbit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9ccba-117">systemRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9ccba-118">시스템 등록</span><span class="sxs-lookup"><span data-stu-id="9ccba-118">System register</span></span>



## <a name="output--unit"></a><span data-ttu-id="9ccba-119">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9ccba-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9ccba-120">설명</span><span class="sxs-lookup"><span data-stu-id="9ccba-120">Remarks</span></span>

<span data-ttu-id="9ccba-121">특정 보조 시작 상태 $ \ket{\text{start}} \_ a $, 특정 보조 대상 상태 $ \ket{\text{target}} \_ a $ 및 모든 시스템 상태 $ \ket{\psi} s $가 지정 된 \_ 경우 일부 단일 $U $에 대해 \begin{align} O\ket {\ text {start}} \_ a\ket {\ psi} \_ s = \lambda\ket{\text{target}} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{\text{target} ^ \perp} a\cdots \end{align}이 있다고 가정 \_ 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ccba-121">Given a particular auxiliary start state $\ket{\text{start}}\_a$, a particular auxiliary target state $\ket{\text{target}}\_a$, and any system state $\ket{\psi}\_s$, suppose that \begin{align} O\ket{\text{start}}\_a\ket{\psi}\_s= \lambda\ket{\text{target}}\_a U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{\text{target}^\perp}\_a\cdots \end{align} for some unitary $U$.</span></span>
<span data-ttu-id="9ccba-122">및 해당 adjoint의 응용 프로그램에 의해 인터리브 된 보조 레지스터의 시작 및 대상 상태에 대 한 반사 시퀀스를 통해 `signalOracle` U 적용의 성공 확률이 변경 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ccba-122">By a sequence of reflections about the start and target states on the auxiliary register interleaved by applications of `signalOracle` and its adjoint, the success probability of applying U may be altered.</span></span>

<span data-ttu-id="9ccba-123">대부분의 경우 `auxiliaryRegister` 는 $ \ket{\text{start}} a $ 상태에서 초기화 됩니다 \_ .</span><span class="sxs-lookup"><span data-stu-id="9ccba-123">In most cases, `auxiliaryRegister` is initialized in the state $\ket{\text{start}}\_a$.</span></span>

## <a name="references"></a><span data-ttu-id="9ccba-124">참조</span><span class="sxs-lookup"><span data-stu-id="9ccba-124">References</span></span>

<span data-ttu-id="9ccba-125">참조</span><span class="sxs-lookup"><span data-stu-id="9ccba-125">See</span></span>

- <span data-ttu-id="9ccba-126">표준 버전에 대 한 [ *D.W. Berry, A.M. Childs, Cleve, Kothari, R.D. Somma*](https://arxiv.org/abs/1312.1414) 입니다.</span><span class="sxs-lookup"><span data-stu-id="9ccba-126">[ *D.W. Berry, A.M. Childs, R. Cleve, R. Kothari, R.D. Somma* ](https://arxiv.org/abs/1312.1414) for the standard version.</span></span>
  <span data-ttu-id="9ccba-127">참조</span><span class="sxs-lookup"><span data-stu-id="9ccba-127">See</span></span>
- <span data-ttu-id="9ccba-128">[ *G.H. Low, I.L. Chuang*](https://arxiv.org/abs/1610.06546) 를 통해 부분 반사를 일반화 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ccba-128">[ *G.H. Low, I.L. Chuang* ](https://arxiv.org/abs/1610.06546) for a generalization to partial reflections.</span></span>