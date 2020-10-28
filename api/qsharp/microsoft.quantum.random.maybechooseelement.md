---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: MaybeChooseElement 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 12640d9dc3aad301146eff7bcbbaae33d3ccd420
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722167"
---
# <a name="maybechooseelement-operation"></a><span data-ttu-id="5464e-102">MaybeChooseElement 작업</span><span class="sxs-lookup"><span data-stu-id="5464e-102">MaybeChooseElement operation</span></span>

<span data-ttu-id="5464e-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="5464e-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="5464e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5464e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5464e-105">데이터 배열 및 해당 인덱스에 대 한 분포를 지정 하는 경우에서 임의로 요소를 선택 하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="5464e-105">Given an array of data and an a distribution over its indices, attempts to choose an element at random.</span></span>

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a><span data-ttu-id="5464e-106">입력</span><span class="sxs-lookup"><span data-stu-id="5464e-106">Input</span></span>

### <a name="data--t"></a><span data-ttu-id="5464e-107">데이터: ' t []</span><span class="sxs-lookup"><span data-stu-id="5464e-107">data : 'T[]</span></span>

<span data-ttu-id="5464e-108">요소를 선택 해야 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5464e-108">The array from which an element should be chosen.</span></span>


### <a name="indexdistribution--discretedistribution"></a><span data-ttu-id="5464e-109">indexDistribution: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="5464e-109">indexDistribution : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="5464e-110">의 인덱스에 대 한 분포 `data` 입니다.</span><span class="sxs-lookup"><span data-stu-id="5464e-110">A distribution over the indices of `data`.</span></span>



## <a name="output--boolt"></a><span data-ttu-id="5464e-111">Output: ([Bool](xref:microsoft.quantum.lang-ref.bool), ' t)</span><span class="sxs-lookup"><span data-stu-id="5464e-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5464e-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5464e-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5464e-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="5464e-113">'T</span></span>

