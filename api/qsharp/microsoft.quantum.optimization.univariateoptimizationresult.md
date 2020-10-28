---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: UnivariateOptimizationResult 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: c8aa91bbdc9e9e9bb4d110b470ff2041f9460a38
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724323"
---
# <a name="univariateoptimizationresult-user-defined-type"></a><span data-ttu-id="48227-102">UnivariateOptimizationResult 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="48227-102">UnivariateOptimizationResult user defined type</span></span>

<span data-ttu-id="48227-103">네임 스페이스: [Microsoft 양자 최적화](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="48227-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="48227-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="48227-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="48227-105">단일 함수를 최적화 한 결과를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="48227-105">Represents the result of optimizing a univariate function.</span></span>

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a><span data-ttu-id="48227-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="48227-106">Named Items</span></span>

### <a name="coordinate--double"></a><span data-ttu-id="48227-107">좌표: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="48227-107">Coordinate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="48227-108">최적가 발견 된 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="48227-108">Input at which an optimum was found.</span></span>
### <a name="value--double"></a><span data-ttu-id="48227-109">값: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="48227-109">Value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="48227-110">함수가 최적으로 반환 하는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="48227-110">Value returned by the function at its optimum.</span></span>