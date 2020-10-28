---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterC
title: RestrictedToSubregisterC 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterC
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 2ca32cf8c85f33f498a30f71833b3dd69db6da6e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715513"
---
# <a name="restrictedtosubregisterc-function"></a>RestrictedToSubregisterC 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


작업을 레지스터의 인덱스 배열, 즉 subregister로 제한 합니다.
한정자는 `C` 작업을 제어할 수 있음을 나타냅니다.

```qsharp
function RestrictedToSubregisterC (op : (Qubit[] => Unit is Ctl), idxs : Int[]) : (Qubit[] => Unit is Ctl)
```


## <a name="input"></a>입력

### <a name="op--qubit--unit-ctl"></a>op:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl

Subregister로 제한 될 작업입니다.


### <a name="idxs--int"></a>idxs: [Int](xref:microsoft.quantum.lang-ref.int)[]

작업을 제한할 비트를 나타내는 인덱스의 배열입니다.



## <a name="output--qubit--unit-ctl"></a>출력:가 중 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl



## <a name="see-also"></a>참고 항목

- [RestrictedToSubregister입니다.](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)