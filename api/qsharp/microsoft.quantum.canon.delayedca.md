---
uid: Microsoft.Quantum.Canon.DelayedCA
title: DelayedCA 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedCA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: c44e3448c471f2a20f995d4546ee54f3affb726e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840541"
---
# <a name="delayedca-function"></a>DelayedCA 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 인수를 사용 하 여 지정 된 작업을 적용 하는 작업을 반환 합니다.

```qsharp
function DelayedCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T) : (Unit => Unit is Ctl + Adj)
```


## <a name="input"></a>입력

### <a name="op--t--unit--is-adj--ctl"></a>op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

반환 값을 적용 한 결과로 적용 되는 작업입니다.


### <a name="arg--t"></a>인수: ' '

작업이 `op` 적용 되는 입력입니다.



## <a name="output--unit--unit--is-adj--ctl"></a>출력: [unit](xref:microsoft.quantum.lang-ref.unit) => [unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

입력에 적용 되는 새 작업입니다. `op``arg`

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

연기할 작업의 입력 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. 지연](xref:Microsoft.Quantum.Canon.Delayed)
- [Microsoft. 양자 지연](xref:Microsoft.Quantum.Canon.Delay)