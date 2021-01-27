---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: DrawRandomBool 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: 7c13f8305756421b8d07baf22ff87764efac0418
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853684"
---
# <a name="drawrandombool-operation"></a><span data-ttu-id="bc628-102">DrawRandomBool 작업</span><span class="sxs-lookup"><span data-stu-id="bc628-102">DrawRandomBool operation</span></span>

<span data-ttu-id="bc628-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="bc628-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="bc628-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="bc628-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="bc628-105">성공 확률이 지정 된 경우 지정 된 확률을 사용 하 여 true 인 단일 베르누이 평가판을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc628-105">Given a success probability, returns a single Bernoulli trial that is true with the given probability.</span></span>

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="bc628-106">입력</span><span class="sxs-lookup"><span data-stu-id="bc628-106">Input</span></span>

### <a name="successprobability--double"></a><span data-ttu-id="bc628-107">successProbability: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bc628-107">successProbability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bc628-108">이 반환 되어야 하는 확률 `true` 입니다.</span><span class="sxs-lookup"><span data-stu-id="bc628-108">The probability with which `true` should be returned.</span></span>



## <a name="output--bool"></a><span data-ttu-id="bc628-109">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="bc628-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="bc628-110">`true` 확률 `successProbability` 및 확률을 포함 `false` `1.0 - successProbability` 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc628-110">`true` with probability `successProbability` and `false` with probability `1.0 - successProbability`.</span></span>

## <a name="example"></a><span data-ttu-id="bc628-111">예</span><span class="sxs-lookup"><span data-stu-id="bc628-111">Example</span></span>

<span data-ttu-id="bc628-112">다음 Q # 코드 조각 샘플은 편향 동전에서 대칭 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc628-112">The following Q# snippet samples flips from a biased coin:</span></span>

```qsharp
let flips = DrawMany(DrawRandomBool, 10, 0.6);
```