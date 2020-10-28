---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable
title: ApplyXControlledOnTruthTable 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTable
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: 73d63936f02a52dfbbad7b8575110177a9e4463d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725247"
---
# <a name="applyxcontrolledontruthtable-operation"></a>ApplyXControlledOnTruthTable 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지 [](https://nuget.org/packages/)


@"microsoft.quantum.intrinsic.x" `target` `func` 의 기존 할당에 대해 부울 함수가 true로 평가 되는 경우에 작업을 적용 합니다 `controlRegister` .

```qsharp
operation ApplyXControlledOnTruthTable (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="description"></a>Description

작업은 단일 작업 \begin{align} U\ket {x} \ k {y} = \ket{x}\ket{y \oplus f (x)} \end{align}을 구현 합니다. 여기서 $x $ 및 $y $는 `controlRegister` `target` 각각 및를 나타냅니다.

부울 함수 $f $는 큰 정수를 기준으로 참 테이블로 표현 됩니다.
예를 들어 세 입력의 과반수 함수는 bitstring으로 표현 됩니다 `11101000` . 여기서 가장 중요 한 비트는 `1` 입력 할당에 해당 하 `(1, 1, 1)` 고 가장 중요 한 비트는 `0` 입력 할당에 해당 합니다 `(0, 0, 0)` .
이 값은 `0xE8L` 16 진수 표기법으로 큰 정수 또는 10 진수 표기법으로 나타낼 수 있습니다 `232L` .  `L`접미사는 상수가 형식 임을 나타냅니다 `BigInt` .
이 표현에 대 한 자세한 내용은 [kata 테이블](https://github.com/microsoft/QuantumKatas/tree/main/TruthTables)에서도 확인할 수 있습니다.

구현에서는 @"microsoft.quantum.intrinsic.cnot" 및 게이트를 사용 @"microsoft.quantum.intrinsic.r1" 합니다.

## <a name="input"></a>입력

### <a name="func--bigint"></a>func: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

큰 정수로 표시 되는 부울 참 테이블


### <a name="controlregister--qubit"></a>controlRegister: [bit](xref:microsoft.quantum.lang-ref.qubit)[]

컨트롤의 등록


### <a name="target--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

대상 비트



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>참조

- [*Schuch* , *Siewert* , prl 91, 027902, 2003, arxiv:/0303063](https://arxiv.org/abs/quant-ph/0303063)
- [*Mathias Soeken* , *Martin Roetteler* , arxiv: 2005.12310](https://arxiv.org/abs/2005.12310)

## <a name="see-also"></a>참고 항목

- [ApplyXControlledOnTruthTableWithCleanTarget.](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget)