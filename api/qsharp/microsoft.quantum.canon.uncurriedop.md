---
uid: Microsoft.Quantum.Canon.UncurriedOp
title: UncurriedOp 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOp
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple.
ms.openlocfilehash: d707b52bb17f4dea795fa4ff824c785e506b8b20
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852001"
---
# <a name="uncurriedop-function"></a>UncurriedOp 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


작업을 반환 하는 함수가 지정 된 경우 두 입력을 튜플로 받는 새 작업을 반환 합니다.

```qsharp
function UncurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit))) : (('T, 'U) => Unit)
```


## <a name="input"></a>입력

### <a name="curriedop--t---u--unit"></a>curriedOp: ' t-> ' U => [단위](xref:microsoft.quantum.lang-ref.unit) 

작업을 반환 하는 함수입니다.



## <a name="output--tu--unit"></a>출력: (' t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit) 

에 해당 하는 새 작업입니다 `op` `op(t, u)` `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

변환 작업에 대 한 첫 번째 입력의 형식입니다.
### <a name="u"></a>' U

커리 된 작업에 대 한 두 번째 입력의 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. UncurriedOpC](xref:Microsoft.Quantum.Canon.UncurriedOpC)
- [Microsoft. 양자. UncurriedOpA](xref:Microsoft.Quantum.Canon.UncurriedOpA)
- [Microsoft. 양자. UncurriedOpCA](xref:Microsoft.Quantum.Canon.UncurriedOpCA)