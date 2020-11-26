---
uid: Microsoft.Quantum.Canon.ApplyIfA
title: ApplyIfA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfA
qsharp.summary: Applies a adjointable operation conditioned on a classical bit.
ms.openlocfilehash: d2880bbb95ebaf621ef9e5885051b94f32a3f1cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218770"
---
# <a name="applyifa-operation"></a>ApplyIfA 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


클래식 비트에 adjointable 작업 조건 화 된을 적용 합니다.

```qsharp
operation ApplyIfA<'T> (op : ('T => Unit is Adj), bit : Bool, target : 'T) : Unit is Adj
```


## <a name="description"></a>Description

작업 `op` 및 비트 값이 지정 된 `bit` `op` `target` 경우가 인 경우에 적용 됩니다 `bit` `true` . 이면이 `false` 발생 하지 않습니다 `target` .
접미사는 `A` 적용 될 작업이 adjointable을 나타냅니다.

## <a name="input"></a>입력

### <a name="op--t--unit--is-adj"></a>op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj

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