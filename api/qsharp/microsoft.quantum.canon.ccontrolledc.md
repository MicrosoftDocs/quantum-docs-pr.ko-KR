---
uid: Microsoft.Quantum.Canon.CControlledC
title: CControlledC 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledC
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: e5975455385e182236d7e2864e26ca00795a40c6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716577"
---
# <a name="ccontrolledc-function"></a>CControlledC 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


작업 op가 지정 된 경우 기존 컨트롤 비트가 true 이면 op를 적용 하는 새 작업을 반환 합니다. 이면 `false` 아무 작업도 수행 되지 않습니다.
한정자는 `C` 작업을 제어할 수 있음을 나타냅니다.

```qsharp
function CControlledC<'T> (op : ('T => Unit is Ctl)) : ((Bool, 'T) => Unit is Ctl)
```


## <a name="input"></a>입력

### <a name="op--t--unit-ctl"></a>op: ' t => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl

조건부로 적용 될 작업입니다.



## <a name="output--boolt--unit-ctl"></a>출력: ([Bool](xref:microsoft.quantum.lang-ref.bool), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl

클래식 컨트롤 비트가 true 인 경우 op 인 새 작업입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

조건부로 적용할 작업의 입력 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자 제어](xref:Microsoft.Quantum.Canon.CControlled)