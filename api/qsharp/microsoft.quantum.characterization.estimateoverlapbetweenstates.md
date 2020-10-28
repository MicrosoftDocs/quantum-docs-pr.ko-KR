---
uid: Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates
title: EstimateOverlapBetweenStates 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the squared overlap between the states prepared by each operation.
ms.openlocfilehash: 58a367c7ff7d13ac5c1eb1588fb8dac66414776c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714995"
---
# <a name="estimateoverlapbetweenstates-operation"></a>EstimateOverlapBetweenStates 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)

패키지 [](https://nuget.org/packages/)


각각 상태의 복사본을 준비 하는 두 개의 작업이 지정 된 경우 각 작업에 의해 준비 된 상태 사이에서 제곱이 중복 되는 것을 추정 합니다.

```qsharp
operation EstimateOverlapBetweenStates (preparation1 : (Qubit[] => Unit is Adj), preparation2 : (Qubit[] => Unit is Adj), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>입력

### <a name="preparation1--qubit--unit-adj"></a>preparation1: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)

비교할 두 개의 상태 준비 작업 중 첫 번째 작업입니다.


### <a name="preparation2--qubit--unit-adj"></a>preparation2: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)

비교할 두 개의 상태 준비 작업 중 두 번째입니다.


### <a name="nqubits--int"></a>N Bits: [Int](xref:microsoft.quantum.lang-ref.int)

`commonPreparation`, `preparation1` 및가 모두 작동 하는 데 사용할 수 있는 값입니다 `preparation2` .


### <a name="nmeasurements--int"></a>n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)

겹치기를 추정 하는 데 사용할 측정 수입니다.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>설명

이 작업은 교환 테스트를 사용 하 여 $ $ \begin{align} \left |를 찾습니다. \braket{00\cdots 0 | V ^ {\dagger} U | 00 \ cdots 0} \right | ^ 2 \end{align} $ $ 여기서 $U $은의 동작에 대 한 단일 표현 `preparation1` 이며 $V $는에 해당 `preparation2` 합니다.

## <a name="see-also"></a>참고 항목

- [EstimateRealOverlapBetweenStates.](xref:Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates)
- [EstimateImagOverlapBetweenStates.](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)