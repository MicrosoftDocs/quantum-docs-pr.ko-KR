---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: DrawRandomDouble 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: 792e9c714b761b48618aec2091e167a359c2b522
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847618"
---
# <a name="drawrandomdouble-operation"></a><span data-ttu-id="6d2df-102">DrawRandomDouble 작업</span><span class="sxs-lookup"><span data-stu-id="6d2df-102">DrawRandomDouble operation</span></span>

<span data-ttu-id="6d2df-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="6d2df-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="6d2df-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="6d2df-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="6d2df-105">지정 된 포함 간격으로 임의의 실수를 그립니다.</span><span class="sxs-lookup"><span data-stu-id="6d2df-105">Draws a random real number in a given inclusive interval.</span></span>

```qsharp
operation DrawRandomDouble (min : Double, max : Double) : Double
```


## <a name="input"></a><span data-ttu-id="6d2df-106">입력</span><span class="sxs-lookup"><span data-stu-id="6d2df-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="6d2df-107">min: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6d2df-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6d2df-108">그릴 최소 실수입니다.</span><span class="sxs-lookup"><span data-stu-id="6d2df-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="6d2df-109">최대값: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6d2df-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6d2df-110">그릴 최대 실수입니다.</span><span class="sxs-lookup"><span data-stu-id="6d2df-110">The largest real number to be drawn.</span></span>



## <a name="output--double"></a><span data-ttu-id="6d2df-111">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6d2df-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6d2df-112">에서로의 포괄 간격의 임의의 실수 `min` `max` 입니다.</span><span class="sxs-lookup"><span data-stu-id="6d2df-112">A random real number in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="example"></a><span data-ttu-id="6d2df-113">예</span><span class="sxs-lookup"><span data-stu-id="6d2df-113">Example</span></span>

<span data-ttu-id="6d2df-114">다음 Q # 코드 조각은 임의로 $0 $과 $2 \pi $ 사이의 각도를 그립니다.</span><span class="sxs-lookup"><span data-stu-id="6d2df-114">The following Q# snippet randomly draws an angle between $0$ and $2 \pi$:</span></span>

```qsharp
let angle = DrawRandomDouble(0.0, 2.0 * PI());
```

## <a name="remarks"></a><span data-ttu-id="6d2df-115">설명</span><span class="sxs-lookup"><span data-stu-id="6d2df-115">Remarks</span></span>

<span data-ttu-id="6d2df-116">인 경우 실패 `max <= min` 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d2df-116">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d2df-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6d2df-117">See Also</span></span>

- [<span data-ttu-id="6d2df-118">ContinuousUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="6d2df-118">Microsoft.Quantum.ContinuousUniformDistribution</span></span>](xref:Microsoft.Quantum.ContinuousUniformDistribution)