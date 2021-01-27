---
uid: Microsoft.Quantum.Canon.ApplyLowDepthAnd
title: ApplyLowDepthAnd 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyLowDepthAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, with T-depth 1, using measurement to perform the adjoint operation.
ms.openlocfilehash: 7fa9d9bf2f1905bf1b59e783d7bceb8cb2e09fa4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841700"
---
# <a name="applylowdepthand-operation"></a>ApplyLowDepthAnd 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 대상 값을 반전 합니다. 두 컨트롤이 모두 1 상태에 있는 경우에만 T-수준 1을 사용 하 여 adjoint 작업을 수행 합니다.

```qsharp
operation ApplyLowDepthAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>설명

`target`두 컨트롤이 모두 1 인 경우에만를 반전 하지만는 `target` 상태 0 이라고 가정 합니다.  작업은 T-수 4, T-깊이 1을 사용 하 고 하나의 도우미를 필요로 하며, 따라서 `target` 가 0으로 알려진 경우 CCNOT 연산에 더 적합할 수 있습니다.  이 작업의 adjoint는 측정을 기반으로 하며, T 게이트는 없으며 도우미를 사용 하지 않아도 됩니다.

## <a name="input"></a>입력

### <a name="control1--qubit"></a>control1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

첫 번째 제어 비트


### <a name="control2--qubit"></a>control2: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

두 번째 제어 비트


### <a name="target--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

대상 보조 비트 상태 0 이어야 합니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>참조

- Cody Jones: "내결함성 Toffoli 게이트 Novel 생성", Phys 87, 022328, 2013 [Arxiv: 1212.5069](https://arxiv.org/abs/1212.5069) doi: 10.1103/PhysRevA. 87.022328
- Peter Selinger: "T-depth one의 퀀텀 회로", Phys 87, 042302, 2013 [Arxiv: 1210.0974](https://arxiv.org/abs/1210.0974) doi: 10.1103/PhysRevA. 87.042302