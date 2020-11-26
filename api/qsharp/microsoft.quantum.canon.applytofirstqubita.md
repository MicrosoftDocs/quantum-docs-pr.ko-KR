---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitA
title: Applytofirst Bita 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitA
qsharp.summary: Applies an operation to the first qubit in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 4f0b209988c01076bdd0429d36d98c8060141618
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208842"
---
# <a name="applytofirstqubita-operation"></a>Applytofirst Bita 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


레지스터의 첫 번째 비트에 작업을 적용 합니다.
한정자는 `A` 작업이 adjointable를 나타냅니다.

```qsharp
operation ApplyToFirstQubitA (op : (Qubit => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a>입력

### <a name="op--qubit--unit--is-adj"></a>op: Adj [비트](xref:microsoft.quantum.lang-ref.qubit) => [단위](xref:microsoft.quantum.lang-ref.unit)

첫 번째 비트에 적용 되는 연산입니다.


### <a name="register--qubit"></a>register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

연산이 적용 되는 첫 번째 작업에 대 한 기본 비트 배열



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. Applytofirstbit](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)