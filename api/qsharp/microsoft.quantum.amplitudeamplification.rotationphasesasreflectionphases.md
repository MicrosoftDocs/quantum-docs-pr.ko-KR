---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhasesAsReflectionPhases
title: RotationPhasesAsReflectionPhases 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhasesAsReflectionPhases
qsharp.summary: Converts phases specified as single-qubit rotations to phases specified as partial reflections.
ms.openlocfilehash: 6e601cfd867b449d628da7cd60dfacd465e48860
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191196"
---
# <a name="rotationphasesasreflectionphases-function"></a><span data-ttu-id="1fbd1-102">RotationPhasesAsReflectionPhases 함수</span><span class="sxs-lookup"><span data-stu-id="1fbd1-102">RotationPhasesAsReflectionPhases function</span></span>

<span data-ttu-id="1fbd1-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="1fbd1-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="1fbd1-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1fbd1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1fbd1-105">단일 비트 회전으로 지정 된 단계를 부분 반사로 지정 된 단계로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fbd1-105">Converts phases specified as single-qubit rotations to phases specified as partial reflections.</span></span>

```qsharp
function RotationPhasesAsReflectionPhases (rotPhases : Microsoft.Quantum.AmplitudeAmplification.RotationPhases) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="1fbd1-106">입력</span><span class="sxs-lookup"><span data-stu-id="1fbd1-106">Input</span></span>

### <a name="rotphases--rotationphases"></a><span data-ttu-id="1fbd1-107">rotPhases: [RotationPhases](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)</span><span class="sxs-lookup"><span data-stu-id="1fbd1-107">rotPhases : [RotationPhases](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)</span></span>

<span data-ttu-id="1fbd1-108">부분 반사로 변환할 단일 비트 회전의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbd1-108">Array of single-qubit rotations to be converted to partial reflections.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="1fbd1-109">출력: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="1fbd1-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="1fbd1-110">부분 반사로 지정 된 단계를 구현 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbd1-110">An operation that implements phases specified as partial reflections.</span></span>

## <a name="references"></a><span data-ttu-id="1fbd1-111">참조 항목</span><span class="sxs-lookup"><span data-stu-id="1fbd1-111">References</span></span>

<span data-ttu-id="1fbd1-112">에서 규칙을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fbd1-112">We use the convention in</span></span>

- <span data-ttu-id="1fbd1-113">[ *G.H. Low, Chuang, a. L. L. L.*](https://arxiv.org/abs/1707.05391)</span><span class="sxs-lookup"><span data-stu-id="1fbd1-113">[ *G.H. Low, I. L. Chuang* ](https://arxiv.org/abs/1707.05391) for relating single-qubit rotation phases to reflection operator phases.</span></span>