---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhasesAsReflectionPhases
title: RotationPhasesAsReflectionPhases 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhasesAsReflectionPhases
qsharp.summary: Converts phases specified as single-qubit rotations to phases specified as partial reflections.
ms.openlocfilehash: 5d50b3fdc2b0f948e93cb11b5c69403d97574ccd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843947"
---
# <a name="rotationphasesasreflectionphases-function"></a><span data-ttu-id="4d32a-102">RotationPhasesAsReflectionPhases 함수</span><span class="sxs-lookup"><span data-stu-id="4d32a-102">RotationPhasesAsReflectionPhases function</span></span>

<span data-ttu-id="4d32a-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="4d32a-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="4d32a-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4d32a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4d32a-105">단일 비트 회전으로 지정 된 단계를 부분 반사로 지정 된 단계로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d32a-105">Converts phases specified as single-qubit rotations to phases specified as partial reflections.</span></span>

```qsharp
function RotationPhasesAsReflectionPhases (rotPhases : Microsoft.Quantum.AmplitudeAmplification.RotationPhases) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="4d32a-106">입력</span><span class="sxs-lookup"><span data-stu-id="4d32a-106">Input</span></span>

### <a name="rotphases--rotationphases"></a><span data-ttu-id="4d32a-107">rotPhases: [RotationPhases](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)</span><span class="sxs-lookup"><span data-stu-id="4d32a-107">rotPhases : [RotationPhases](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)</span></span>

<span data-ttu-id="4d32a-108">부분 반사로 변환할 단일 비트 회전의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="4d32a-108">Array of single-qubit rotations to be converted to partial reflections.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="4d32a-109">출력: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="4d32a-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="4d32a-110">부분 반사로 지정 된 단계를 구현 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="4d32a-110">An operation that implements phases specified as partial reflections.</span></span>

## <a name="references"></a><span data-ttu-id="4d32a-111">참조</span><span class="sxs-lookup"><span data-stu-id="4d32a-111">References</span></span>

<span data-ttu-id="4d32a-112">에서 규칙을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d32a-112">We use the convention in</span></span>

- <span data-ttu-id="4d32a-113">[ *G.H. Low, Chuang, a. L. L. L.*](https://arxiv.org/abs/1707.05391)</span><span class="sxs-lookup"><span data-stu-id="4d32a-113">[ *G.H. Low, I. L. Chuang* ](https://arxiv.org/abs/1707.05391) for relating single-qubit rotation phases to reflection operator phases.</span></span>