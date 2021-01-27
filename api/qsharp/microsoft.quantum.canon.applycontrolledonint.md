---
uid: Microsoft.Quantum.Canon.ApplyControlledOnInt
title: ApplyControlledOnInt 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnInt
qsharp.summary: Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 499a25104742b2d03886065baad4d535ea92e83b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845111"
---
# <a name="applycontrolledonint-operation"></a>ApplyControlledOnInt 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


컨트롤 레지스터 상태가 지정 된 양의 정수에 해당 하는 경우 대상 레지스터에 단일 작업을 적용 합니다.

```qsharp
operation ApplyControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="numberstate--int"></a>번호 상태: [Int](xref:microsoft.quantum.lang-ref.int)

작업을 제어 해야 하는 음수가 아닌 정수 `oracle` 입니다.


### <a name="oracle--t--unit--is-adj--ctl"></a>oracle: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

제어할 단일 작업입니다.


### <a name="controlregister--qubit"></a>controlRegister: [bit](xref:microsoft.quantum.lang-ref.qubit)[]

의 응용 프로그램을 제어 하는 퀀텀 레지스터입니다 `oracle` .


### <a name="targetregister--t"></a>targetRegister: ' t

적용할 레지스터 `oracle` 입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="remarks"></a>설명

의 값은 `numberState` 작은 endian 인코딩을 사용 하 여 해석 됩니다.

`numberState` 최대 $2 ^ \texttt{Length (controlRegister)}-$1 여야 합니다.
예를 들어는 `numberState = 537` `oracle` `controlRegister` 가 $ \ket $ 상태에 있는 경우에만이 적용 됨을 의미 합니다 {537} .