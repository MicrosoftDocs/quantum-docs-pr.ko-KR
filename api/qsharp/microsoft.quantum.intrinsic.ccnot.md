---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: CCNOT 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: a9186269a868c2ac9d2f15727a3b0ed1bfec3fa4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98819023"
---
# <a name="ccnot-operation"></a>CCNOT 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


3 가지 비트에 이중 제어 – (CCNOT) 게이트를 적용 합니다.

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="control1--qubit"></a>control1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

먼저 CCNOT gate의 비트를 제어 합니다.


### <a name="control2--qubit"></a>control2: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

CCNOT gate의 두 번째 제어 비트입니다.


### <a name="target--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

CCNOT gate의 대상입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

다음에 해당 합니다.

```qsharp
Controlled X([control1, control2], target);
```