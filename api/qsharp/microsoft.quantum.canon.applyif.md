---
uid: Microsoft.Quantum.Canon.ApplyIf
title: ApplyIf 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIf
qsharp.summary: Applies an operation conditioned on a classical bit.
ms.openlocfilehash: 109a5c4748d183f199e420b4b1aef687613d220c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841882"
---
# <a name="applyif-operation"></a>ApplyIf 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


클래식 비트에 조건 화 된 작업을 적용 합니다.

```qsharp
operation ApplyIf<'T> (op : ('T => Unit), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a>설명

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

## <a name="example"></a>예

다음은 값의 배열로 지정 된 기존 비트 문자열로 표현 되는 계산 기준 상태로 값의 레지스터를 준비 합니다 `Bool` .

```qsharp
let bitstring = [true, false, true];
using (register = Qubit(3)) {
    ApplyToEach(ApplyIf(X, _, _), Zipped(bitstring, register));
    // register should now be in the state |101⟩.
    ...
}
```

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyIfC](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [Microsoft. 양자. ApplyIfA](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [Microsoft 양자. ApplyIfCA](xref:Microsoft.Quantum.Canon.ApplyIfCA)