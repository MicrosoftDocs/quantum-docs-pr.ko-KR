---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: 잘못 분류 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: e13a9b9b65931678d5d87878e81fa172329a28ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211681"
---
# <a name="misclassifications-function"></a><span data-ttu-id="cf5ba-102">잘못 분류 함수</span><span class="sxs-lookup"><span data-stu-id="cf5ba-102">Misclassifications function</span></span>

<span data-ttu-id="cf5ba-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="cf5ba-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="cf5ba-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="cf5ba-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="cf5ba-105">유추 된 레이블 집합과 올바른 레이블 집합을 지정 하면 각 레이블 집합이 다른에 대 한 인덱스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ba-105">Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.</span></span>

```qsharp
function Misclassifications (inferredLabels : Int[], actualLabels : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="cf5ba-106">입력</span><span class="sxs-lookup"><span data-stu-id="cf5ba-106">Input</span></span>

### <a name="inferredlabels--int"></a><span data-ttu-id="cf5ba-107">inferredLabels: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="cf5ba-107">inferredLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="cf5ba-108">지정 된 학습 또는 유효성 검사 집합에 대해 유추 된 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ba-108">The labels inferred for a given training or validation set.</span></span>


### <a name="actuallabels--int"></a><span data-ttu-id="cf5ba-109">actualLabels: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="cf5ba-109">actualLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="cf5ba-110">지정 된 학습 또는 유효성 검사 집합의 실제 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ba-110">The true labels for a given training or validation set.</span></span>



## <a name="output--int"></a><span data-ttu-id="cf5ba-111">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="cf5ba-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="cf5ba-112">`idx`이에 해당 하는 인덱스의 배열입니다 `inferredLabels[idx] != actualLabels[idx]` .</span><span class="sxs-lookup"><span data-stu-id="cf5ba-112">An array of indices `idx` such that `inferredLabels[idx] != actualLabels[idx]`.</span></span>