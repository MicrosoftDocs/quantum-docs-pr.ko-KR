---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterCA
title: RestrictedToSubregisterCA 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterCA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 9b1c8a6d1c843fb0533af16aafc4b3ca2ba2f0e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852182"
---
# <a name="restrictedtosubregisterca-function"></a>RestrictedToSubregisterCA 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


작업을 레지스터의 인덱스 배열, 즉 subregister로 제한 합니다.
한정자는 `CA` 작업을 제어 하 고 adjointable 나타냅니다.

```qsharp
function RestrictedToSubregisterCA (op : (Qubit[] => Unit is Adj + Ctl), idxs : Int[]) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>입력

### <a name="op--qubit--unit--is-adj--ctl"></a>op: [이상](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Adj + Ctl입니다.

Subregister로 제한 될 작업입니다.


### <a name="idxs--int"></a>idxs: [Int](xref:microsoft.quantum.lang-ref.int)[]

작업을 제한할 비트를 나타내는 인덱스의 배열입니다.



## <a name="output--qubit--unit--is-adj--ctl"></a>출력:가 중 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Adj + Ctl입니다.



## <a name="see-also"></a>참고 항목

- [RestrictedToSubregister입니다.](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)