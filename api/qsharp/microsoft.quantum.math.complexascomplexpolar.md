---
uid: Microsoft.Quantum.Math.ComplexAsComplexPolar
title: ComplexAsComplexPolar 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexAsComplexPolar
qsharp.summary: Converts a complex number of type `Complex` to a complex number of type `ComplexPolar`.
ms.openlocfilehash: 4d7da9b2fd79c4b39494fd1746c303a6003139eb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848858"
---
# <a name="complexascomplexpolar-function"></a>ComplexAsComplexPolar 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


복소수 수를 형식의 복소수로 변환 `Complex` `ComplexPolar` 합니다.

```qsharp
function ComplexAsComplexPolar (input : Microsoft.Quantum.Math.Complex) : Microsoft.Quantum.Math.ComplexPolar
```


## <a name="input"></a>입력

### <a name="input--complex"></a>입력: [복합](xref:Microsoft.Quantum.Math.Complex)

복소수 $c = x + i y $입니다.



## <a name="output--complexpolar"></a>출력: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)

복소수 $c = r e ^ {i t} $입니다.