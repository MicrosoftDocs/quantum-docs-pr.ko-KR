---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: SetToBasisState 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: dfa054360a5e82b7ae6ec5a6d52e7d5fe566f42e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854615"
---
# <a name="settobasisstate-operation"></a>SetToBasisState 작업

네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


필요에 따라 비트를 측정 하 고 비트 대칭을 적용 하 여 지정 된 계산 기준 상태로 원하는 비트를 설정 합니다.

```qsharp
operation SetToBasisState (desired : Result, target : Qubit) : Unit
```


## <a name="input"></a>입력

### <a name="desired--__invalidresult__"></a>desired: __유효 <Result> 하지 않음__

원하는 비트를 설정 해야 하는 기본 상태입니다.


### <a name="target--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

상태를 설정할의 비트입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

이 작업의 invariant로 직후를 호출 하면 `M(q)` `SetToBasisState(result, q)` 가 반환 됩니다 `result` .