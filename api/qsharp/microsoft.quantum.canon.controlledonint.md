---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: ControlledOnInt 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 3cc5c00d9c7295106901149e06571ef1963d1323
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207261"
---
# <a name="controlledonint-function"></a>ControlledOnInt 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


컨트롤 레지스터 상태가 지정 된 양의 정수에 해당 하는 경우 대상 레지스터에 oracle을 적용 하는 단일 연산자를 반환 합니다.

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a>입력

### <a name="numberstate--int"></a>번호 상태: [Int](xref:microsoft.quantum.lang-ref.int)

양의 정수입니다.


### <a name="oracle--t--unit--is-adj--ctl"></a>oracle: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

단일 연산자.



## <a name="output--qubitt--unit--is-adj--ctl"></a>출력[: (Adj](xref:microsoft.quantum.lang-ref.qubit)+ [], ' t) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl + Ctl

`oracle`컨트롤 레지스터 상태가 숫자 상태에 해당 하는 경우 대상 레지스터에 적용 되는 단일 연산자입니다 `numberState` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="remarks"></a>설명

의 값은 `numberState` 작은 endian 인코딩을 사용 하 여 해석 됩니다.