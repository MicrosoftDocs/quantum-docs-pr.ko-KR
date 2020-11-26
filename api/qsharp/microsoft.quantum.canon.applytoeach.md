---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: 각 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: 11f9363feb38676df3f805496c74036aa96160c1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217869"
---
# <a name="applytoeach-operation"></a>각 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


레지스터의 각 요소에 단일 수준 비트 작업을 적용 합니다.

```qsharp
operation ApplyToEach<'T> (singleElementOperation : ('T => Unit), register : 'T[]) : Unit
```


## <a name="input"></a>입력

### <a name="singleelementoperation--t--unit"></a>singleElementOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) 

각 고 비트에 적용할 연산입니다.


### <a name="register--t"></a>등록: ' t []

지정 된 작업을 적용할 대상 비트의 배열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

작업이 수행 되는 대상입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyToEachC](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [ApplyToEachA입니다.](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [Microsoft. 양자. ApplyToEachCA](xref:Microsoft.Quantum.Canon.ApplyToEachCA)