---
uid: Microsoft.Quantum.AmplitudeAmplification.ObliviousAmplitudeAmplificationFromStatePreparation
title: ObliviousAmplitudeAmplificationFromStatePreparation 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ObliviousAmplitudeAmplificationFromStatePreparation
qsharp.summary: Oblivious amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 9975d26af8f9beb2b91e409ad78159d6f04936e3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721831"
---
# <a name="obliviousamplitudeamplificationfromstatepreparation-function"></a>ObliviousAmplitudeAmplificationFromStatePreparation 함수

네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

패키지 [](https://nuget.org/packages/)


부분 반사에 대해 oracles 명확한 진폭 증폭

```qsharp
function ObliviousAmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, idxFlagQubit : Int) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a>입력

### <a name="phases--reflectionphases"></a>단계: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

부분 반사의 단계


### <a name="startstateoracle--deterministicstateoracle"></a>startStateOracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

보조 시작 상태를 준비 하는 단일 oracle $A $


### <a name="signaloracle--obliviousoracle"></a>signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

`ObliviousOracle`보조 및 시스템 레지스터에 공동으로 작동 하는 형식의 단일 oracle $O $


### <a name="idxflagqubit--int"></a>Idx플래그 [Int](xref:microsoft.quantum.lang-ref.int)

단일 수준 비트 플래그 레지스터의 인덱스입니다.



## <a name="output--qubitqubit--unit-adj--ctl"></a>출력: (Adj[[]](xref:microsoft.quantum.lang-ref.qubit)[, []](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl

부분 반사를 기준으로 명확한 진폭 증폭을 구현 하는 작업입니다.

## <a name="remarks"></a>설명

이로 인해의 보조 시작 및 대상 상태 형식에 보다 엄격한 조건이 부과 `AmpAmpObliviousByReflectionPhases` 됩니다.
$A \ket {0} \_ f\ket {0} \_ A = \ket{\text{start}} \_ {fa} $는 \_ 계산 기준 $ \ket f\ket $에서 보조 시작 상태 $ \ket{\text{start}} {fa} $를 준비 {0} \_ {0} 하는 것으로 가정 합니다.
대상 상태가 $ \ket f $로 표시 되어 있다고 가정 합니다 {1} \_ .
\Begin{align} O\ket {\ text {start}} \_ {fa} \ket{\psi} \_ s = \lambda\ket {1} \_ f\ket {\ text {모든}} \_ a\ket {\ text {target}} \_ s U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots,에 대 한 일부 단일 $U $로 가정 합니다.