---
uid: Microsoft.Quantum.Diagnostics._prepareEntangledState
title: _prepareEntangledState 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _prepareEntangledState
qsharp.summary: >-
  Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers. All qubits must start in the |0⟩ state.

  The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.
ms.openlocfilehash: 5a74978a536a92dafae0b532805bd8e8ae1c888e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830981"
---
# <a name="_prepareentangledstate-operation"></a>_prepareEntangledState 작업

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


두 개의 레지스터가 지정 된 경우는 각 레지스터의 각 비트 쌍 간에 최대 entangled 상태를 준비 합니다.
모든 비트는 | 0 ⟩ 상태에서 시작 해야 합니다.

결과적으로 각 레지스터의 해당 \bra{\ 쌍은 $ beta_ {00} } \ket{\ beta_ {00} } $에 있습니다.

```qsharp
operation _prepareEntangledState (left : Qubit[], right : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="left--qubit"></a>left: 좌 [bit](xref:microsoft.quantum.lang-ref.qubit)[]

$ \Ket{0\cdots 0} $ 상태의 고 비트 배열


### <a name="right--qubit"></a>right: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

$ \Ket{0\cdots 0} $ 상태의 고 비트 배열



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

