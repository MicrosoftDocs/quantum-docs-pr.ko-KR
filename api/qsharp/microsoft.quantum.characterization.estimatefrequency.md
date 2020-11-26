---
uid: Microsoft.Quantum.Characterization.EstimateFrequency
title: EstimateFrequency 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequency
qsharp.summary: Given a preparation and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: 30b21a8e86eb5a4dd8dd8207dbdc6a0970308319
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216254"
---
# <a name="estimatefrequency-operation"></a>EstimateFrequency 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


준비 및 측정을 고려 하 여 `Zero` 지정 된 수의 평가판을 수행 하 여 측정값이 성공 (반환) 하는 빈도를 추정 합니다.

```qsharp
operation EstimateFrequency (preparation : (Qubit[] => Unit), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>입력

### <a name="preparation--qubit--unit"></a>준비: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit) 

지정 된 상태 $ \rho $를 해당 입력 레지스터에 준비 하는 작업을 $ $P 합니다.


### <a name="measurement--qubit--__invalidresult__"></a>측정: [값](xref:microsoft.quantum.lang-ref.qubit)이 __잘못 <Result> 된__> 

작업 $M $는 관심 측정을 나타냅니다.


### <a name="nqubits--int"></a>N Bits: [Int](xref:microsoft.quantum.lang-ref.int)

각 작업의 준비 및 측정값이 작동 하는 데 사용할 수 있는 값입니다.


### <a name="nmeasurements--int"></a>n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)

관련 빈도를 예측 하기 위해 측정이 수행 되어야 하는 횟수입니다.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)

$M (P (\ket{00 \cdots 0} \bra{00 \cdots 0})) $가 반환 되 `Zero` 고, 비편향 이항 평가기 $ \hat{p} = n {\uparrow}/n {\text{measurements}} $를 사용 하 여 얻은 빈도의 예상 $ \hat{p} $ \_ \_ \_ 입니다. 여기서 $n {\uparrow} $은 관찰 된 결과의 수입니다 `Zero` .

이는 확률을 측정할 수 없다는 점에서 물리적인 제한을 적용 하는 대상 컴퓨터에서 특히 중요 합니다.