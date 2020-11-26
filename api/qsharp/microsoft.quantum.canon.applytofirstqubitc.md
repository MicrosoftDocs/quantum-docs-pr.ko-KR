---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitC
title: Applytofirst Bitc 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitC
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 2659c3a97baa68cb4c1d7781381f89742902594d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217512"
---
# <a name="applytofirstqubitc-operation"></a>Applytofirst Bitc 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


레지스터의 첫 번째 비트에 작업 op를 적용 합니다.
한정자는 `C` 작업을 제어할 수 있음을 나타냅니다.

```qsharp
operation ApplyToFirstQubitC (op : (Qubit => Unit is Ctl), register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a>입력

### <a name="op--qubit--unit--is-ctl"></a>op: 고 [비트](xref:microsoft.quantum.lang-ref.qubit) => [단위가](xref:microsoft.quantum.lang-ref.unit)  Ctl입니다.

첫 번째 비트에 적용 되는 연산입니다.


### <a name="register--qubit"></a>register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

연산이 적용 되는 첫 번째 작업에 대 한 기본 비트 배열



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. Applytofirstbit](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)