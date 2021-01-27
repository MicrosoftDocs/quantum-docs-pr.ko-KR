---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: EstimateTermExpectation 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: 7df4c1ea859140a669698434c6f8a786ea3bc2ea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835663"
---
# <a name="estimatetermexpectation-operation"></a>EstimateTermExpectation 작업

네임 스페이스: [JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


지정 된 Jordan-Wigner Hamiltonian term에 연결 된 에너지를 계산 합니다.

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a>설명

이 작업은 각 측정 연산자에 연결 된 예상 값을 예측 하 고 샘플링을 사용 하 여 해당 계수를 곱합니다.
결과는 Jordan-Wigner 용어의 에너지를 포함 하는 변수로 집계 됩니다.

## <a name="input"></a>입력

### <a name="inputstateunitary--qubit--unit--is-adj"></a>inputStateUnitary: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj

상태 준비에 사용 되는 단일.


### <a name="ops--pauli"></a>ops: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Jordan-Wigner 용어의 측정 연산자입니다.


### <a name="coeffs--double"></a>coeffs: [Double](xref:microsoft.quantum.lang-ref.double)[]

Jordan-Wigner 용어의 계수입니다.


### <a name="nqubits--int"></a>N Bits: [Int](xref:microsoft.quantum.lang-ref.int)

분자 시스템을 시뮬레이트하는 데 필요한 비트 수입니다.


### <a name="nsamples--int"></a>nSamples: [Int](xref:microsoft.quantum.lang-ref.int)

용어 예상을 추정 하는 데 사용할 샘플 수입니다.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)

Jordan-Wigner 용어에 연결 된 에너지입니다.