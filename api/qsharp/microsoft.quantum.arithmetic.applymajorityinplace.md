---
uid: Microsoft.Quantum.Arithmetic.ApplyMajorityInPlace
title: ApplyMajorityInPlace 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyMajorityInPlace
qsharp.summary: Applies the three-qubit majority operation in-place on a register of qubits.
ms.openlocfilehash: 10b512392b2098663c09b2e07a09c4025da90706
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843722"
---
# <a name="applymajorityinplace-operation"></a>ApplyMajorityInPlace 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


은 (는) 다양 한 비트의 레지스터에 세 가지 주요 비트 작업을 적용 합니다.

```qsharp
operation ApplyMajorityInPlace (output : Qubit, input : Qubit[]) : Unit is Adj + Ctl
```


## <a name="description"></a>설명

이 작업을 수행 하면 3 개의 환경에서 과반수 함수를 계산 합니다.

출력을 $z $로 표시 하 고 입력을 $x $ 및 $y $로 표시 하는 경우 작업은 $ \ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)} $ 변환을 수행 합니다.

## <a name="input"></a>입력

### <a name="output--qubit"></a>출력: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

첫 번째 입력 비트입니다. 출력은 내부에서 계산 된 후에 저장 됩니다.


### <a name="input--qubit"></a>input: [bit](xref:microsoft.quantum.lang-ref.qubit)[]

두 번째 및 세 번째 입력 비트입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

