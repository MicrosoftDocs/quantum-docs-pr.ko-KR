---
uid: Microsoft.Quantum.Canon.ApplyPauli
title: ApplyPauli 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauli
qsharp.summary: Given a multi-qubit Pauli operator, applies the corresponding operation to a register.
ms.openlocfilehash: ccf8e1b3dbe5d4cd916a581aeab190ab0cff2021
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717816"
---
# <a name="applypauli-operation"></a>ApplyPauli 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


여러 기능을 제공 하는 경우 해당 작업을 레지스터에 적용 합니다.

```qsharp
operation ApplyPauli (pauli : Pauli[], target : Qubit[]) : Unit
```


## <a name="input"></a>입력

### <a name="pauli--pauli"></a>pauli: [pauli](xref:microsoft.quantum.lang-ref.pauli)[]

단일 수준 비트 Pauli 연산자의 배열로 표현 되는 다중 기능 비트 Pauli 연산자입니다.


### <a name="target--qubit"></a>target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

등록 하 여 지정 된 Pauli 작업을 적용 합니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

