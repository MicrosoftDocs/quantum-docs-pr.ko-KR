---
uid: Microsoft.Quantum.Canon.RAll1
title: RAll1 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RAll1
qsharp.summary: >-
  Performs a phase shift operation.

  $R=\boldone-(1-e^{i \phi})\ket{1\cdots 1}\bra{1\cdots 1}$.
ms.openlocfilehash: f4159a6cc0e0b4f18f418a53a309b5ce527b2608
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852255"
---
# <a name="rall1-operation"></a>RAll1 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


단계 이동 작업을 수행 합니다.

$R = \boldone-(1-e ^ {i \phi}) \ket{1\cdots 1} \bra{1\cdots 1} $.

```qsharp
operation RAll1 (phase : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="phase--double"></a>단계: [Double](xref:microsoft.quantum.lang-ref.double)

$ \\\A$ 단계는 $ \ket{1\cdots 1} \bra{1\cdots 1} $ 상태에 적용 됩니다.


### <a name="qubits--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

$R $에서 해당 상태를 회전할 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

