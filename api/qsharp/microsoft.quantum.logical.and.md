---
uid: Microsoft.Quantum.Logical.And
title: And 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: 279221ed785dd76e28146e4c22e70290936bf529
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198574"
---
# <a name="and-function"></a>And 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


두 값의 부울 값을 반환 합니다.

```qsharp
function And (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>입력

### <a name="a--bool"></a>a: [Bool](xref:microsoft.quantum.lang-ref.bool)

고려해 야 할 첫 번째 값입니다.


### <a name="b--bool"></a>b: [Bool](xref:microsoft.quantum.lang-ref.bool)

고려할 두 번째 값입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`true``a`및 `b` 가 둘 다 인 경우에만 `true` 입니다.

## <a name="remarks"></a>설명

연산자와 달리 `and` 이 함수는 두 입력이 모두 완전히 계산 되도록 하는 짧은 회로는 아닙니다.

단기 동작으로, 다음은 동일 합니다.

```Q#
let x = a and b;
let x = And(a, b);
```