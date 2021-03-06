---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterC
title: RestrictedToSubregisterC 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterC
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: f44e9ea4d17dcadc6d3c64941529db819b7f9784
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840211"
---
# <a name="restrictedtosubregisterc-function"></a>RestrictedToSubregisterC 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


작업을 레지스터의 인덱스 배열, 즉 subregister로 제한 합니다.
한정자는 `C` 작업을 제어할 수 있음을 나타냅니다.

```qsharp
function RestrictedToSubregisterC (op : (Qubit[] => Unit is Ctl), idxs : Int[]) : (Qubit[] => Unit is Ctl)
```


## <a name="input"></a>입력

### <a name="op--qubit--unit--is-ctl"></a>op: [이상](xref:microsoft.quantum.lang-ref.qubit)[] => [단위가](xref:microsoft.quantum.lang-ref.unit)  Ctl입니다.

Subregister로 제한 될 작업입니다.


### <a name="idxs--int"></a>idxs: [Int](xref:microsoft.quantum.lang-ref.int)[]

작업을 제한할 비트를 나타내는 인덱스의 배열입니다.



## <a name="output--qubit--unit--is-ctl"></a>출력: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위가](xref:microsoft.quantum.lang-ref.unit)  Ctl입니다.



## <a name="see-also"></a>참고 항목

- [RestrictedToSubregister입니다.](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)