---
uid: Microsoft.Quantum.Logical.Or
title: Or 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Or
qsharp.summary: Returns the Boolean disjunction of two values.
ms.openlocfilehash: 4a29b7684b28b904b43ccceb8e63280999690349
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848475"
---
# <a name="or-function"></a>Or 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


두 값의 부울 분리를 반환 합니다.

```qsharp
function Or (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>입력

### <a name="a--bool"></a>a: [Bool](xref:microsoft.quantum.lang-ref.bool)

고려해 야 할 첫 번째 값입니다.


### <a name="b--bool"></a>b: [Bool](xref:microsoft.quantum.lang-ref.bool)

고려할 두 번째 값입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`true``a`또는가 인 경우에만 `b` `true` 입니다.

## <a name="remarks"></a>설명

연산자와 달리 `or` 이 함수는 두 입력이 모두 완전히 계산 되도록 하는 짧은 회로는 아닙니다.

단기 동작으로, 다음은 동일 합니다.

```qsharp
let x = a or b;
let x = Or(a, b);
```