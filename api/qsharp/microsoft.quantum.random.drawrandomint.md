---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: DrawRandomInt 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: ebed7f52b7c4a8c538ed9d718c486b5aa94a0327
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851134"
---
# <a name="drawrandomint-operation"></a><span data-ttu-id="780ca-102">DrawRandomInt 작업</span><span class="sxs-lookup"><span data-stu-id="780ca-102">DrawRandomInt operation</span></span>

<span data-ttu-id="780ca-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="780ca-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="780ca-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="780ca-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="780ca-105">지정 된 포함 범위에서 임의의 정수를 그립니다.</span><span class="sxs-lookup"><span data-stu-id="780ca-105">Draws a random integer in a given inclusive range.</span></span>

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a><span data-ttu-id="780ca-106">입력</span><span class="sxs-lookup"><span data-stu-id="780ca-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="780ca-107">min: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="780ca-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="780ca-108">그릴 가장 작은 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="780ca-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="780ca-109">최대: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="780ca-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="780ca-110">그릴 가장 큰 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="780ca-110">The largest integer to be drawn.</span></span>



## <a name="output--int"></a><span data-ttu-id="780ca-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="780ca-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="780ca-112">의 포함 범위에서에 해당 하는 정수 `min` `max` 입니다.</span><span class="sxs-lookup"><span data-stu-id="780ca-112">An integer in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="example"></a><span data-ttu-id="780ca-113">예</span><span class="sxs-lookup"><span data-stu-id="780ca-113">Example</span></span>

<span data-ttu-id="780ca-114">다음 Q # 코드 조각은 임의로 6 면 주사위를 롤업 합니다.</span><span class="sxs-lookup"><span data-stu-id="780ca-114">The following Q# snippet randomly rolls a six-sided die:</span></span>

```qsharp
let roll = DrawRandomInt(1, 6);
```

## <a name="remarks"></a><span data-ttu-id="780ca-115">설명</span><span class="sxs-lookup"><span data-stu-id="780ca-115">Remarks</span></span>

<span data-ttu-id="780ca-116">인 경우 실패 `max <= min` 합니다.</span><span class="sxs-lookup"><span data-stu-id="780ca-116">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="780ca-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="780ca-117">See Also</span></span>

- [<span data-ttu-id="780ca-118">DiscreteUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="780ca-118">Microsoft.Quantum.DiscreteUniformDistribution</span></span>](xref:Microsoft.Quantum.DiscreteUniformDistribution)