---
uid: Microsoft.Quantum.Simulation.BlockEncodingReflectionByLCU
title: BlockEncodingReflectionByLCU 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingReflectionByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncodingReflection`.

  This constructs a `BlockEncodingReflection` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: ef92e517ae40e76c94aff1121c78ece9985109fc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857721"
---
# <a name="blockencodingreflectionbylcu-function"></a>BlockEncodingReflectionByLCU 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


원하는 연산자를로 인코딩합니다 `BlockEncodingReflection` .

이는 `BlockEncodingReflection` 단일 $U = P\cdot V\cdot P ^ \kcdot $를 생성 합니다 .이 경우 일부 연산자 $H = \ sum_ {j} | \ alpha_j | Unitaries의 선형 조합 인 관심 U_j $입니다. 일반적으로 $P $은 $P \ket {0} \_ a \ sum_j \sqrt{\ alpha_j/ \| \vec\alpha \| \_ 2} \ket{j} \_ a $ 및 $V = \ sum_ {j} \ket{j}\bra{j} \_ a\otimes U_j $ 같은 상태 준비의 단일입니다.

```qsharp
function BlockEncodingReflectionByLCU (statePreparation : (Qubit[] => Unit is Adj + Ctl), selector : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a>입력

### <a name="statepreparation--qubit--unit--is-adj--ctl"></a>statePreparation: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

일부 대상 상태를 준비 하는 단일 $P $입니다.


### <a name="selector--qubitqubit--unit--is-adj--ctl"></a>selector: (추가[비트](xref:microsoft.quantum.lang-ref.qubit)[[], [](xref:microsoft.quantum.lang-ref.qubit)]) => [Unit](xref:microsoft.quantum.lang-ref.unit) is Adj + Ctl

$H $의 unitaries 구성 요소를 인코딩하는 단일 $V $입니다.



## <a name="output--blockencodingreflection"></a>출력: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)

단일 $U $는 레지스터에 대해 공동으로 작동 `a` 하며 `s` $H $를 차단 하 고 $U ' ^ {-1} = U $를 충족 합니다.

## <a name="remarks"></a>설명

이 `BlockEncoding` 구현에서는의 속성을 제공 `BlockEncodingReflection` 합니다.

## <a name="see-also"></a>참고 항목

- [Microsoft 양자. 블록 인코딩](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [BlockEncodingReflection.](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)