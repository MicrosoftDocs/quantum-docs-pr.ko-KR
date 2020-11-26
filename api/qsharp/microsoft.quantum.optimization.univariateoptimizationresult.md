---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: UnivariateOptimizationResult 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: 0bcdbda5586181f965297cb2a398d766f9c6fabb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194035"
---
# <a name="univariateoptimizationresult-user-defined-type"></a><span data-ttu-id="0035d-102">UnivariateOptimizationResult 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="0035d-102">UnivariateOptimizationResult user defined type</span></span>

<span data-ttu-id="0035d-103">네임 스페이스: [Microsoft 양자 최적화](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="0035d-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="0035d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0035d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0035d-105">단일 함수를 최적화 한 결과를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0035d-105">Represents the result of optimizing a univariate function.</span></span>

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a><span data-ttu-id="0035d-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="0035d-106">Named Items</span></span>

### <a name="coordinate--double"></a><span data-ttu-id="0035d-107">좌표: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0035d-107">Coordinate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0035d-108">최적가 발견 된 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="0035d-108">Input at which an optimum was found.</span></span>
### <a name="value--double"></a><span data-ttu-id="0035d-109">값: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0035d-109">Value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0035d-110">함수가 최적으로 반환 하는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="0035d-110">Value returned by the function at its optimum.</span></span>