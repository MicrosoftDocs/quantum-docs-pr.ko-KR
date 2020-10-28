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
# <a name="univariateoptimizationresult-user-defined-type"></a>UnivariateOptimizationResult 사용자 정의 형식

네임 스페이스: [Microsoft 양자 최적화](xref:Microsoft.Quantum.Optimization)

패키지 [](https://nuget.org/packages/)


단일 함수를 최적화 한 결과를 나타냅니다.

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a>명명 된 항목

### <a name="coordinate--double"></a>좌표: [Double](xref:microsoft.quantum.lang-ref.double)

최적가 발견 된 입력입니다.
### <a name="value--double"></a>값: [Double](xref:microsoft.quantum.lang-ref.double)

함수가 최적으로 반환 하는 값입니다.