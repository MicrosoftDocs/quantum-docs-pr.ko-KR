---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromPartialReflections
title: AmplitudeAmplificationFromPartialReflections 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromPartialReflections
qsharp.summary: Amplitude amplification by partial reflections.
ms.openlocfilehash: fc7c2c0d05ea626f7f7e5d8ebf3ce5ecea61390b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721950"
---
# <a name="amplitudeamplificationfrompartialreflections-function"></a><span data-ttu-id="1b333-102">AmplitudeAmplificationFromPartialReflections 함수</span><span class="sxs-lookup"><span data-stu-id="1b333-102">AmplitudeAmplificationFromPartialReflections function</span></span>

<span data-ttu-id="1b333-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="1b333-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="1b333-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1b333-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1b333-105">부분 반사에의 한 진폭 증폭입니다.</span><span class="sxs-lookup"><span data-stu-id="1b333-105">Amplitude amplification by partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromPartialReflections (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="1b333-106">입력</span><span class="sxs-lookup"><span data-stu-id="1b333-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="1b333-107">단계: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="1b333-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="1b333-108">부분 반사의 단계</span><span class="sxs-lookup"><span data-stu-id="1b333-108">Phases of partial reflections</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="1b333-109">startStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="1b333-109">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="1b333-110">시작 상태에 대 한 리플렉션 연산자</span><span class="sxs-lookup"><span data-stu-id="1b333-110">Reflection operator about start state</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="1b333-111">targetStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="1b333-111">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="1b333-112">대상 상태에 대 한 리플렉션 연산자</span><span class="sxs-lookup"><span data-stu-id="1b333-112">Reflection operator about target state</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="1b333-113">출력: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="1b333-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="1b333-114">부분 반사로 진폭 증폭을 구현 하는 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="1b333-114">An operation that implements amplitude amplification by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b333-115">설명</span><span class="sxs-lookup"><span data-stu-id="1b333-115">Remarks</span></span>

<span data-ttu-id="1b333-116">진폭 증폭은 명확한 진폭 증폭의 특수 한 경우 이며,이 경우 시스템의 비트가 없으며 명확한 oracle이 identity로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b333-116">Amplitude amplification is a special case of oblivious amplitude amplification where there are no system qubits and the oblivious oracle is set to identity.</span></span>
<span data-ttu-id="1b333-117">대부분의 경우 `startQubits` 는 $ \ket{\text{start}} \_ $1의 $-$1 eigenstate에서 초기화 됩니다 `startStateReflection` .</span><span class="sxs-lookup"><span data-stu-id="1b333-117">In most cases, `startQubits` is initialized in the state $\ket{\text{start}}\_1$, which is the $-1$ eigenstate of `startStateReflection`.</span></span>