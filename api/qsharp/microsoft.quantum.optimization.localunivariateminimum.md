---
uid: Microsoft.Quantum.Optimization.LocalUnivariateMinimum
title: LocalUnivariateMinimum 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: LocalUnivariateMinimum
qsharp.summary: Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.
ms.openlocfilehash: 3b09af88bbed20a392768d005e5e9567b3bb7022
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711019"
---
# <a name="localunivariateminimum-function"></a><span data-ttu-id="d7962-102">LocalUnivariateMinimum 함수</span><span class="sxs-lookup"><span data-stu-id="d7962-102">LocalUnivariateMinimum function</span></span>

<span data-ttu-id="d7962-103">네임 스페이스: [Microsoft 양자 최적화](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="d7962-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="d7962-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d7962-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d7962-105">골든 간격 검색을 사용 하 여 제한 된 간격에 걸쳐 단일 함수에 대 한 지역 최소값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7962-105">Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.</span></span>

```qsharp
function LocalUnivariateMinimum (fn : (Double -> Double), bounds : (Double, Double), tolerance : Double) : Microsoft.Quantum.Optimization.UnivariateOptimizationResult
```


## <a name="input"></a><span data-ttu-id="d7962-106">입력</span><span class="sxs-lookup"><span data-stu-id="d7962-106">Input</span></span>

### <a name="fn--double---double"></a><span data-ttu-id="d7962-107">fn: [이중](xref:microsoft.quantum.lang-ref.double) -> [double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d7962-107">fn : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d7962-108">최소화할 수 있는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="d7962-108">The univariate function to be minimized.</span></span>


### <a name="bounds--doubledouble"></a><span data-ttu-id="d7962-109">범위: ([double](xref:microsoft.quantum.lang-ref.double),[double](xref:microsoft.quantum.lang-ref.double))</span><span class="sxs-lookup"><span data-stu-id="d7962-109">bounds : ([Double](xref:microsoft.quantum.lang-ref.double),[Double](xref:microsoft.quantum.lang-ref.double))</span></span>

<span data-ttu-id="d7962-110">로컬 최소값을 찾을 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="d7962-110">The interval in which the local minimum is to be found.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="d7962-111">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d7962-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d7962-112">허용 되는 함수 입력의 정확도입니다.</span><span class="sxs-lookup"><span data-stu-id="d7962-112">The accuracy in the function input to be tolerated.</span></span>
<span data-ttu-id="d7962-113">로컬 optima 검색은 간격이이 허용 오차 보다 작을 때까지 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7962-113">The search for local optima will continue until the interval is smaller in width than this tolerance.</span></span>



## <a name="output--univariateoptimizationresult"></a><span data-ttu-id="d7962-114">출력: [UnivariateOptimizationResult](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)</span><span class="sxs-lookup"><span data-stu-id="d7962-114">Output : [UnivariateOptimizationResult](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)</span></span>

<span data-ttu-id="d7962-115">지정 된 범위 내에 있는 지정 된 함수의 로컬 optima.</span><span class="sxs-lookup"><span data-stu-id="d7962-115">A local optima of the given function, located within the given bounds.</span></span>