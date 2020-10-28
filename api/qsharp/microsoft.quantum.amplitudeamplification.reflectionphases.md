---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: ReflectionPhases 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: e0c7db6cd1aad636a34684958be117de1b9888f8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721817"
---
# <a name="reflectionphases-user-defined-type"></a><span data-ttu-id="eab54-102">ReflectionPhases 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="eab54-102">ReflectionPhases user defined type</span></span>

<span data-ttu-id="eab54-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="eab54-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="eab54-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="eab54-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="eab54-105">진폭 증폭의 부분 반사 시퀀스에 대 한 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="eab54-105">Phases for a sequence of partial reflections in amplitude amplification.</span></span>

```qsharp

newtype ReflectionPhases = (AboutStart : Double[], AboutTarget : Double[]);
```



## <a name="named-items"></a><span data-ttu-id="eab54-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="eab54-106">Named Items</span></span>

### <a name="aboutstart--double"></a><span data-ttu-id="eab54-107">AboutStart: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="eab54-107">AboutStart : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="eab54-108">시작 상태를 반영 하기 위한 단계의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="eab54-108">An array of phases for reflection about the start state.</span></span>
### <a name="abouttarget--double"></a><span data-ttu-id="eab54-109">AboutTarget: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="eab54-109">AboutTarget : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="eab54-110">대상 상태에 대 한 리플렉션의 단계 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="eab54-110">An array of phases for reflection about the target state.</span></span>

## <a name="remarks"></a><span data-ttu-id="eab54-111">설명</span><span class="sxs-lookup"><span data-stu-id="eab54-111">Remarks</span></span>

<span data-ttu-id="eab54-112">두 배열의 길이는 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eab54-112">Both arrays must be of equal length.</span></span> <span data-ttu-id="eab54-113">대부분의 경우 시작 상태와 대상 상태에 대 한 마지막 단계에 대 한 첫 번째 단계는 글로벌 위상 교대조를 소개 하며, $0 $로 설정 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eab54-113">Note that in many cases, the first phase about the start state and last phase about the target state introduces a global phase shift and may be set to $0$.</span></span>