---
uid: Microsoft.Quantum.MachineLearning.InferredLabels
title: InferredLabels 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabels
qsharp.summary: Given an array of classification probabilities and a bias, returns the label inferred from each probability.
ms.openlocfilehash: 576b4b1f11fc21476bbb019d4b0326981294528c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848402"
---
# <a name="inferredlabels-function"></a><span data-ttu-id="751a2-102">InferredLabels 함수</span><span class="sxs-lookup"><span data-stu-id="751a2-102">InferredLabels function</span></span>

<span data-ttu-id="751a2-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="751a2-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="751a2-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="751a2-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="751a2-105">분류 확률 및 바이어스의 배열이 지정 된 경우 각 확률에서 유추 된 레이블을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="751a2-105">Given an array of classification probabilities and a bias, returns the label inferred from each probability.</span></span>

```qsharp
function InferredLabels (bias : Double, probabilities : Double[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="751a2-106">입력</span><span class="sxs-lookup"><span data-stu-id="751a2-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="751a2-107">바이어스: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="751a2-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="751a2-108">두 클래스 간의 편차 (일반적으로 분류자 학습의 결과)입니다.</span><span class="sxs-lookup"><span data-stu-id="751a2-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probabilities--double"></a><span data-ttu-id="751a2-109">확률: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="751a2-109">probabilities : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="751a2-110">일반적으로 분류 빈도를 추정 하 여 얻은 샘플 집합에 대 한 분류 확률의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="751a2-110">An array of classification probabilities for a set of samples, typically resulting from estimating classification frequencies.</span></span>



## <a name="output--int"></a><span data-ttu-id="751a2-111">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="751a2-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="751a2-112">각 분류 확률에서 유추 된 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="751a2-112">The label inferred from each classification probability.</span></span>