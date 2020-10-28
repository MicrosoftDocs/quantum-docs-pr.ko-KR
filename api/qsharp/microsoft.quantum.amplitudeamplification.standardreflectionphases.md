---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: StandardReflectionPhases 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: c189b34b641989ab458986fb3f2872759b949be5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721733"
---
# <a name="standardreflectionphases-function"></a><span data-ttu-id="fea5d-102">StandardReflectionPhases 함수</span><span class="sxs-lookup"><span data-stu-id="fea5d-102">StandardReflectionPhases function</span></span>

<span data-ttu-id="fea5d-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="fea5d-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="fea5d-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fea5d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fea5d-105">표준 진폭 증폭의 부분 반사 단계를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="fea5d-105">Computes partial reflection phases for standard amplitude amplification.</span></span>

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="fea5d-106">입력</span><span class="sxs-lookup"><span data-stu-id="fea5d-106">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="fea5d-107">nIterations: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fea5d-107">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fea5d-108">에 대 한 부분 반사 단계를 생성 하는 진폭 증폭 반복의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fea5d-108">Number of amplitude amplification iterations to generate partial reflection phases for.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="fea5d-109">출력: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="fea5d-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="fea5d-110">부분 반사로 지정 된 단계를 구현 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="fea5d-110">An operation that implements phases specified as partial reflections</span></span>

## <a name="remarks"></a><span data-ttu-id="fea5d-111">설명</span><span class="sxs-lookup"><span data-stu-id="fea5d-111">Remarks</span></span>

<span data-ttu-id="fea5d-112">모든 단계는 시작 상태와 대상 상태에 대 한 마지막 반사 ($0 $)에 대 한 첫 번째 리플렉션을 제외 하 고 $ \pi $입니다.</span><span class="sxs-lookup"><span data-stu-id="fea5d-112">All phases are $\pi$, except for the first reflection about the start state and the last reflection about the target state, which are $0$.</span></span>