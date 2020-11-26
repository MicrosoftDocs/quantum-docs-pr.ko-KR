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
# <a name="localunivariateminimum-function"></a>LocalUnivariateMinimum 함수

네임 스페이스: [Microsoft 양자 최적화](xref:Microsoft.Quantum.Optimization)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


골든 간격 검색을 사용 하 여 제한 된 간격에 걸쳐 단일 함수에 대 한 지역 최소값을 반환 합니다.

```qsharp
function LocalUnivariateMinimum (fn : (Double -> Double), bounds : (Double, Double), tolerance : Double) : Microsoft.Quantum.Optimization.UnivariateOptimizationResult
```


## <a name="input"></a>입력

### <a name="fn--double---double"></a>fn: [이중](xref:microsoft.quantum.lang-ref.double) -> [double](xref:microsoft.quantum.lang-ref.double)

최소화할 수 있는 함수입니다.


### <a name="bounds--doubledouble"></a>범위: ([double](xref:microsoft.quantum.lang-ref.double),[double](xref:microsoft.quantum.lang-ref.double))

로컬 최소값을 찾을 간격입니다.


### <a name="tolerance--double"></a>허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)

허용 되는 함수 입력의 정확도입니다.
로컬 optima 검색은 간격이이 허용 오차 보다 작을 때까지 계속 됩니다.



## <a name="output--univariateoptimizationresult"></a>출력: [UnivariateOptimizationResult](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)

지정 된 범위 내에 있는 지정 된 함수의 로컬 optima.