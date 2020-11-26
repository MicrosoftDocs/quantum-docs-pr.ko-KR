---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationC
title: ApplyWithInputTransformationC 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationC
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: 030c41d3ce0a5d613a95c6511f7278497ec5cda1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217172"
---
# <a name="applywithinputtransformationc-operation"></a>ApplyWithInputTransformationC 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


일부 입력을 허용 하는 작업, 해당 작업과 호환 되는 출력을 반환 하는 함수 및이 함수에 대 한 입력을 제공 하는 경우 함수를 사용 하 여 작업에 필요한 형식으로 입력을 변환 하는 작업을 적용 합니다.

```qsharp
operation ApplyWithInputTransformationC<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Ctl), input : 'U) : Unit is Ctl
```


## <a name="input"></a>입력

### <a name="fn--u---t"></a>fn: ' U-> '

지정 된 입력을 작업에서 예상 하는 형식으로 변환 하는 함수입니다.


### <a name="op--t--unit--is-ctl"></a>op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.

적용 될 작업입니다.


### <a name="input--u"></a>입력: ' U

함수에 대 한 입력입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다


### <a name="u"></a>' U



## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyWithInputTransformation](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [ApplyWithInputTransformationA입니다.](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [ApplyWithInputTransformationCA입니다.](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [TransformedOperation입니다.](xref:Microsoft.Quantum.Canon.TransformedOperation)