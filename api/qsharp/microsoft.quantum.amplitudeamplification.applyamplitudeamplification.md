---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyAmplitudeAmplification
title: ApplyAmplitudeAmplification 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyAmplitudeAmplification
qsharp.summary: Applies amplitude amplification on a given register, using a given set of phases and oracles to reflect about the initial and final states.
ms.openlocfilehash: be884eab70c7f72f994baf6bd7caf05769e0d5f2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721929"
---
# <a name="applyamplitudeamplification-operation"></a><span data-ttu-id="e6d3f-102">ApplyAmplitudeAmplification 작업</span><span class="sxs-lookup"><span data-stu-id="e6d3f-102">ApplyAmplitudeAmplification operation</span></span>

<span data-ttu-id="e6d3f-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="e6d3f-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="e6d3f-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e6d3f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e6d3f-105">지정 된 단계와 oracles를 사용 하 여 초기 및 최종 상태를 반영 하는 지정 된 레지스터에 진폭 증폭을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6d3f-105">Applies amplitude amplification on a given register, using a given set of phases and oracles to reflect about the initial and final states.</span></span>

```qsharp
operation ApplyAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e6d3f-106">입력</span><span class="sxs-lookup"><span data-stu-id="e6d3f-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="e6d3f-107">단계: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="e6d3f-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="e6d3f-108">진폭 증폭 알고리즘의 각 단계에서 부분 반사를 설명 하는 일련의 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="e6d3f-108">A set of phases describing the partial reflections at each step of the amplitude amplification algorithm.</span></span> <span data-ttu-id="e6d3f-109">예제는 @"microsoft.quantum.amplitudeamplification.standardreflectionphases"을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e6d3f-109">See @"microsoft.quantum.amplitudeamplification.standardreflectionphases" for an example.</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="e6d3f-110">startStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="e6d3f-110">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="e6d3f-111">초기 상태에 대 한 정보를 반영 하는 oracle입니다.</span><span class="sxs-lookup"><span data-stu-id="e6d3f-111">An oracle that reflects about the initial state.</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="e6d3f-112">targetStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="e6d3f-112">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="e6d3f-113">원하는 최종 상태를 반영 하는 oracle입니다.</span><span class="sxs-lookup"><span data-stu-id="e6d3f-113">An oracle that reflects about the desired final state.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="e6d3f-114">target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e6d3f-114">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e6d3f-115">진폭 증폭을 수행할 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="e6d3f-115">A register to perform amplitude amplification on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e6d3f-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e6d3f-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

