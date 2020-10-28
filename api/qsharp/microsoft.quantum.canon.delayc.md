---
uid: Microsoft.Quantum.Canon.DelayC
title: DelayC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayC
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: acb817c3322063353dc08c5d6f8c539391b3bf39
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716290"
---
# <a name="delayc-operation"></a>DelayC 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


지정 된 작업을 지연 시간에 적용 합니다.

```qsharp
operation DelayC<'T> (op : ('T => Unit is Ctl), arg : 'T, aux : Unit) : Unit
```


## <a name="description"></a>Description

작업 및 해당 작업에 대 한 입력이 주어진 경우 추가 입력이 제공 되 면에서 작업을 적용 합니다.
특히 식은 `Delay(op, arg, _)` `op` 호출 될 때에 적용 되는 연산입니다 `arg` .
식을 `Delay(op,arg,_)` 사용 하면의 응용 프로그램을 연기할 수 있습니다 `op` .

## <a name="input"></a>입력

### <a name="op--t--unit-ctl"></a>op: ' t => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl

적용 될 작업입니다.


### <a name="arg--t"></a>인수: ' '

작업이 적용 되는 입력입니다.


### <a name="aux--unit"></a>aux: [단위](xref:microsoft.quantum.lang-ref.unit)

부분 응용 프로그램을 사용 하 여 작업의 응용 프로그램을 지연 하는 데 사용 되는 인수입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

연기할 작업의 입력 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자 지연](xref:Microsoft.Quantum.Canon.Delay)
- [Microsoft. 양자. 지연](xref:Microsoft.Quantum.Canon.Delayed)