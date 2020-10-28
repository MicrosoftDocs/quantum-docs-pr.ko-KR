---
uid: Microsoft.Quantum.Characterization.EstimateFrequencyA
title: EstimateFrequencyA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequencyA
qsharp.summary: Given a preparation that is adjointable and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: 88f0a237975c158bffcc015f79d2134b210ce83b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715065"
---
# <a name="estimatefrequencya-operation"></a>EstimateFrequencyA 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)

패키지 [](https://nuget.org/packages/)


Adjointable 및 측정 준비를 고려 하 여 지정 된 수의 평가판을 수행 하 여 측정값이 성공 (반환) 하는 빈도를 추정 `Zero` 합니다.

```qsharp
operation EstimateFrequencyA (preparation : (Qubit[] => Unit is Adj), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>입력

### <a name="preparation--qubit--unit-adj"></a>준비:가 중 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj

Adjointable 작업은 지정 된 상태 $ \rho $를 입력 레지스터에서 준비 하는 $ $P 합니다.


### <a name="measurement--qubit--__invalidresult__"></a>측정: [값](xref:microsoft.quantum.lang-ref.qubit)이 __잘못 <Result> 된__ > 

작업 $M $는 관심 측정을 나타냅니다.


### <a name="nqubits--int"></a>N Bits: [Int](xref:microsoft.quantum.lang-ref.int)

각 작업의 준비 및 측정값이 작동 하는 데 사용할 수 있는 값입니다.


### <a name="nmeasurements--int"></a>n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)

관련 빈도를 예측 하기 위해 측정이 수행 되어야 하는 횟수입니다.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)

$M (P (\ket{00 \cdots 0} \bra{00 \cdots 0})) $가 반환 되 `Zero` 고, 비편향 이항 평가기 $ \hat{p} = n {\uparrow}/n {\text{measurements}} $를 사용 하 여 얻은 빈도의 예상 $ \hat{p} $ \_ \_ \_ 입니다. 여기서 $n {\uparrow} $은 관찰 된 결과의 수입니다 `Zero` .

## <a name="remarks"></a>설명

Adjointable 작업의 경우 작업을 호출 하는 것과 같은 특정 가정을 수행할 수 있습니다 .이 경우 대상 컴퓨터에서 성능 최적화를 수행할 수 있도록 하는 작업을 정확히 동일한 상태로 준비 합니다.