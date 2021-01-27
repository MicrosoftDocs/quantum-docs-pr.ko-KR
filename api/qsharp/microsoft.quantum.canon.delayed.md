---
uid: Microsoft.Quantum.Canon.Delayed
title: 지연 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delayed
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 40fcc7d0a178fdb18437b4d6c96542db593347b4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840580"
---
# <a name="delayed-function"></a>지연 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 인수를 사용 하 여 지정 된 작업을 적용 하는 작업을 반환 합니다.

```qsharp
function Delayed<'T, 'U> (op : ('T => 'U), arg : 'T) : (Unit => 'U)
```


## <a name="input"></a>입력

### <a name="op--t--u"></a>op: ' t => ' U 

적용 될 작업입니다.


### <a name="arg--t"></a>인수: ' '

작업이 적용 되는 입력입니다.



## <a name="output--unit--u"></a>출력: [Unit](xref:microsoft.quantum.lang-ref.unit) => ' U 

입력에 적용 되는 새 작업입니다. `op``arg`

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

연기할 작업의 입력 형식입니다.
### <a name="u"></a>' U

연기할 작업의 반환 형식입니다.

## <a name="see-also"></a>참고 항목

- [DelayedC입니다.](xref:Microsoft.Quantum.Canon.DelayedC)
- [Microsoft 양자. DelayedA](xref:Microsoft.Quantum.Canon.DelayedA)
- [Microsoft 양자. DelayedCA](xref:Microsoft.Quantum.Canon.DelayedCA)
- [Microsoft. 양자 지연](xref:Microsoft.Quantum.Canon.Delay)