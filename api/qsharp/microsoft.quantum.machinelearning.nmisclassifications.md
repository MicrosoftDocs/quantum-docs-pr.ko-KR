---
uid: Microsoft.Quantum.MachineLearning.NMisclassifications
title: NMisclassifications 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NMisclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.
ms.openlocfilehash: 9e356d68233519978e007e5a2999ca1be8cb7f83
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709738"
---
# <a name="nmisclassifications-function"></a><span data-ttu-id="ae79b-102">NMisclassifications 함수</span><span class="sxs-lookup"><span data-stu-id="ae79b-102">NMisclassifications function</span></span>

<span data-ttu-id="ae79b-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ae79b-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="ae79b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ae79b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ae79b-105">유추 된 레이블 집합과 올바른 레이블 집합을 지정 하면 각 레이블 집합이 다른 인덱스 수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae79b-105">Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.</span></span>

```qsharp
function NMisclassifications (proposed : Int[], actual : Int[]) : Int
```


## <a name="input"></a><span data-ttu-id="ae79b-106">입력</span><span class="sxs-lookup"><span data-stu-id="ae79b-106">Input</span></span>

### <a name="proposed--int"></a><span data-ttu-id="ae79b-107">제안 됨: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ae79b-107">proposed : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="actual--int"></a><span data-ttu-id="ae79b-108">actual: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ae79b-108">actual : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--int"></a><span data-ttu-id="ae79b-109">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ae79b-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ae79b-110">이에 해당 하는 인덱스 수입니다 `idx` `inferredLabels[idx] != actualLabels[idx]` .</span><span class="sxs-lookup"><span data-stu-id="ae79b-110">The number of indices `idx` such that `inferredLabels[idx] != actualLabels[idx]`.</span></span>