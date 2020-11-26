---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyObliviousAmplitudeAmplification
title: ApplyObliviousAmplitudeAmplification 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyObliviousAmplitudeAmplification
qsharp.summary: Oblivious amplitude amplification by specifying partial reflections.
ms.openlocfilehash: 9b0060201bcdae02a207362a753a0a403cdbb896
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191519"
---
# <a name="applyobliviousamplitudeamplification-operation"></a>ApplyObliviousAmplitudeAmplification 작업

네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


부분 반사를 지정 하 여 명확한 진폭 증폭

```qsharp
operation ApplyObliviousAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, auxiliaryRegister : Qubit[], systemRegister : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="phases--reflectionphases"></a>단계: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

부분 반사의 단계


### <a name="startstatereflection--reflectionoracle"></a>startStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

보조 레지스터의 시작 상태에 대 한 리플렉션 연산자


### <a name="targetstatereflection--reflectionoracle"></a>targetStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

보조 레지스터의 대상 상태에 대 한 리플렉션 연산자


### <a name="signaloracle--obliviousoracle"></a>signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

`ObliviousOracle`보조 및 시스템 레지스터에 대해 공동으로 작동 하는 형식의 단일 oracle $O $입니다.


### <a name="auxiliaryregister--qubit"></a>auxiliaryRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

보조 레지스터


### <a name="systemregister--qubit"></a>systemRegister: [Ontbit](xref:microsoft.quantum.lang-ref.qubit)[]

시스템 등록



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

특정 보조 시작 상태 $ \ket{\text{start}} \_ a $, 특정 보조 대상 상태 $ \ket{\text{target}} \_ a $ 및 모든 시스템 상태 $ \ket{\psi} s $가 지정 된 \_ 경우 일부 단일 $U $에 대해 \begin{align} O\ket {\ text {start}} \_ a\ket {\ psi} \_ s = \lambda\ket{\text{target}} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{\text{target} ^ \perp} a\cdots \end{align}이 있다고 가정 \_ 합니다.
및 해당 adjoint의 응용 프로그램에 의해 인터리브 된 보조 레지스터의 시작 및 대상 상태에 대 한 반사 시퀀스를 통해 `signalOracle` U 적용의 성공 확률이 변경 될 수 있습니다.

대부분의 경우 `auxiliaryRegister` 는 $ \ket{\text{start}} a $ 상태에서 초기화 됩니다 \_ .

## <a name="references"></a>참조 항목

참조 항목

- 표준 버전에 대 한 [ *D.W. Berry, A.M. Childs, Cleve, Kothari, R.D. Somma*](https://arxiv.org/abs/1312.1414) 입니다.
  참조 항목
- [ *G.H. Low, I.L. Chuang*](https://arxiv.org/abs/1610.06546) 를 통해 부분 반사를 일반화 합니다.