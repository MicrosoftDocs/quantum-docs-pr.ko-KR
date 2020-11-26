---
uid: Microsoft.Quantum.Canon.BoundA
title: BoundA 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 3132bf198e98dd1a2b433f36b000060e7e721865
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216951"
---
# <a name="bounda-function"></a>BoundA 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


단일 입력에 대해 작동 하는 작업 배열이 지정 된 경우 지정 된 각 작업을 순서 대로 수행 하는 새 작업을 생성 합니다.
한정자는 `A` 배열의 모든 작업이 adjointable을 나타냅니다.

```qsharp
function BoundA<'T> (operations : ('T => Unit is Adj)[]) : ('T => Unit is Adj)
```


## <a name="input"></a>입력

### <a name="operations--t--unit--is-adj"></a>작업: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj []

지정 된 입력에 대해 수행할 일련의 작업입니다.



## <a name="output--t--unit--is-adj"></a>출력: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj

지정 된 각 작업을 입력에 대해 순서 대로 수행 하는 새 작업입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

배열의 각 작업이 작동 하는 대상입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자.](xref:Microsoft.Quantum.Canon.Bound)