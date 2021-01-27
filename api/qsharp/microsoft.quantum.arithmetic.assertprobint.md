---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: AssertProbInt 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: 85ff04bbad9dc2ed0f803db65508fdfbb0d22c56
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843397"
---
# <a name="assertprobint-operation"></a>AssertProbInt 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


퀀텀 레지스터의 특정 상태에 대 한 확률이 예상 값을 가지는 것을 어설션 합니다.

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a>설명

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



## <a name="example"></a>예

`qubits`레지스터가 3abit 퀀텀 상태 $ \ket{\psi} = \ sqrt {1/8} \ k {0} + \ sqrt {7/8} \ k $를 거의 endian 형식으로 인코드 한다고 가정 합니다 {6} .
즉, 숫자는 $ \ket {0} \equiv\ket {0} \ket {0} \ket {0} $ 및 $ \ket \equiv\ket \ket {6} {0} \ket $로 표시 {1} {1} 됩니다. 그러면 다음 어설션이 성공 합니다.

```qsharp
AssertProbInt(0, 0.125, qubits, 10e-10);
AssertProbInt(6, 0.875, qubits, 10e-10);
```