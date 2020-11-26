---
uid: Microsoft.Quantum.Canon.ApplyIfOneA
title: ApplyIfOneA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being one.
ms.openlocfilehash: 200908f2958b74e4823c891ef901474d75d18336
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218549"
---
# <a name="applyifonea-operation"></a>ApplyIfOneA 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


기존 결과 값이 1 인 조건 화 된 adjointable 작업을 적용 합니다.

```qsharp
operation ApplyIfOneA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit is Adj
```


## <a name="description"></a>Description

작업 `op` 및 결과 값이 지정 된 `result` `op` `target` 경우이 인 경우에 적용 됩니다 `result` `One` . 이면이 `Zero` 발생 하지 않습니다 `target` .
접미사는 `A` 적용 될 작업이 adjointable을 나타냅니다.

## <a name="input"></a>입력

### <a name="result--__invalidresult__"></a>결과: __잘못 <Result> 됨__

Op가 적용 되는지 여부를 제어 하는 측정 결과입니다.


### <a name="op--t--unit--is-adj"></a>op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj

조건부로 적용 될 작업입니다.


### <a name="target--t"></a>대상: ' '

작업이 적용 되는 입력입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

조건부로 적용할 작업의 입력 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyIfOneC](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [Microsoft. 양자. ApplyIfOneA](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [ApplyIfOneCA입니다.](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)