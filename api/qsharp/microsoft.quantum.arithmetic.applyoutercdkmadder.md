---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterCDKMAdder
title: ApplyOuterCDKMAdder 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterCDKMAdder
qsharp.summary: Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below. Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.
ms.openlocfilehash: acaa563245bb7c701316d2dfd35b5be03d8e024d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843717"
---
# <a name="applyoutercdkmadder-operation"></a>ApplyOuterCDKMAdder 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


해독 가능한 내부 ripple 작업은 아래 RippleCarryAdderCDKM 정수 더하기 연산에 사용 됩니다.
두 개의 두 가지 비트 레지스터 `xs` 와 `ys` 길이가 동일한 경우 작업은 CNOT 및 ccnot 게이트의 ripple 작업 시퀀스를의 `xs` 및의 `ys` 컨트롤 및 컨트롤 및의에 있는 컨트롤 및의 컨트롤 및의에 대 한으로 적용 합니다 `xs` .

```qsharp
operation ApplyOuterCDKMAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="xs--littleendian"></a>xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

컨트롤 및 대상을 포함 하는 첫 번째 비트율 비트 레지스터입니다.


### <a name="ys--littleendian"></a>작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

컨트롤에 영향을 주는 두 번째 비트율 비트 레지스터입니다.


### <a name="ancilla--qubit"></a>ancilla: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

이 작업에 전달 된 RippleCarryAdderCDKM에서 사용 되는 ancilla 이상 비트입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>참조

- Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new 퀀텀 ripple and A new, 2004.
  https://arxiv.org/abs/quant-ph/0410184v1