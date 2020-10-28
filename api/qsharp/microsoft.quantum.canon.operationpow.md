---
uid: Microsoft.Quantum.Canon.OperationPow
title: OperationPow 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPow
qsharp.summary: >-
  Raises an operation to a power.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 5cf9017175f44a8a0b8f865624a6c312d25aded1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715772"
---
# <a name="operationpow-function"></a>OperationPow 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


전원에 대 한 작업을 발생 시킵니다.

즉, $ $U $를 나타내는 작업이 지정 된 경우 power $m $에 대해 ^ m $ $U 새 작업을 반환 합니다.

```qsharp
function OperationPow<'T> (op : ('T => Unit), power : Int) : ('T => Unit)
```


## <a name="input"></a>입력

### <a name="op--t--unit"></a>op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) 

반복 될 게이트를 나타내는 연산이 $U입니다.


### <a name="power--int"></a>power: [Int](xref:microsoft.quantum.lang-ref.int)

$U $가 반복 되는 횟수입니다.



## <a name="output--t--unit"></a>출력: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) 

^ M $ $U를 나타내는 새 작업입니다. 여기서 $m = \texttt{power} $입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

켤 작업의 형식입니다.

## <a name="see-also"></a>참고 항목

- [OperationPowC입니다.](xref:Microsoft.Quantum.Canon.OperationPowC)
- [OperationPowA입니다.](xref:Microsoft.Quantum.Canon.OperationPowA)
- [OperationPowCA입니다.](xref:Microsoft.Quantum.Canon.OperationPowCA)