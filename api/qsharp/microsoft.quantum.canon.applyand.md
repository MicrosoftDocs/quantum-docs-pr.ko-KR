---
uid: Microsoft.Quantum.Canon.ApplyAnd
title: ApplyAnd 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, using measurement to perform the adjoint operation.
ms.openlocfilehash: b749013584c89273375da002ac36b3575085b7f2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219297"
---
# <a name="applyand-operation"></a>ApplyAnd 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


Adjoint 작업을 수행 하는 측정을 사용 하 여 두 컨트롤의가 모두 1 상태인 경우에만 지정 된 대상 값을 반전 합니다.

```qsharp
operation ApplyAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Description

`target`두 컨트롤이 모두 1 인 경우에만를 반전 하지만는 `target` 상태 0 이라고 가정 합니다.  작업은 T-카운트 4, T-깊이 2를 포함 하 고 도우미가 필요 하지 않습니다 `target` . 따라서가 0으로 알려진 경우에는 CCNOT 연산에 더 적합할 수 있습니다.  이 작업의 adjoint는 측정을 기반으로 하며 T 게이트가 필요 하지 않습니다.

이 작업을 제어 하는 응용 프로그램에는 도우미를 사용 하지 않아도 `2^c` `Rz` 되며 깊이에 최적화 되지 않습니다 `c` . 여기서은 작업의 두 컨트롤을 포함 하는 전체 컨트롤의 수입니다 `ApplyAnd` .  Adjoint 제어 응용 프로그램에는 `2^c - 1` `Rz` 게이트가 필요 하며,이는 비 adjoint 작업 크기의 각도가 두 배가 되 고, 도우미가 필요 하지 않으며, 깊이를 위해 최적화 되지 않습니다.

## <a name="input"></a>입력

### <a name="control1--qubit"></a>control1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

첫 번째 제어 비트


### <a name="control2--qubit"></a>control2: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

두 번째 제어 비트


### <a name="target--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

대상 보조 비트 상태 0 이어야 합니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>참조 항목

- Cody Jones: "내결함성 Toffoli 게이트 Novel 생성", Phys 87, 022328, 2013 [Arxiv: 1212.5069](https://arxiv.org/abs/1212.5069) doi: 10.1103/PhysRevA. 87.022328
- Craig Gidney: "나누어 the 퀀텀 추가 비용", 퀀텀 2, 페이지 74, 2018 [Arxiv: 1709.06648](https://arxiv.org/abs/1709.06648) doi: 10.1103/PhysRevA. 85.044302
- Mathias Soeken: "퀀텀 Oracle 회로 및 크리스마스 트리 패턴", [2019 년 12 월 19 일의 블로그 문서](https://msoeken.github.io/blog_qac.html) (참고: 여러 제어 된 생성에 대해 설명)