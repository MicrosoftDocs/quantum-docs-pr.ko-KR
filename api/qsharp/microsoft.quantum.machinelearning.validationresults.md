---
uid: Microsoft.Quantum.MachineLearning.ValidationResults
title: ValidationResults 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidationResults
qsharp.summary: The results from having validated a classifier against a set of samples.
ms.openlocfilehash: 1e54a5a086035f5f8d36d777badb306156d99600
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720428"
---
# <a name="validationresults-user-defined-type"></a><span data-ttu-id="46f6a-102">ValidationResults 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="46f6a-102">ValidationResults user defined type</span></span>

<span data-ttu-id="46f6a-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="46f6a-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="46f6a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="46f6a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="46f6a-105">이 결과는 샘플 집합에 대해 분류자의 유효성을 검사 한 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="46f6a-105">The results from having validated a classifier against a set of samples.</span></span>

```qsharp

newtype ValidationResults = (NMisclassifications : Int, NValidationSamples : Int);
```



## <a name="named-items"></a><span data-ttu-id="46f6a-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="46f6a-106">Named Items</span></span>

### <a name="nmisclassifications--int"></a><span data-ttu-id="46f6a-107">N잘못 분류: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="46f6a-107">NMisclassifications : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="46f6a-108">유효성을 검사 하는 동안 관찰 된 오 분류 수입니다.</span><span class="sxs-lookup"><span data-stu-id="46f6a-108">The number of misclassifications observed during validation.</span></span>
### <a name="nvalidationsamples--int"></a><span data-ttu-id="46f6a-109">NValidationSamples: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="46f6a-109">NValidationSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

