---
uid: Microsoft.Quantum.Canon.ApplyWith
title: ApplyWith 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWith
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: fd46f84e30e72672967b90d92f507d2a5c438dba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217308"
---
# <a name="applywith-operation"></a>ApplyWith 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


두 작업을 수행 하는 경우 conjugated로 다른 작업을 적용 합니다.

```qsharp
operation ApplyWith<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit), target : 'T) : Unit
```


## <a name="description"></a>Description

$U $ 및 $V $와 같은 단일 연산자에 의해 각각 설명 된 두 개의 작업은 ^ {\dagger} V U $ $U 시퀀스에 적용 됩니다. 즉,이 작업은 $U $와 $V $ conjugated에서 제공 하는 단일 연산자를 구현 합니다.

## <a name="input"></a>입력

### <a name="outeroperation--t--unit--is-adj"></a>outerOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj

$U $는 켤레 $V $로 사용 해야 합니다. 외부 작업 $U $은 (는) adjointable 해야 하지만 제어할 필요가 없습니다.


### <a name="inneroperation--t--unit"></a>innerOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) 

작업 $V $가 conjugated입니다.


### <a name="target--t"></a>대상: ' '

외부 및 내부 작업에 제공 되는 입력입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

각 내부 및 외부 작업이 작동 하는 대상입니다.

## <a name="remarks"></a>설명

외부 작업은 항상 adjointable으로 간주 되지만 결합 된 작업을 제어 하기 위해 제어 하지 않아도 됩니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyWithA](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [Microsoft. 양자. ApplyWithC](xref:Microsoft.Quantum.Canon.ApplyWithC)
- [Microsoft 양자. ApplyWithCA](xref:Microsoft.Quantum.Canon.ApplyWithCA)