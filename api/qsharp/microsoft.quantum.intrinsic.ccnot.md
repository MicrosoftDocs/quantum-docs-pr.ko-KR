---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: CCNOT 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: bf20ff1e9d25d72e7e8e0207ab947a57dc394cf4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711537"
---
# <a name="ccnot-operation"></a>CCNOT 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)

패키지 [](https://nuget.org/packages/)


3 가지 비트에 이중 제어 – (CCNOT) 게이트를 적용 합니다.

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
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