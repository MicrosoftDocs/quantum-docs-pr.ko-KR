---
uid: Microsoft.Quantum.Canon.CControlled
title: CControlled 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlled
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens.
ms.openlocfilehash: 76e663e9a4b53c7ed74a1b70da516fb07958923b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216899"
---
# <a name="ccontrolled-function"></a>CControlled 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


작업 op가 지정 된 경우 기존 컨트롤 비트가 true 이면 op를 적용 하는 새 작업을 반환 합니다. 이면 `false` 아무 작업도 수행 되지 않습니다.

```qsharp
function CControlled<'T> (op : ('T => Unit)) : ((Bool, 'T) => Unit)
```


## <a name="input"></a>입력

### <a name="op--t--unit"></a>op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) 

조건부로 적용 될 작업입니다.



## <a name="output--boolt--unit"></a>출력: ([Bool](xref:microsoft.quantum.lang-ref.bool), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) 

클래식 컨트롤 비트가 true 인 경우 op 인 새 작업입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

조건부로 적용할 작업의 입력 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. CControlledC](xref:Microsoft.Quantum.Canon.CControlledC)
- [Microsoft. 양자. CControlledA](xref:Microsoft.Quantum.Canon.CControlledA)
- [CControlledCA입니다.](xref:Microsoft.Quantum.Canon.CControlledCA)