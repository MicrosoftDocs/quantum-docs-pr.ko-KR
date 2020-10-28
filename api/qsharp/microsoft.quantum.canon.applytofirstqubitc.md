---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitC
title: Applytofirst Bitc 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitC
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: e2c137ad4a8252731acf94d6f2343f8fd386b8e3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717410"
---
# <a name="applytofirstqubitc-operation"></a>Applytofirst Bitc 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


레지스터의 첫 번째 비트에 작업 op를 적용 합니다.
한정자는 `C` 작업을 제어할 수 있음을 나타냅니다.

```qsharp
operation ApplyToFirstQubitC (op : (Qubit => Unit is Ctl), register : Qubit[]) : Unit
```


## <a name="input"></a>입력

### <a name="op--qubit--unit-ctl"></a>op: 이상 [비트](xref:microsoft.quantum.lang-ref.qubit) => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl

첫 번째 비트에 적용 되는 연산입니다.


### <a name="register--qubit"></a>register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

연산이 적용 되는 첫 번째 작업에 대 한 기본 비트 배열



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. Applytofirstbit](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)