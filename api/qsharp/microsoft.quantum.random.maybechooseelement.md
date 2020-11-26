---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: MaybeChooseElement 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 1a69c8d5a6ae022ceda9269e17434b740809b107
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192862"
---
# <a name="maybechooseelement-operation"></a><span data-ttu-id="b97aa-102">MaybeChooseElement 작업</span><span class="sxs-lookup"><span data-stu-id="b97aa-102">MaybeChooseElement operation</span></span>

<span data-ttu-id="b97aa-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="b97aa-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="b97aa-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="b97aa-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="b97aa-105">데이터 배열 및 해당 인덱스에 대 한 분포를 지정 하는 경우에서 임의로 요소를 선택 하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="b97aa-105">Given an array of data and an a distribution over its indices, attempts to choose an element at random.</span></span>

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a><span data-ttu-id="b97aa-106">입력</span><span class="sxs-lookup"><span data-stu-id="b97aa-106">Input</span></span>

### <a name="data--t"></a><span data-ttu-id="b97aa-107">데이터: ' t []</span><span class="sxs-lookup"><span data-stu-id="b97aa-107">data : 'T[]</span></span>

<span data-ttu-id="b97aa-108">요소를 선택 해야 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="b97aa-108">The array from which an element should be chosen.</span></span>


### <a name="indexdistribution--discretedistribution"></a><span data-ttu-id="b97aa-109">indexDistribution: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="b97aa-109">indexDistribution : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="b97aa-110">의 인덱스에 대 한 분포 `data` 입니다.</span><span class="sxs-lookup"><span data-stu-id="b97aa-110">A distribution over the indices of `data`.</span></span>



## <a name="output--boolt"></a><span data-ttu-id="b97aa-111">Output: ([Bool](xref:microsoft.quantum.lang-ref.bool), ' t)</span><span class="sxs-lookup"><span data-stu-id="b97aa-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b97aa-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b97aa-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b97aa-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="b97aa-113">'T</span></span>

