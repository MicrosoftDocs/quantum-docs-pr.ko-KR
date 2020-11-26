---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromStatePreparation
title: AmplitudeAmplificationFromStatePreparation 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromStatePreparation
qsharp.summary: Amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 30e1cf6e353b8a4491e13a9e2f588ec9cc103cb4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191604"
---
# <a name="amplitudeamplificationfromstatepreparation-function"></a>AmplitudeAmplificationFromStatePreparation 함수

네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


부분 반사를 위해 oracles에 의해 진폭 증폭

```qsharp
function AmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>입력

### <a name="phases--reflectionphases"></a>단계: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

부분 반사의 단계


### <a name="stateoracle--stateoracle"></a>stateOracle: [Stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)

시작 상태를 준비 하는 단일 oracle $A $


### <a name="idxflagqubit--int"></a>Idx플래그 [Int](xref:microsoft.quantum.lang-ref.int)

플래그에 대 한 인덱스입니다.



## <a name="output--qubit--unit--is-adj--ctl"></a>출력:가 중 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Adj + Ctl입니다.

부분 반사에 의해 구현 되는 oracles에 의해 진폭 증폭을 구현 하는 작업입니다.

## <a name="remarks"></a>설명

이를 통해 보다는 시작 및 대상 상태의 형태에 보다 엄격한 조건을 적용 `AmpAmpByReflectionPhases` 합니다.
대상 상태가 $ \ket f $로 표시 되어 있다고 가정 합니다 {1} \_ .
{0} \_ 대부분의 경우 \begin{align} A\ket {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ text {target}} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\citn, \end{align}가 `flagQubit` `auxiliaryRegister` $ \ket {0} \_ {f} \ket s $ 상태에서 초기화 된다고 가정 {0} \_ 합니다.