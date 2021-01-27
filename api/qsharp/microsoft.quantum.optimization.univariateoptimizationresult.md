---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: UnivariateOptimizationResult 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: cc54c0035796aac86482e8a3a6896ceb197c7cfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854579"
---
# <a name="univariateoptimizationresult-user-defined-type"></a><span data-ttu-id="8ab6e-102">UnivariateOptimizationResult 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="8ab6e-102">UnivariateOptimizationResult user defined type</span></span>

<span data-ttu-id="8ab6e-103">네임 스페이스: [Microsoft 양자 최적화](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="8ab6e-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="8ab6e-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8ab6e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8ab6e-105">단일 함수를 최적화 한 결과를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8ab6e-105">Represents the result of optimizing a univariate function.</span></span>

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a><span data-ttu-id="8ab6e-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="8ab6e-106">Named Items</span></span>

### <a name="coordinate--double"></a><span data-ttu-id="8ab6e-107">좌표: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8ab6e-107">Coordinate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8ab6e-108">최적가 발견 된 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="8ab6e-108">Input at which an optimum was found.</span></span>
### <a name="value--double"></a><span data-ttu-id="8ab6e-109">값: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8ab6e-109">Value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8ab6e-110">함수가 최적으로 반환 하는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8ab6e-110">Value returned by the function at its optimum.</span></span>