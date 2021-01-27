---
uid: Microsoft.Quantum.Math.ComplexPolarAsComplex
title: ComplexPolarAsComplex 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolarAsComplex
qsharp.summary: Converts a complex number of type `ComplexPolar` to a complex number of type `Complex`.
ms.openlocfilehash: 6834b47705d080d4597ae1a6037462521fac45f7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853882"
---
# <a name="complexpolarascomplex-function"></a>ComplexPolarAsComplex 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


복소수 수를 형식의 복소수로 변환 `ComplexPolar` `Complex` 합니다.

```qsharp
function ComplexPolarAsComplex (input : Microsoft.Quantum.Math.ComplexPolar) : Microsoft.Quantum.Math.Complex
```


## <a name="input"></a>입력

### <a name="input--complexpolar"></a>입력: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)

복소수 $c = r e ^ {i t} $입니다.



## <a name="output--complex"></a>출력: [복합](xref:Microsoft.Quantum.Math.Complex)

복소수 $c = x + i y $입니다.