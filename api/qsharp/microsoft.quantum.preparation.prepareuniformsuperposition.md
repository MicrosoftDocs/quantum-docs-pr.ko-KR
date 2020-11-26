---
uid: Microsoft.Quantum.Preparation.PrepareUniformSuperposition
title: PrepareUniformSuperposition 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareUniformSuperposition
qsharp.summary: >-
  Creates a uniform superposition over states that encode 0 through `nIndices - 1`.

  That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$. In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}. \end{align} $$.
ms.openlocfilehash: 9b9f182ed7c1ea24ae74b8a2321a309042a17c97
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230092"
---
# <a name="prepareuniformsuperposition-operation"></a>PrepareUniformSuperposition 작업

네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


0부터까지 인코딩하는 상태에 대 한 균일 한 superposition를 만듭니다 `nIndices - 1` .

즉,이 단일 $U $는 입력 상태가 $ \ket{0\cdots 0} $ 인 경우 $0 $에서 $1 $M까지 모든 숫자 상태에 대 한 균일 한 superposition를 만듭니다. 즉, $ $ \begin{align} U\ket {0} = \frac {1} {\sqrt{m}}\ sum_ {j = 0} ^ {M-1} \ket{j}.
\end{align} $ $.

```qsharp
operation PrepareUniformSuperposition (nIndices : Int, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="nindices--int"></a>n 인덱스: [Int](xref:microsoft.quantum.lang-ref.int)

Uniform superposition에서 원하는 상태 수 $M $입니다.


### <a name="indexregister--littleendian"></a>indexRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

숫자 상태를 형식으로 저장 하는? `LittleEndian`
이 레지스터는 $M-$1 수를 저장할 수 있어야 하며, $ \ket{0\cdots 0} $ 상태에서 초기화 되는 것으로 간주 됩니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

작업은 adjointable 이지만, `indexRegister` 이 경우에는 첫 번째 기준 상태에서가 균일 한 superposition에 있어야 `nIndices` 합니다.