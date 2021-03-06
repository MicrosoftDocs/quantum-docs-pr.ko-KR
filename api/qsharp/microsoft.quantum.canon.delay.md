---
uid: Microsoft.Quantum.Canon.Delay
title: 지연 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delay
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: c8ba128e44a9b217ec196e39ff1df639ef276784
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840651"
---
# <a name="delay-operation"></a>지연 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 작업을 지연 시간에 적용 합니다.

```qsharp
operation Delay<'T, 'U> (op : ('T => 'U), arg : 'T, aux : Unit) : 'U
```


## <a name="description"></a>설명

작업 및 해당 작업에 대 한 입력이 주어진 경우 추가 입력이 제공 되 면에서 작업을 적용 합니다.
특히 식은 `Delay(op, arg, _)` `op` 호출 될 때에 적용 되는 연산입니다 `arg` .
식을 `Delay(op,arg,_)` 사용 하면의 응용 프로그램을 연기할 수 있습니다 `op` .

## <a name="input"></a>입력

### <a name="op--t--u"></a>op: ' t => ' U 

적용 될 작업입니다.


### <a name="arg--t"></a>인수: ' '

작업이 적용 되는 입력입니다.


### <a name="aux--unit"></a>aux: [단위](xref:microsoft.quantum.lang-ref.unit)

부분 응용 프로그램을 사용 하 여 작업의 응용 프로그램을 지연 하는 데 사용 되는 인수입니다.



## <a name="output--u"></a>출력: ' U



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

연기할 작업의 입력 형식입니다.
### <a name="u"></a>' U

연기할 작업의 반환 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft 양자. DelayC](xref:Microsoft.Quantum.Canon.DelayC)
- [DelayA입니다.](xref:Microsoft.Quantum.Canon.DelayA)
- [Microsoft 양자.](xref:Microsoft.Quantum.Canon.DelayCA)
- [Microsoft. 양자. 지연](xref:Microsoft.Quantum.Canon.Delayed)