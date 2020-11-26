---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: RotationPhases 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: 60fcda7d58a19f8891e252ddb18b504afddf5514
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191366"
---
# <a name="rotationphases-user-defined-type"></a><span data-ttu-id="f0c2d-102">RotationPhases 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="f0c2d-102">RotationPhases user defined type</span></span>

<span data-ttu-id="f0c2d-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="f0c2d-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="f0c2d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f0c2d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f0c2d-105">진폭 증폭에서 단일 비트 회전의 시퀀스에 대 한 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="f0c2d-105">Phases for a sequence of single-qubit rotations in amplitude amplification.</span></span>

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a><span data-ttu-id="f0c2d-106">설명</span><span class="sxs-lookup"><span data-stu-id="f0c2d-106">Remarks</span></span>

<span data-ttu-id="f0c2d-107">첫 번째 매개 변수는 단일가 나 비트 회전의 곱으로 표현 되는 반사의 단계 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f0c2d-107">The first parameter is an array of phases for reflections, expressed as a product of single-qubit rotations.</span></span>
<span data-ttu-id="f0c2d-108">[ G.H.</span><span class="sxs-lookup"><span data-stu-id="f0c2d-108">[ G.H.</span></span> <span data-ttu-id="f0c2d-109">낮음, L. L.</span><span class="sxs-lookup"><span data-stu-id="f0c2d-109">Low, I. L.</span></span> <span data-ttu-id="f0c2d-110">Chuang, https://arxiv.org/abs/1707.05391 ].</span><span class="sxs-lookup"><span data-stu-id="f0c2d-110">Chuang, https://arxiv.org/abs/1707.05391].</span></span>