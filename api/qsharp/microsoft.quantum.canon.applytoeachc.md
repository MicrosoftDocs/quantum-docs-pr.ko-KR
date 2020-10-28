---
uid: Microsoft.Quantum.Canon.ApplyToEachC
title: ApplyToEachC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachC
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: dfa18b6eb7a2c42fa2982994a2fc92170b52599c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717564"
---
# <a name="applytoeachc-operation"></a>ApplyToEachC 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


레지스터의 각 요소에 단일 수준 비트 작업을 적용 합니다.
한정자는 `C` 단일 비트 작업을 제어할 수 있음을 나타냅니다.

```qsharp
operation ApplyToEachC<'T> (singleElementOperation : ('T => Unit is Ctl), register : 'T[]) : Unit
```


## <a name="input"></a>입력

### <a name="singleelementoperation--t--unit-ctl"></a>singleElementOperation: ' ' => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl

각 고 비트에 적용할 연산입니다.


### <a name="register--t"></a>등록: ' t []

지정 된 작업을 적용할 대상 비트의 배열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

작업이 수행 되는 대상입니다.

## <a name="see-also"></a>참고 항목

- [각각의 Microsoft 양자](xref:Microsoft.Quantum.Canon.ApplyToEach)