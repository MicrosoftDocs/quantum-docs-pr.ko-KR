---
uid: Microsoft.Quantum.Canon.RestrictedToSubregister
title: RestrictedToSubregister 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregister
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister.
ms.openlocfilehash: c5a6bbe16d2f6a317f6ed6f258077095465995f9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840222"
---
# <a name="restrictedtosubregister-function"></a>RestrictedToSubregister 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


작업을 레지스터의 인덱스 배열, 즉 subregister로 제한 합니다.

```qsharp
function RestrictedToSubregister (op : (Qubit[] => Unit), idxs : Int[]) : (Qubit[] => Unit)
```


## <a name="input"></a>입력

### <a name="op--qubit--unit"></a>op:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit) 

Subregister로 제한 될 작업입니다.


### <a name="idxs--int"></a>idxs: [Int](xref:microsoft.quantum.lang-ref.int)[]

작업을 제한할 비트를 나타내는 인덱스의 배열입니다.



## <a name="output--qubit--unit"></a>출력:가 중 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit) 



## <a name="see-also"></a>참고 항목

- [RestrictedToSubregisterA입니다.](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterA)
- [RestrictedToSubregisterC입니다.](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterC)
- [RestrictedToSubregisterCA입니다.](xref:Microsoft.Quantum.Canon.RestrictedToSubregisterCA)