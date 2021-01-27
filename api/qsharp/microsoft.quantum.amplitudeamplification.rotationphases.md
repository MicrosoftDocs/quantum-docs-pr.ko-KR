---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: RotationPhases 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: 2f955ce3bfb9ea057c26c79547895df39ed322ab
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843972"
---
# <a name="rotationphases-user-defined-type"></a><span data-ttu-id="1fd5e-102">RotationPhases 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="1fd5e-102">RotationPhases user defined type</span></span>

<span data-ttu-id="1fd5e-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="1fd5e-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="1fd5e-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1fd5e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1fd5e-105">진폭 증폭에서 단일 비트 회전의 시퀀스에 대 한 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="1fd5e-105">Phases for a sequence of single-qubit rotations in amplitude amplification.</span></span>

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a><span data-ttu-id="1fd5e-106">설명</span><span class="sxs-lookup"><span data-stu-id="1fd5e-106">Remarks</span></span>

<span data-ttu-id="1fd5e-107">첫 번째 매개 변수는 단일가 나 비트 회전의 곱으로 표현 되는 반사의 단계 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="1fd5e-107">The first parameter is an array of phases for reflections, expressed as a product of single-qubit rotations.</span></span>
<span data-ttu-id="1fd5e-108">[ G.H.</span><span class="sxs-lookup"><span data-stu-id="1fd5e-108">[ G.H.</span></span> <span data-ttu-id="1fd5e-109">낮음, L. L.</span><span class="sxs-lookup"><span data-stu-id="1fd5e-109">Low, I. L.</span></span> <span data-ttu-id="1fd5e-110">Chuang, https://arxiv.org/abs/1707.05391 ].</span><span class="sxs-lookup"><span data-stu-id="1fd5e-110">Chuang, https://arxiv.org/abs/1707.05391].</span></span>