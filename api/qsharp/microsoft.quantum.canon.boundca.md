---
uid: Microsoft.Quantum.Canon.BoundCA
title: BoundCA 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundCA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `CA` indicates that all operations in the array are adjointable and controllable.
ms.openlocfilehash: 391183829a3cc8b7aa8051767dcfc6bec9638223
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844523"
---
# <a name="boundca-function"></a>BoundCA 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


단일 입력에 대해 작동 하는 작업 배열이 지정 된 경우 지정 된 각 작업을 순서 대로 수행 하는 새 작업을 생성 합니다.
한정자는 `CA` 배열의 모든 작업이 adjointable 및 제어 가능 함을 나타냅니다.

```qsharp
function BoundCA<'T> (operations : ('T => Unit is Adj + Ctl)[]) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a>입력

### <a name="operations--t--unit--is-adj--ctl"></a>작업: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl []

지정 된 입력에 대해 수행할 일련의 작업입니다.



## <a name="output--t--unit--is-adj--ctl"></a>출력: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

지정 된 각 작업을 입력에 대해 순서 대로 수행 하는 새 작업입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

배열의 각 작업이 작동 하는 대상입니다.

## <a name="example"></a>예

다음은 동일 합니다.

```qsharp
let bound = BoundCA([U, V]);
bound(x);
```

및

```qsharp
U(x); V(x);
```

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자.](xref:Microsoft.Quantum.Canon.Bound)