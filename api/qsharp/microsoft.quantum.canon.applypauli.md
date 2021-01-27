---
uid: Microsoft.Quantum.Canon.ApplyPauli
title: ApplyPauli 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauli
qsharp.summary: Given a multi-qubit Pauli operator, applies the corresponding operation to a register.
ms.openlocfilehash: b3557c6d8b5a90019f6d4cfa7b405475a3ab39fb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844748"
---
# <a name="applypauli-operation"></a>ApplyPauli 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


여러 기능을 제공 하는 경우 해당 작업을 레지스터에 적용 합니다.

```qsharp
operation ApplyPauli (pauli : Pauli[], target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="pauli--pauli"></a>pauli: [pauli](xref:microsoft.quantum.lang-ref.pauli)[]

단일 수준 비트 Pauli 연산자의 배열로 표현 되는 다중 기능 비트 Pauli 연산자입니다.


### <a name="target--qubit"></a>target: [](xref:microsoft.quantum.lang-ref.qubit)

등록 하 여 지정 된 Pauli 작업을 적용 합니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>예

다음은 동일 합니다.

```qsharp
ApplyPauli([PauliY, PauliZ, PauliX], target);
```

및

```qsharp
Y(target[0]);
Z(target[1]);
X(target[2]);
```