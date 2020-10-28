---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: UncurriedOpC 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: f3e5ecf3f7df0393dfbb948f064c27505f04cfcf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715212"
---
# <a name="uncurriedopc-function"></a>UncurriedOpC 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


작업을 반환 하는 함수가 지정 된 경우 두 입력을 튜플로 받는 새 작업을 반환 합니다.
한정자는 `C` 작업을 제어할 수 있음을 나타냅니다.

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a>입력

### <a name="curriedop--t---u--unit-ctl"></a>curriedOp: ' t-> ' U => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl

작업을 반환 하는 함수입니다.



## <a name="output--tu--unit-ctl"></a>출력: (' t, ' U) => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl

에 해당 하는 새 작업입니다 `op` `op(t, u)` `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

커리 된 함수의 첫 번째 인수 형식입니다.
### <a name="u"></a>' U

커리 된 함수의 두 번째 인수 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. UncurriedOp](xref:Microsoft.Quantum.Canon.UncurriedOp)