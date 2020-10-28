---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: MAJ 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: c1801d1d7ed04ead11b672f24d44a94989cf8f1d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721016"
---
# <a name="maj-operation"></a>MAJ 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지 [](https://nuget.org/packages/)


이는 내부 과반수 작업을 3 개의 비트에 적용 합니다.

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit
```


## <a name="description"></a>Description

$ \Ket{z} $로 대상의 상태를 표시 하 고 입력의 입력 상태를 $ \ket{x} $ 및 $ \ket{y} $로 표시 하는 경우이 작업은 다음 변환을 수행 합니다. $ \ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)} $.

## <a name="input"></a>입력

### <a name="input0--qubit"></a>input0: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

첫 번째 입력 비트입니다.


### <a name="input1--qubit"></a>input1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

두 번째 입력 비트입니다.


### <a name="target--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

과반수 함수가 적용 될 대상입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

