---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardAmplitudeAmplification
title: StandardAmplitudeAmplification 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardAmplitudeAmplification
qsharp.summary: Standard Amplitude Amplification algorithm
ms.openlocfilehash: 984bfee89b6d79750228b8ca6aaf404f58aecd41
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843938"
---
# <a name="standardamplitudeamplification-function"></a>StandardAmplitudeAmplification 함수

네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


표준 진폭 증폭 알고리즘

```qsharp
function StandardAmplitudeAmplification (nIterations : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>입력

### <a name="niterations--int"></a>nIterations: [Int](xref:microsoft.quantum.lang-ref.int)

진폭 증폭의 $ $n 반복 횟수


### <a name="stateoracle--stateoracle"></a>stateOracle: [Stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)

시작 상태를 준비 하는 단일 oracle $A $


### <a name="idxflagqubit--int"></a>Idx플래그 [](xref:microsoft.quantum.lang-ref.int)

플래그에 대 한 인덱스입니다.



## <a name="output--qubit--unit--is-adj--ctl"></a>출력:가 중 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Adj + Ctl입니다.

표준 진폭 증폭 퀀텀 알고리즘을 구현 하는 작업입니다.

## <a name="remarks"></a>설명

이는 `AmpAmpPhasesStandard` \Begin{align} A\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ text {target}} s + \sqrt{1-| \lambda | ^ 2} \ket f\cdots로 가정 하 여 계산 된 리플렉션 단계 중에서 가져온 표준 진폭 증폭 알고리즘입니다. \_ {0} \_ 이 작업을 \end{align} 대부분의 경우 \begin{align} \operatorname{AmpAmpByOracle}\ket {0} \_ {f} \ket {0} \_ s = \lambda ((2n + 1) \lambda ^ {-1} (\lambda)) \ket {1} \_ f\ket {\ text {target}} \_ s + \cdots\ket {0} \_ f \end{align}을 준비 `flagQubit` 하 고, `auxiliaryRegister` 상태 $ \ket {0} \_ f\ket {0} \_ a $에서 초기화 됩니다.

## <a name="references"></a>참조

- [*G. Brtis, Hoyer, M. Mosca, .Ttapp*](https://arxiv.org/abs/quant-ph/0005055)