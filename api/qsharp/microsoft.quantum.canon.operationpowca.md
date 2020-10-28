---
uid: Microsoft.Quantum.Canon.OperationPowCA
title: OperationPowCA 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowCA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is controllable and adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 753063452616747309e3e228ce8a702f4378c61f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715674"
---
# <a name="operationpowca-function"></a>OperationPowCA 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


전원에 대 한 작업을 발생 시킵니다.
한정자는 `A` 작업을 제어 하 고 adjointable 나타냅니다.

즉, $ $U $를 나타내는 작업이 지정 된 경우 power $m $에 대해 ^ m $ $U 새 작업을 반환 합니다.

```qsharp
function OperationPowCA<'T> (op : ('T => Unit is Ctl + Adj), power : Int) : ('T => Unit is Ctl + Adj)
```


## <a name="input"></a>입력

### <a name="op--t--unit-ctl--adj"></a>op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj

반복 될 게이트를 나타내는 연산이 $U입니다.


### <a name="power--int"></a>power: [Int](xref:microsoft.quantum.lang-ref.int)

$U $가 반복 되는 횟수입니다.



## <a name="output--t--unit-ctl--adj"></a>출력: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj

^ M $ $U를 나타내는 새 작업입니다. 여기서 $m = \texttt{power} $입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

켤 작업의 형식입니다.

## <a name="see-also"></a>참고 항목

- [OperationPow입니다.](xref:Microsoft.Quantum.Canon.OperationPow)