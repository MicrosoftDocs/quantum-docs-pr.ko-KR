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