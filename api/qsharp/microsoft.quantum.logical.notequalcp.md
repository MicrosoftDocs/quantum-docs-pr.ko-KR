---
uid: Microsoft.Quantum.Logical.NotEqualCP
title: NotEqualCP 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualCP
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 85225109a3822a9b63a231631f3d7265143418b6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814410"
---
# <a name="notequalcp-function"></a>NotEqualCP 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


두 입력이 같지 않은 경우에만 true를 반환 합니다.

```qsharp
function NotEqualCP (a : Microsoft.Quantum.Math.ComplexPolar, b : Microsoft.Quantum.Math.ComplexPolar) : Bool
```


## <a name="input"></a>입력

### <a name="a--complexpolar"></a>a: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)

비교할 첫 번째 값입니다.


### <a name="b--complexpolar"></a>b: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)

비교할 두 번째 값입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`true``a`가와 같지 않은 경우에만입니다 `b` .