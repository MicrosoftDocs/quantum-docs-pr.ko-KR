---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: RotationPhases 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: b0373f964b77f8ea561c6e96b11e476b42e7fc55
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721768"
---
# <a name="rotationphases-user-defined-type"></a><span data-ttu-id="f7662-102">RotationPhases 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="f7662-102">RotationPhases user defined type</span></span>

<span data-ttu-id="f7662-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="f7662-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="f7662-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f7662-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f7662-105">진폭 증폭에서 단일 비트 회전의 시퀀스에 대 한 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="f7662-105">Phases for a sequence of single-qubit rotations in amplitude amplification.</span></span>

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a><span data-ttu-id="f7662-106">설명</span><span class="sxs-lookup"><span data-stu-id="f7662-106">Remarks</span></span>

<span data-ttu-id="f7662-107">첫 번째 매개 변수는 단일가 나 비트 회전의 곱으로 표현 되는 반사의 단계 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f7662-107">The first parameter is an array of phases for reflections, expressed as a product of single-qubit rotations.</span></span>
<span data-ttu-id="f7662-108">[ G.H.</span><span class="sxs-lookup"><span data-stu-id="f7662-108">[ G.H.</span></span> <span data-ttu-id="f7662-109">낮음, L. L.</span><span class="sxs-lookup"><span data-stu-id="f7662-109">Low, I. L.</span></span> <span data-ttu-id="f7662-110">Chuang, https://arxiv.org/abs/1707.05391 ].</span><span class="sxs-lookup"><span data-stu-id="f7662-110">Chuang, https://arxiv.org/abs/1707.05391].</span></span>