---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: FixedPointReflectionPhases 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 8cc1073447f5fae87ece38db64dcc312f6208899
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191451"
---
# <a name="fixedpointreflectionphases-function"></a><span data-ttu-id="ead4b-102">FixedPointReflectionPhases 함수</span><span class="sxs-lookup"><span data-stu-id="ead4b-102">FixedPointReflectionPhases function</span></span>

<span data-ttu-id="ead4b-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="ead4b-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="ead4b-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ead4b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ead4b-105">고정 소수점 진폭 증폭의 부분 반사 단계를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="ead4b-105">Computes partial reflection phases for fixed-point amplitude amplification.</span></span>

```qsharp
function FixedPointReflectionPhases (nQueries : Int, successMin : Double) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="ead4b-106">입력</span><span class="sxs-lookup"><span data-stu-id="ead4b-106">Input</span></span>

### <a name="nqueries--int"></a><span data-ttu-id="ead4b-107">nQueries: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ead4b-107">nQueries : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ead4b-108">Oracle 상태 준비에 대 한 쿼리 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ead4b-108">Number of queries to the state preparation oracle.</span></span> <span data-ttu-id="ead4b-109">홀수 정수 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ead4b-109">Must be an odd integer.</span></span>


### <a name="successmin--double"></a><span data-ttu-id="ead4b-110">successMin: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ead4b-110">successMin : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ead4b-111">대상 최소 성공 확률입니다.</span><span class="sxs-lookup"><span data-stu-id="ead4b-111">Target minimum success probability.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="ead4b-112">출력: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="ead4b-112">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="ead4b-113">고정 소수점 진폭 진폭 퀀텀 알고리즘 구현에 사용할 수 있는 일련의 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="ead4b-113">Array of phases that can be used in fixed-point amplitude amplification quantum algorithm implementation.</span></span>

## <a name="references"></a><span data-ttu-id="ead4b-114">참조 항목</span><span class="sxs-lookup"><span data-stu-id="ead4b-114">References</span></span>

<span data-ttu-id="ead4b-115">"고정 된 수의 쿼리 수와 함께 고정 소수점 진폭 증폭"의 단계를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ead4b-115">We use the phases in "Fixed-Point Amplitude Amplification with an Optimal Number of Queries"</span></span>

- <span data-ttu-id="ead4b-116">[YoderLowChuang2014](https://arxiv.org/abs/1409.3305) "복합 퀀텀 게이트 방법론"도 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ead4b-116">[YoderLowChuang2014](https://arxiv.org/abs/1409.3305) See also "Methodology of composite quantum gates"</span></span>
- <span data-ttu-id="ead4b-117">형식의 단계에 대 한 [LowYoderChuang2016](https://arxiv.org/abs/1603.03996) `RotationPhases` 입니다.</span><span class="sxs-lookup"><span data-stu-id="ead4b-117">[LowYoderChuang2016](https://arxiv.org/abs/1603.03996) for phases in the `RotationPhases` format.</span></span>