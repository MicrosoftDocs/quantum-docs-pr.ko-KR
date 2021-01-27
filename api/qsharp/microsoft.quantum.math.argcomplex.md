---
uid: Microsoft.Quantum.Math.ArgComplex
title: ArgComplex 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: e8ce73a43940ab0ed66338f962cc6f76fc2b694b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842766"
---
# <a name="argcomplex-function"></a>ArgComplex 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


복소수 형식의 단계를 반환 합니다 `Complex` .

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a>입력

### <a name="input--complex"></a>입력: [복합](xref:Microsoft.Quantum.Math.Complex)

복소수 $c = x + i y $입니다.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)

단계 $ \text{Arg} [c] = \text{ArcTan} (y, x) \in (-\pi, \pi] $.