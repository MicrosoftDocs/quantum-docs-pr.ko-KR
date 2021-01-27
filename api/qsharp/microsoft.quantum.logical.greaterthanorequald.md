---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualD
title: GreaterThanOrEqualD 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualD
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 98fa55c249f2ade414254d1bccda46a8602b828c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815862"
---
# <a name="greaterthanorequald-function"></a>GreaterThanOrEqualD 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


숫자가 다른 숫자 보다 크거나 같은 경우에만 true를 반환 합니다.

```qsharp
function GreaterThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a>입력

### <a name="a--double"></a>a: [Double](xref:microsoft.quantum.lang-ref.double)

비교할 첫 번째 값입니다.


### <a name="b--double"></a>b: [Double](xref:microsoft.quantum.lang-ref.double)

비교할 두 번째 값입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`true``a`가 보다 크거나가와 같은 경우에만입니다 `b` .

## <a name="remarks"></a>설명

다음은 동일 합니다.

```qsharp
let cond = a >= b;
let cond = GreaterThanOrEqualD(a, b);
```