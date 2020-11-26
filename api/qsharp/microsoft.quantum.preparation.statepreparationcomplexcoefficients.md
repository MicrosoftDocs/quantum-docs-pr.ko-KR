---
uid: Microsoft.Quantum.Preparation.StatePreparationComplexCoefficients
title: StatePreparationComplexCoefficients 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationComplexCoefficients
qsharp.summary: >-
  > [!WARNING]

  > StatePreparationComplexCoefficients has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.


  Returns an operation that prepares a specific quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U\ket{0...0}=\ket{\psi}=\frac{\sum_{j=0}^{2^n-1}r_j e^{i t_j}\ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|r_j|^2}}. \end{align} $$
ms.openlocfilehash: 1d0efa7b83d2e8e75c4b293866f3929f357ec44b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210372"
---
# <a name="statepreparationcomplexcoefficients-function"></a>StatePreparationComplexCoefficients 함수

네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> StatePreparationComplexCoefficients는 더 이상 사용 되지 않습니다. 대신 <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP>를 사용하십시오.

특정 퀀텀 상태를 준비 하는 작업을 반환 합니다.

반환 된 작업 $U $은 $n $-\ket{0...0} $에서 t_j e ^ {i} $ 복합 _j $r 계수를 사용 하 여 임의의 퀀텀 상태 $ \ket{\psi} $을 준비 합니다.

새로 할당 된 레지스터의 U 동작은 $ $ \begin{align} U\ket {0 ... 0} = \ket{\psi} = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}에 의해 제공 됩니다.
\end{align} $ $

```qsharp
function StatePreparationComplexCoefficients (coefficients : Microsoft.Quantum.Math.ComplexPolar[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a>입력

### <a name="coefficients--complexpolar"></a>계수: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]

절대 값으로 표현 되는 $2 ^ n $ 복합 계수와 $ (r_j, t_j) $ 단계로 이루어진 배열입니다. $J $ th 계수는 작은 endian 형식으로 인코딩된 number state $ \ket{j} $를 인덱싱합니다.



## <a name="output--littleendian--unit--is-adj--ctl"></a>출력: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

상태 준비 단일 작업 $U $.

## <a name="remarks"></a>설명

음수 입력 계수 $r _j < $0는 값 $ | r_j | $로 긍정으로 처리 됩니다. `coefficients` $2 ^ n $ 보다 작은 경우는 $ (r_j, t_j) = (0.0, 0.0) $ 요소로 채워집니다.