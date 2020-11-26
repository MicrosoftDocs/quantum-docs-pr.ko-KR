---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: AssertProbInt 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: b95c2c6294dd5a95b7215c22bd6c50a41635f432
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223700"
---
# <a name="assertprobint-operation"></a>AssertProbInt 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


퀀텀 레지스터의 특정 상태에 대 한 확률이 예상 값을 가지는 것을 어설션 합니다.

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a>Description

$N $-stbit 퀀텀 상태 $ \ket{\psi} = \sum ^ {2 ^ n-1} _ {j = 0} \ alpha_j \ket{j} $로 지정 된 상태 $ \ket{j} $ $j 인덱싱된 상태 $ $의 확률 $ | \ alpha_j | ^ 2 $에 필요한 값이 있음을 어설션 합니다.

## <a name="input"></a>입력

### <a name="stateindex--int"></a>stateIndex: [Int](xref:microsoft.quantum.lang-ref.int)

레지스터가 나타내는 $ \ket{j} $ 상태의 인덱스 $j $입니다 `LittleEndian` .


### <a name="expected--double"></a>예상: [Double](xref:microsoft.quantum.lang-ref.double)

예상 값은 $ | \ alpha_j | ^ 2 $입니다.


### <a name="qubits--littleendian"></a>작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$ \Ket{\psi} $를 거의 endian 형식으로 저장 하는?


### <a name="tolerance--double"></a>허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)

실제 및 예상의 차이에 대 한 절대 허용 오차입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

