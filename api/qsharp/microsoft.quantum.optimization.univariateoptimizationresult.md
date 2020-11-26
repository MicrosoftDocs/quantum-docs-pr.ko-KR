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
# <a name="univariateoptimizationresult-user-defined-type"></a>UnivariateOptimizationResult 사용자 정의 형식

네임 스페이스: [Microsoft 양자 최적화](xref:Microsoft.Quantum.Optimization)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


단일 함수를 최적화 한 결과를 나타냅니다.

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a>명명 된 항목

### <a name="coordinate--double"></a>좌표: [Double](xref:microsoft.quantum.lang-ref.double)

최적가 발견 된 입력입니다.
### <a name="value--double"></a>값: [Double](xref:microsoft.quantum.lang-ref.double)

함수가 최적으로 반환 하는 값입니다.