---
uid: Microsoft.Quantum.Arithmetic.Carry
title: 작업 수행
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Carry
qsharp.summary: Implements a reversible carry gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.
ms.openlocfilehash: dfb08a9a9c805c0b611ab993c9b1eb949810a7da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843349"
---
# <a name="carry-operation"></a>작업 수행

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


해독 가능한 전달 게이트를 구현 합니다. 에서로 인코딩된 전달 비트 `carryIn` 와 및에서 인코딩된 두 개의 summand 비트가 지정 된 경우 `summand1` `summand2` ,는의 비트 xor를 계산 하 고,는이 비트의 비트 xor를 계산 `carryIn` `summand1` `summand2` `summand2` 합니다 `carryOut` .

```qsharp
operation Carry (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit, carryOut : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="carryin--qubit"></a>carryIn: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

운반 비트입니다.


### <a name="summand1--qubit"></a>summand1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

첫 번째 summand입니다.


### <a name="summand2--qubit"></a>summand2: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

두 번째 summand는 및의 합계에서 하위 비트를 대체 합니다 `summand1` `summand2` .


### <a name="carryout--qubit"></a>carryOut: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

수행 하는 것은 합계의 상위 비트를 사용 하 여 xored 됩니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

