---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: LabeledSample 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: b357aae20b5bddb968ce1906fed3c1001efbfde7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846973"
---
# <a name="labeledsample-user-defined-type"></a><span data-ttu-id="5fee4-102">LabeledSample 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="5fee4-102">LabeledSample user defined type</span></span>

<span data-ttu-id="5fee4-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="5fee4-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="5fee4-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="5fee4-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="5fee4-105">예제가 속한 클래스를 사용 하 여 레이블이 지정 된 샘플입니다.</span><span class="sxs-lookup"><span data-stu-id="5fee4-105">A sample, labeled with a class to which that sample belongs.</span></span>

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a><span data-ttu-id="5fee4-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="5fee4-106">Named Items</span></span>

### <a name="features--double"></a><span data-ttu-id="5fee4-107">기능: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="5fee4-107">Features : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="5fee4-108">지정 된 샘플에 대 한 기능 벡터입니다.</span><span class="sxs-lookup"><span data-stu-id="5fee4-108">A vector of features for the given sample.</span></span>
### <a name="label--int"></a><span data-ttu-id="5fee4-109">레이블: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5fee4-109">Label : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5fee4-110">이 샘플이 속한 클래스의 정수 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="5fee4-110">An integer label for the class to which this sample belongs.</span></span>