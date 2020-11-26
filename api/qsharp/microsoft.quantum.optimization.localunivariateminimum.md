---
uid: Microsoft.Quantum.Optimization.LocalUnivariateMinimum
title: LocalUnivariateMinimum 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: LocalUnivariateMinimum
qsharp.summary: Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.
ms.openlocfilehash: e804e6a6ed82f14dcc9b8f721ad503d77922dc0f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194086"
---
# <a name="localunivariateminimum-function"></a><span data-ttu-id="fe0a1-102">LocalUnivariateMinimum 함수</span><span class="sxs-lookup"><span data-stu-id="fe0a1-102">LocalUnivariateMinimum function</span></span>

<span data-ttu-id="fe0a1-103">네임 스페이스: [Microsoft 양자 최적화](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="fe0a1-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="fe0a1-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fe0a1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fe0a1-105">골든 간격 검색을 사용 하 여 제한 된 간격에 걸쳐 단일 함수에 대 한 지역 최소값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-105">Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.</span></span>

```qsharp
function LocalUnivariateMinimum (fn : (Double -> Double), bounds : (Double, Double), tolerance : Double) : Microsoft.Quantum.Optimization.UnivariateOptimizationResult
```


## <a name="input"></a><span data-ttu-id="fe0a1-106">입력</span><span class="sxs-lookup"><span data-stu-id="fe0a1-106">Input</span></span>

### <a name="fn--double---double"></a><span data-ttu-id="fe0a1-107">fn: [이중](xref:microsoft.quantum.lang-ref.double) -> [double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fe0a1-107">fn : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fe0a1-108">최소화할 수 있는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-108">The univariate function to be minimized.</span></span>


### <a name="bounds--doubledouble"></a><span data-ttu-id="fe0a1-109">범위: ([double](xref:microsoft.quantum.lang-ref.double),[double](xref:microsoft.quantum.lang-ref.double))</span><span class="sxs-lookup"><span data-stu-id="fe0a1-109">bounds : ([Double](xref:microsoft.quantum.lang-ref.double),[Double](xref:microsoft.quantum.lang-ref.double))</span></span>

<span data-ttu-id="fe0a1-110">로컬 최소값을 찾을 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-110">The interval in which the local minimum is to be found.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="fe0a1-111">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fe0a1-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fe0a1-112">허용 되는 함수 입력의 정확도입니다.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-112">The accuracy in the function input to be tolerated.</span></span>
<span data-ttu-id="fe0a1-113">로컬 optima 검색은 간격이이 허용 오차 보다 작을 때까지 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-113">The search for local optima will continue until the interval is smaller in width than this tolerance.</span></span>



## <a name="output--univariateoptimizationresult"></a><span data-ttu-id="fe0a1-114">출력: [UnivariateOptimizationResult](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)</span><span class="sxs-lookup"><span data-stu-id="fe0a1-114">Output : [UnivariateOptimizationResult](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)</span></span>

<span data-ttu-id="fe0a1-115">지정 된 범위 내에 있는 지정 된 함수의 로컬 optima.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-115">A local optima of the given function, located within the given bounds.</span></span>