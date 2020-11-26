---
uid: Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates
title: EstimateRealOverlapBetweenStates 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateRealOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the real part of the overlap between the states prepared by each operation.
ms.openlocfilehash: d9f569ceffc16f377189dc94035213b9075609cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216186"
---
# <a name="estimaterealoverlapbetweenstates-operation"></a>EstimateRealOverlapBetweenStates 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


각각 상태의 복사본을 준비 하는 두 개의 작업이 지정 된 경우 각 작업에서 준비 된 상태 간에 겹치는 부분을 예상 합니다.

```qsharp
operation EstimateRealOverlapBetweenStates (commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>입력

### <a name="commonpreparation--qubit--unit--is-adj"></a>commonPreparation: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is

고정 된 입력 상태를 준비 하는 작업입니다.


### <a name="preparation1--qubit--unit--is-adj--ctl"></a>preparation1: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl + Ctl

비교할 두 개의 상태 준비 작업 중 첫 번째 작업입니다.


### <a name="preparation2--qubit--unit--is-adj--ctl"></a>preparation2: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl + Ctl

비교할 두 개의 상태 준비 작업 중 두 번째입니다.


### <a name="nqubits--int"></a>N Bits: [Int](xref:microsoft.quantum.lang-ref.int)

`commonPreparation`, `preparation1` 및가 모두 작동 하는 데 사용할 수 있는 값입니다 `preparation2` .


### <a name="nmeasurements--int"></a>n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)

겹치기를 추정 하는 데 사용할 측정 수입니다.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>설명

이 작업은 Hadamard 테스트를 사용 하 여 $ $ \begin{align} \braket{\psi |의 실제 부분을 찾습니다. V ^ {\dagger} U | \psi} \end{align} $ $ where $ \ket{\psi} $는에 의해 준비 된 상태이 `commonPreparation` 고, $U $은의 동작에 대 한 단일 표현 `preparation1` 이며, $V $은에 해당 `preparation2` 합니다.

## <a name="references"></a>참조 항목

- Aharonov *et al.* [/0511096](https://arxiv.org/abs/quant-ph/0511096)입니다.

## <a name="see-also"></a>참고 항목

- [EstimateImagOverlapBetweenStates.](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)
- [EstimateOverlapBetweenStates.](xref:Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates)