---
uid: Microsoft.Quantum.Canon.OperationPowC
title: OperationPowC 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowC
qsharp.summary: >-
  Raises an operation to a power. The modifier `C` indicates that the operation is controllable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: f3c51410fb7c091385b64a1c4c99b3972d5055b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715688"
---
# <a name="operationpowc-function"></a>OperationPowC 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


전원에 대 한 작업을 발생 시킵니다.
한정자는 `C` 작업을 제어할 수 있음을 나타냅니다.

즉, $ $U $를 나타내는 작업이 지정 된 경우 power $m $에 대해 ^ m $ $U 새 작업을 반환 합니다.

```qsharp
function OperationPowC<'T> (op : ('T => Unit is Ctl), power : Int) : ('T => Unit is Ctl)
```


## <a name="input"></a>입력

### <a name="op--t--unit-ctl"></a>op: ' t => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl

반복 될 게이트를 나타내는 연산이 $U입니다.


### <a name="power--int"></a>power: [Int](xref:microsoft.quantum.lang-ref.int)

$U $가 반복 되는 횟수입니다.



## <a name="output--t--unit-ctl"></a>출력: ' t => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl

^ M $ $U를 나타내는 새 작업입니다. 여기서 $m = \texttt{power} $입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

켤 작업의 형식입니다.

## <a name="see-also"></a>참고 항목

- [OperationPow입니다.](xref:Microsoft.Quantum.Canon.OperationPow)