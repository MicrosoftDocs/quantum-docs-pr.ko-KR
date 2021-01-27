---
uid: Microsoft.Quantum.Preparation.PrepareEntangledState
title: PrepareEntangledState 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareEntangledState
qsharp.summary: >-
  Pairwise entangles two qubit registers.

  That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.
ms.openlocfilehash: 9bf42131860b9fe9bd223ade32f95ec747abefe8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854374"
---
# <a name="prepareentangledstate-operation"></a>PrepareEntangledState 작업

네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


쌍 2 비트 레지스터입니다.

즉, 두 개의 레지스터가 지정 된 경우 {1} {2} 각 레지스터가 {00} {11} $ \ket{0\cdots 0} $ 상태에서 시작 되는 것으로 가정 하 여 각 레지스터의 각 \ket 쌍 사이에 최대 entangled 상태 $ \frac {\sqrt} \left (+ \ket \right) $를 준비 합니다.

```qsharp
operation PrepareEntangledState (left : Qubit[], right : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="left--qubit"></a>left: 좌 [bit](xref:microsoft.quantum.lang-ref.qubit)[]

$ \Ket{0\cdots 0} $ 상태의 고 비트 배열


### <a name="right--qubit"></a>right: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

$ \Ket{0\cdots 0} $ 상태의 고 비트 배열



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

