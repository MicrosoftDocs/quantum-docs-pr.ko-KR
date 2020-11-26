---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledLowDepthAnd
title: ApplyMultiplyControlledLowDepthAnd 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledLowDepthAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.  Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.
ms.openlocfilehash: 1aeab429bd6304c621e0d5225b43a76eab607c84
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209199"
---
# <a name="applymultiplycontrolledlowdepthand-operation"></a>ApplyMultiplyControlledLowDepthAnd 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


는 해당 대상의 비트를 0으로 초기화 한다고 가정 하 고 다중 제어 된 Toffoli gate를 구현 합니다.  Adjoint 연산은 대상의 비트를 0으로 다시 설정 한다고 가정 합니다.  에는 Rz 깊이가 1이 필요 하지만 도우미의 수는 지 수의 지 수입니다.

```qsharp
operation ApplyMultiplyControlledLowDepthAnd (controls : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="input"></a>입력

### <a name="controls--qubit"></a>컨트롤: [이상](xref:microsoft.quantum.lang-ref.qubit)[]

제어 비트


### <a name="target--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

대상 비트



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

