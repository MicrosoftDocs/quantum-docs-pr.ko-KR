---
uid: Microsoft.Quantum.Math.ArgComplexPolar
title: ArgComplexPolar 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplexPolar
qsharp.summary: Returns the phase of a complex number of type `ComplexPolar`.
ms.openlocfilehash: 5809b5463e6bf8ee73d095dfe4eafedfbb5e0702
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852909"
---
# <a name="argcomplexpolar-function"></a>ArgComplexPolar 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


복소수 형식의 단계를 반환 합니다 `ComplexPolar` .

```qsharp
function ArgComplexPolar (input : Microsoft.Quantum.Math.ComplexPolar) : Double
```


## <a name="input"></a>입력

### <a name="input--complexpolar"></a>입력: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)

복소수 $c = r e ^ {i t} $입니다.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)

$ \Text{Arg} [c] = t $ 단계입니다.