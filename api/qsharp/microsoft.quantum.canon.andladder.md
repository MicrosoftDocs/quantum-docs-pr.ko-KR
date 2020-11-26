---
uid: Microsoft.Quantum.Canon.AndLadder
title: AndLadder 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: AndLadder
qsharp.summary: Performs a controlled "AND ladder" on a register of target qubits.
ms.openlocfilehash: 2c6114ec8a5caabdeea8ab7e26a4877e1633671c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209726"
---
# <a name="andladder-operation"></a>AndLadder 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


대상의 레지스터에서 제어 되는 "및 사다리"를 수행 합니다.

```qsharp
operation AndLadder (ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit is Adj
```


## <a name="description"></a>Description

이 작업은 계산 기준, $ $ \begin{align} \ket{x \_ 1, \dots, x \_ n} \ket{y \_ 1, \dots, y \_ {n-1}} \maps\ket{x \_ 1, \dots, x \_ n} \ket{y \_ 1 \oplus (x 1 \stx 2), \sti의 매핑에 의해 설명 된 변환을 적용 합니다. \_ \_ y \_ {n-1} \oplus (x \_ 1 \stx \_ 2 \st\cststomx \_ {n-1}}, \end{align} $ $ where $ \ket{x \_ 1, \dots, x \_ n} $는의 계산 기준 상태를 나타내며 `controls` , 여기서 $ \ket{y \_ 1, \dots, y \_ {n-1}} $는의 계산 기준 상태를 나타냅니다 `targets` .

## <a name="input"></a>입력

### <a name="ccnot--ccnotop"></a>ccnot: [Ccnotop](xref:Microsoft.Quantum.Canon.CCNOTop)

생성에 사용할 CCNOT gate입니다.


### <a name="controls--qubit"></a>컨트롤: [이상](xref:microsoft.quantum.lang-ref.qubit)[]

및 사다리의 컨트롤로 사용할 비트의 레지스터입니다.
이 작업은 고정의 계산 기준 상태를 유지 `controls` 합니다.
의 길이는 `controls` 2 자 이상 이어야 하며,의 길이는 1과 같아야 합니다 `targets` .


### <a name="targets--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

의 길이는 `targets` 1 자 이상 이어야 하 고 1의 길이에서 1을 뺀 값 사이 여야 합니다 `controls` .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

- 및의 일부로 사용 <xref:microsoft.quantum.canon.applymulticontrolledc> <xref:microsoft.quantum.canon.applymulticontrolledca> 됩니다.
- 설명 및 회로 다이어그램의 경우 그림 4.10, Nielsen & Chuang의 섹션 4.3을 참조 하세요.

## <a name="references"></a>참조 항목

- [*Michael Nielsen, Isaac Chuang*, 퀀텀 계산 및 퀀텀 정보](http://doi.org/10.1017/CBO9780511976667)