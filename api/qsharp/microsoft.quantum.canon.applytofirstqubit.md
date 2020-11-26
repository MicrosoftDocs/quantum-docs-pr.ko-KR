---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubit
title: Applytofirst의 비트 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubit
qsharp.summary: Applies an operation to the first qubit in the register.
ms.openlocfilehash: 851f2b58a914c8b09188f442e442b91a8ede5416
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217495"
---
# <a name="applytofirstqubit-operation"></a>Applytofirst의 비트 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


레지스터의 첫 번째 비트에 작업을 적용 합니다.

```qsharp
operation ApplyToFirstQubit (op : (Qubit => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a>입력

### <a name="op--qubit--unit"></a>op:의 [비트](xref:microsoft.quantum.lang-ref.qubit) => [단위](xref:microsoft.quantum.lang-ref.unit) 

첫 번째 비트에 적용 되는 연산입니다.


### <a name="register--qubit"></a>register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

연산이 적용 되는 첫 번째 작업에 대 한 기본 비트 배열



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyToFirstQubitA](xref:Microsoft.Quantum.Canon.ApplyToFirstQubitA)
- [Microsoft. 양자. ApplyToFirstQubitC](xref:Microsoft.Quantum.Canon.ApplyToFirstQubitC)
- [Microsoft. 양자. ApplyToFirstQubitCA](xref:Microsoft.Quantum.Canon.ApplyToFirstQubitCA)