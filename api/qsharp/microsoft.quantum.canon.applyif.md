---
uid: Microsoft.Quantum.Canon.ApplyIf
title: ApplyIf 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIf
qsharp.summary: Applies an operation conditioned on a classical bit.
ms.openlocfilehash: c5a1012328fa012ee02707aa59c94ac9c44b8e87
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218838"
---
# <a name="applyif-operation"></a>ApplyIf 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


클래식 비트에 조건 화 된 작업을 적용 합니다.

```qsharp
operation ApplyIf<'T> (op : ('T => Unit), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a>Description

작업 `op` 및 비트 값이 지정 된 `bit` `op` `target` 경우가 인 경우에 적용 됩니다 `bit` `true` . 이면이 `false` 발생 하지 않습니다 `target` .

## <a name="input"></a>입력

### <a name="op--t--unit"></a>op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) 

조건부로 적용 될 작업입니다.


### <a name="bit--bool"></a>bit: [Bool](xref:microsoft.quantum.lang-ref.bool)

op가 적용 되는지 여부를 제어 하는 부울입니다.


### <a name="target--t"></a>대상: ' '

작업이 적용 되는 입력입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

조건부로 적용할 작업의 입력 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyIfC](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [Microsoft. 양자. ApplyIfA](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [Microsoft 양자. ApplyIfCA](xref:Microsoft.Quantum.Canon.ApplyIfCA)