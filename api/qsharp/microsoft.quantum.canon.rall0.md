---
uid: Microsoft.Quantum.Canon.RAll0
title: RAll0 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RAll0
qsharp.summary: >-
  Performs a phase shift operation.

  $R=\boldone-(1-e^{i \phi})\ket{0\cdots 0}\bra{0\cdots 0}$.
ms.openlocfilehash: 660e6633df6750747963d41a6ff28a4fd4b02d4e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840244"
---
# <a name="rall0-operation"></a>RAll0 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


단계 이동 작업을 수행 합니다.

$R = \boldone-(1-e ^ {i \phi}) \ket{0\cdots 0} \bra{0\cdots 0} $.

```qsharp
operation RAll0 (phase : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="phase--double"></a>단계: [Double](xref:microsoft.quantum.lang-ref.double)

$ \\\A$ 단계는 $ \ket{0\cdots 0} \bra{0\cdots 0} $ 상태에 적용 됩니다.


### <a name="qubits--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

$R $에서 해당 상태를 회전할 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [RAll1입니다.](xref:Microsoft.Quantum.Canon.RAll1)