---
uid: Microsoft.Quantum.MachineLearning.ValidationResults
title: ValidationResults 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidationResults
qsharp.summary: The results from having validated a classifier against a set of samples.
ms.openlocfilehash: 923fd80333b6bf77daeaac2bf205db620e61cfd0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846085"
---
# <a name="validationresults-user-defined-type"></a><span data-ttu-id="738e3-102">ValidationResults 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="738e3-102">ValidationResults user defined type</span></span>

<span data-ttu-id="738e3-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="738e3-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="738e3-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="738e3-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="738e3-105">이 결과는 샘플 집합에 대해 분류자의 유효성을 검사 한 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="738e3-105">The results from having validated a classifier against a set of samples.</span></span>

```qsharp

newtype ValidationResults = (NMisclassifications : Int, NValidationSamples : Int);
```



## <a name="named-items"></a><span data-ttu-id="738e3-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="738e3-106">Named Items</span></span>

### <a name="nmisclassifications--int"></a><span data-ttu-id="738e3-107">N잘못 분류: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="738e3-107">NMisclassifications : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="738e3-108">유효성을 검사 하는 동안 관찰 된 오 분류 수입니다.</span><span class="sxs-lookup"><span data-stu-id="738e3-108">The number of misclassifications observed during validation.</span></span>
### <a name="nvalidationsamples--int"></a><span data-ttu-id="738e3-109">NValidationSamples: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="738e3-109">NValidationSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

