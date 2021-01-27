---
uid: Microsoft.Quantum.Characterization.SingleQubitProcessTomographyMeasurement
title: SingleQubitProcessTomographyMeasurement 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: SingleQubitProcessTomographyMeasurement
qsharp.summary: Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.
ms.openlocfilehash: 883b98ad4f2d0ac4a02e55e444c04e8e7cf37af5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839647"
---
# <a name="singlequbitprocesstomographymeasurement-operation"></a>SingleQubitProcessTomographyMeasurement 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


특정 채널을 지정 하 여 Pauli에서 단일 tomography 비트 프로세스를 수행 합니다.

```qsharp
operation SingleQubitProcessTomographyMeasurement (preparation : Pauli, measurement : Pauli, channel : (Qubit => Unit)) : Result
```


## <a name="input"></a>입력

### <a name="preparation--pauli"></a>준비: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Pabit를 준비할 수 있는 Pauli 기준 요소 $P입니다.


### <a name="measurement--pauli"></a>측정: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

이 요소는 원하는 비트를 측정할 수 있는 $Q $입니다.


### <a name="channel--qubit--unit"></a>채널:가 중 [비트](xref:microsoft.quantum.lang-ref.qubit) => [단위](xref:microsoft.quantum.lang-ref.unit) 

Process tomography를 사용 하 여 동작을 예측 하는 단일 valbit channel $ \Lambda $.



## <a name="output--__invalidresult__"></a>출력: __잘못 <Result> 됨__

`Zero`확률 $ $ \Begin{align} \Pr (\texttt{Zero} | \Pr;)이 포함 된 결과 P, Q) = \operatorname{Tr}\left (\frac{\boldone + Q} {2} \Lambda\left [\frac{\boldone + P} {2} \right] \right).
\end{align} $ $

## <a name="remarks"></a>설명

이 작업에서 반환 되는 결과에 대 한 분포는 2 ~ 2-tomography의 특별 한 경우입니다. $ \Rho = J (\Lambda)/$2는 $ \Lambda $의 Choi – Jamiłkowski state입니다. 그런 다음 위의 분포가 $ $ \begin{align} \Pr (\texttt{Zero} | \rho;)과 동일 합니다. M) = \operatorname{Tr} (M \rho), \end{align} $ $ where $M = 2 (\boldone + P) ^ \mathrm{T}/2\cdot (\boldone + Q)/$2는 $P $ 및 $Q $에 해당 하는 유효 측정입니다.