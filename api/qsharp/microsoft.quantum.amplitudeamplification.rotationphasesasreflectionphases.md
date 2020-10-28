---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhasesAsReflectionPhases
title: RotationPhasesAsReflectionPhases 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhasesAsReflectionPhases
qsharp.summary: Converts phases specified as single-qubit rotations to phases specified as partial reflections.
ms.openlocfilehash: d62a7584324c9467ccc759e4bed81acbceee719c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721754"
---
# <a name="rotationphasesasreflectionphases-function"></a><span data-ttu-id="4a70c-102">RotationPhasesAsReflectionPhases 함수</span><span class="sxs-lookup"><span data-stu-id="4a70c-102">RotationPhasesAsReflectionPhases function</span></span>

<span data-ttu-id="4a70c-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="4a70c-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="4a70c-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4a70c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4a70c-105">단일 비트 회전으로 지정 된 단계를 부분 반사로 지정 된 단계로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a70c-105">Converts phases specified as single-qubit rotations to phases specified as partial reflections.</span></span>

```qsharp
function RotationPhasesAsReflectionPhases (rotPhases : Microsoft.Quantum.AmplitudeAmplification.RotationPhases) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="4a70c-106">입력</span><span class="sxs-lookup"><span data-stu-id="4a70c-106">Input</span></span>

### <a name="rotphases--rotationphases"></a><span data-ttu-id="4a70c-107">rotPhases: [RotationPhases](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)</span><span class="sxs-lookup"><span data-stu-id="4a70c-107">rotPhases : [RotationPhases](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)</span></span>

<span data-ttu-id="4a70c-108">부분 반사로 변환할 단일 비트 회전의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="4a70c-108">Array of single-qubit rotations to be converted to partial reflections.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="4a70c-109">출력: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="4a70c-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="4a70c-110">부분 반사로 지정 된 단계를 구현 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="4a70c-110">An operation that implements phases specified as partial reflections.</span></span>

## <a name="references"></a><span data-ttu-id="4a70c-111">참조</span><span class="sxs-lookup"><span data-stu-id="4a70c-111">References</span></span>

<span data-ttu-id="4a70c-112">에서 규칙을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a70c-112">We use the convention in</span></span>

- <span data-ttu-id="4a70c-113">[ *G.H. Low, Chuang, a. L. L. L.*](https://arxiv.org/abs/1707.05391)</span><span class="sxs-lookup"><span data-stu-id="4a70c-113">[ *G.H. Low, I. L. Chuang* ](https://arxiv.org/abs/1707.05391) for relating single-qubit rotation phases to reflection operator phases.</span></span>