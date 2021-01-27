---
uid: Microsoft.Quantum.Canon.ConjugatedBy
title: ConjugatedBy 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedBy
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: c11e6b2cc97e682bf4fe266997f60ce69e87ba96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840869"
---
# <a name="conjugatedby-function"></a>ConjugatedBy 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


외부 및 내부 연산을 지정 하면는 외부 작업에 의해 내부 작업을 변화 시키고 하는 새 작업을 반환 합니다.

```qsharp
function ConjugatedBy<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit)) : ('T => Unit)
```


## <a name="input"></a>입력

### <a name="outeroperation--t--unit--is-adj"></a>outerOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj

$U $는 켤레 $V $로 사용 해야 합니다. 외부 작업 $U $은 (는) adjointable 해야 하지만 제어할 필요가 없습니다.


### <a name="inneroperation--t--unit"></a>innerOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) 

작업 $V $가 conjugated입니다.



## <a name="output--t--unit"></a>출력: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) 

해당 작업이 단일 $U ^ {\dagger} V U $로 표시 되는 새 작업입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

각 내부 및 외부 작업이 작동 하는 대상의 형식입니다.

## <a name="remarks"></a>설명

외부 작업은 항상 adjointable으로 간주 되지만 결합 된 작업을 제어 하기 위해 제어 하지 않아도 됩니다.

## <a name="see-also"></a>참고 항목

- [ConjugatedByA입니다.](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [ConjugatedByC입니다.](xref:Microsoft.Quantum.Canon.ConjugatedByC)
- [ConjugatedByCA입니다.](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [Microsoft. 양자.](xref:Microsoft.Quantum.Canon.ApplyWith)