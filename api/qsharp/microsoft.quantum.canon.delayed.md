---
uid: Microsoft.Quantum.Canon.Delayed
title: 지연 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delayed
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 820a38c2b4de2e0151d55bd88fb4f69567182f6b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716255"
---
# <a name="delayed-function"></a>지연 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


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