---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: UncurriedOpA 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: feb5da771ee6cb6a750fa76f9ffd8f5a3e0b5734
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840064"
---
# <a name="uncurriedopa-function"></a>UncurriedOpA 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


작업을 반환 하는 함수가 지정 된 경우 두 입력을 튜플로 받는 새 작업을 반환 합니다.
한정자는 `A` 작업이 adjointable 나타냅니다.

```qsharp
function UncurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj))) : (('T, 'U) => Unit is Adj)
```


## <a name="input"></a>입력

### <a name="curriedop--t---u--unit--is-adj"></a>curriedOp: ' t > ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj

작업을 반환 하는 함수입니다.



## <a name="output--tu--unit--is-adj"></a>출력: (' t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj

에 해당 하는 새 작업입니다 `op` `op(t, u)` `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

커리 된 함수의 첫 번째 인수 형식입니다.
### <a name="u"></a>' U

커리 된 함수의 두 번째 인수 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. UncurriedOp](xref:Microsoft.Quantum.Canon.UncurriedOp)