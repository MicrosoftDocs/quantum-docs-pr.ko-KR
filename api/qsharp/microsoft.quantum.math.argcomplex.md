---
uid: Microsoft.Quantum.Math.ArgComplex
title: ArgComplex 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: 629aa32ad80e5aa3d6f5ff75ac65df9b1a96fc15
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723266"
---
# <a name="argcomplex-function"></a>ArgComplex 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지 [](https://nuget.org/packages/)


복소수 형식의 단계를 반환 합니다 `Complex` .

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a>입력

### <a name="input--complex"></a>입력: [복합](xref:Microsoft.Quantum.Math.Complex)

복소수 $c = x + i y $입니다.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)

단계 $ \text{Arg} [c] = \text{ArcTan} (y, x) \in (-\pi, \pi] $.