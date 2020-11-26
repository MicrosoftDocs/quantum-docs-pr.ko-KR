---
uid: Microsoft.Quantum.Math.ComplexAsComplexPolar
title: ComplexAsComplexPolar 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexAsComplexPolar
qsharp.summary: Converts a complex number of type `Complex` to a complex number of type `ComplexPolar`.
ms.openlocfilehash: 5155583291e69a78df66f3b77d758fc1708d9146
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195633"
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