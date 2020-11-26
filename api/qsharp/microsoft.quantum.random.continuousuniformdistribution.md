---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: ContinuousUniformDistribution 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: a3911fe9962ce18daa239de0272c53d83344134a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193083"
---
# <a name="continuousuniformdistribution-function"></a><span data-ttu-id="78df5-102">ContinuousUniformDistribution 함수</span><span class="sxs-lookup"><span data-stu-id="78df5-102">ContinuousUniformDistribution function</span></span>

<span data-ttu-id="78df5-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="78df5-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="78df5-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="78df5-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="78df5-105">지정 된 포함 간격에 대해 균일 한 분포를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="78df5-105">Returns a uniform distribution over a given inclusive interval.</span></span>

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="78df5-106">입력</span><span class="sxs-lookup"><span data-stu-id="78df5-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="78df5-107">min: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="78df5-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="78df5-108">그릴 최소 실수입니다.</span><span class="sxs-lookup"><span data-stu-id="78df5-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="78df5-109">최대값: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="78df5-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="78df5-110">그릴 최대 실수입니다.</span><span class="sxs-lookup"><span data-stu-id="78df5-110">The largest real number to be drawn.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="78df5-111">출력: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="78df5-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="78df5-112">난수를 생성 하는 분포는의 포괄 간격에서 단일 확률을 갖는 실제 숫자입니다 `min` `max` .</span><span class="sxs-lookup"><span data-stu-id="78df5-112">A distribution whose random variates are real numbers in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="78df5-113">설명</span><span class="sxs-lookup"><span data-stu-id="78df5-113">Remarks</span></span>

<span data-ttu-id="78df5-114">인 경우 실패 `max <= min` 합니다.</span><span class="sxs-lookup"><span data-stu-id="78df5-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="78df5-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="78df5-115">See Also</span></span>

- [<span data-ttu-id="78df5-116">DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="78df5-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)