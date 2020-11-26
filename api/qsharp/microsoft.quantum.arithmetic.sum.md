---
uid: Microsoft.Quantum.Arithmetic.Sum
title: 합계(Sum) 연산
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Sum
qsharp.summary: Implements a reversible sum gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.
ms.openlocfilehash: 7758e29c9f08f4d05253defbe5a43a5316289522
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221796"
---
# <a name="sum-operation"></a>합계(Sum) 연산

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


해독 가능한 sum gate를 구현 합니다. 에서로 인코딩된 전달 비트 `carryIn` 와 및에서 인코딩된 두 개의 summand 비트가 지정 된 경우 `summand1` 는 `summand2` 의 비트 xor를 계산 합니다 `carryIn` `summand1` `summand2` `summand2` .

```qsharp
operation Sum (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="carryin--qubit"></a>carryIn: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

운반 비트입니다.


### <a name="summand1--qubit"></a>summand1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

첫 번째 summand입니다.


### <a name="summand2--qubit"></a>summand2: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

두 번째 summand는 및의 합계에서 하위 비트를 대체 합니다 `summand1` `summand2` .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

`Carry`작업과 달리이 작업은 실행 비트를 계산 하지 않습니다.