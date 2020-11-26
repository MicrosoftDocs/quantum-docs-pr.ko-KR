---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledCA
title: ApplyMultiControlledCA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledCA
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: 28797583c23e21eb4bcae996a34c70ee06c6dbe8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209284"
---
# <a name="applymulticontrolledca-operation"></a>ApplyMultiControlledCA 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


단일 제어 작업의 곱셈 제어 버전을 적용 합니다.
한정자는 `CA` 단일의 비트 작업을 제어 하 고 adjointable 나타냅니다.

```qsharp
operation ApplyMultiControlledCA (singlyControlledOp : (Qubit[] => Unit is Adj), ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="singlycontrolledop--qubit--unit--is-adj"></a>singlyControlledOp: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is

단일 비트에 대해 제어 되는 연산입니다.
작업의 인수에서 첫 번째 인수는 컨트롤로 간주 되 고 나머지는 대상 비트 비트로 간주 됩니다.
`ApplyMultiControlled` 항상 `singlyControlledOp` 1 이상의 길이 인수를 사용 하 여를 호출 합니다.


### <a name="ccnot--ccnotop"></a>ccnot: [Ccnotop](xref:Microsoft.Quantum.Canon.CCNOTop)

생성에 사용할 제어 되지 않은 제어 된 게이트입니다.


### <a name="controls--qubit"></a>컨트롤: [이상](xref:microsoft.quantum.lang-ref.qubit)[]

`singlyControlledOp`제어 될의 대상 비트입니다.
의 길이는 `controls` 1 이상 이어야 합니다.


### <a name="targets--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

에 대해 작동 하는 대상 비트 `singlyControlledOp` 입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

이 작업은 clean ancilla  비트만 사용 합니다.

설명 및 회로 다이어그램의 경우 그림 4.10, Nielsen & Chuang의 섹션 4.3을 참조 하세요.

## <a name="references"></a>참조 항목

- [*Michael Nielsen, Isaac Chuang*, 퀀텀 계산 및 퀀텀 정보](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a>참고 항목

- [ApplyMultiControlledC입니다.](xref:Microsoft.Quantum.Canon.ApplyMultiControlledC)