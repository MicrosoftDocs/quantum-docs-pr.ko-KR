---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: InferredLabel 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: 46b24c283a01e6ac1c959ee4a6899591ee708ff7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848412"
---
# <a name="inferredlabel-function"></a><span data-ttu-id="20eac-102">InferredLabel 함수</span><span class="sxs-lookup"><span data-stu-id="20eac-102">InferredLabel function</span></span>

<span data-ttu-id="20eac-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="20eac-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="20eac-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="20eac-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="20eac-105">분류 확률 및 바이어스가 지정 된 경우 해당 확률에서 유추 된 레이블을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="20eac-105">Given a of classification probability and a bias, returns the label inferred from that probability.</span></span>

```qsharp
function InferredLabel (bias : Double, probability : Double) : Int
```


## <a name="input"></a><span data-ttu-id="20eac-106">입력</span><span class="sxs-lookup"><span data-stu-id="20eac-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="20eac-107">바이어스: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="20eac-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="20eac-108">두 클래스 간의 편차 (일반적으로 분류자 학습의 결과)입니다.</span><span class="sxs-lookup"><span data-stu-id="20eac-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probability--double"></a><span data-ttu-id="20eac-109">확률: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="20eac-109">probability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="20eac-110">특정 샘플에 대 한 분류 확률입니다. 일반적으로 분류 빈도를 예측 한 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="20eac-110">A classification probabilities for a particular sample, typically resulting from estimating its classification frequency.</span></span>



## <a name="output--int"></a><span data-ttu-id="20eac-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="20eac-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="20eac-112">지정 된 분류 확률에서 유추 된 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="20eac-112">The label inferred from the given classification probability.</span></span>