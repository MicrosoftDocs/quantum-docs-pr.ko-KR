---
uid: Microsoft.Quantum.Math.AbsComplex
title: AbsComplex 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: AbsComplex
qsharp.summary: Returns the absolute value of a complex number of type `Complex`.
ms.openlocfilehash: d47e04616d4bcf49273bec31fc22990a8244962b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723889"
---
# <a name="abscomplex-function"></a>AbsComplex 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지 [](https://nuget.org/packages/)


형식의 복소수의 절대값을 반환 합니다 `Complex` .

```qsharp
function AbsComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a>입력

### <a name="input--complex"></a>입력: [복합](xref:Microsoft.Quantum.Math.Complex)

복소수 $c = x + i y $입니다.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)

절대값 $ | c | = \sqrt{x ^ 2 + y ^ 2} $.