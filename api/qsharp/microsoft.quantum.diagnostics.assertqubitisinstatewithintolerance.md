---
uid: Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance
title: AssertQubitIsInStateWithinTolerance 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitIsInStateWithinTolerance
qsharp.summary: >-
  Asserts that a qubit in the expected state.

  `expected` represents a complex vector, $\ket{\psi} = \begin{bmatrix}a & b\end{bmatrix}^{\mathrm{T}}$. The first element of the tuples representing each of $a$, $b$ is the real part of the complex number, while the second one is the imaginary part. The last argument defines the tolerance with which assertion is made.
ms.openlocfilehash: 1ceb7243cba93e42c67cc3655283a5d07c96863e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202212"
---
# <a name="assertqubitisinstatewithintolerance-operation"></a>AssertQubitIsInStateWithinTolerance 작업

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


예상 상태에서의 비트를 어설션 합니다.

`expected` 복합 벡터, $ \ket{\psi} = \begin{bmatrix}a & b\end {bmatrix} ^ {\mathrm{T}} $를 나타냅니다.
$A $, $b $를 나타내는 튜플의 첫 번째 요소는 복소수의 실수부 이며 두 번째 요소는 허수 부분입니다.
마지막 인수는 어설션이 만들어지는 허용 오차를 정의 합니다.

```qsharp
operation AssertQubitIsInStateWithinTolerance (expected : (Microsoft.Quantum.Math.Complex, Microsoft.Quantum.Math.Complex), register : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a>입력

### <a name="expected--complexcomplex"></a>예상: ([복합](xref:Microsoft.Quantum.Math.Complex),[복합](xref:Microsoft.Quantum.Math.Complex))

각각 $ \ket {0} $ 및 $ \ket $에 대 한 복잡 한 amplitudes {1} 이 필요 합니다.


### <a name="register--qubit"></a>등록: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

상태를 어설션할의 비트입니다. 이 원하는 비트는 할당 되지 않은 다른 것으로 간주 되는 것으로 간주 됩니다.


### <a name="tolerance--double"></a>허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)

실제 amplitudes이 예상 대로 벗어날 수 있는 추가 허용 오차입니다.
자세한 내용은 아래 설명 부분을 참조 하세요.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

다음 Mathematica 코드를 사용 하 여 mi, mx, my, mz에 대 한 식을 확인할 수 있습니다.

```mathematica
{Id, X, Y, Z} = Table[PauliMatrix[k], {k, 0, 3}];
st = {{ reA + I imA }, { reB + I imB} };
M = st . ConjugateTranspose[st];
mx = Tr[M.X] // ComplexExpand;
my = Tr[M.Y] // ComplexExpand;
mz = Tr[M.Z] // ComplexExpand;
mi = Tr[M.Id] // ComplexExpand;
2 m == Id mi + X mx + Z mz + Y my // ComplexExpand // Simplify
```

허용 $L 오차는 \_ 3 차원 실제 벡터 (x ₂, \infty} $ distance x ₃, x ₄)에 의해 정의 된 $ \langle\psi | \psi\rangle = x \_ 1 I + x \_ 2 x + x \_ 3 y + x \_ 4 z $ 및 real vector (y ₂, y ₃, y ₄)에 의해 정의 됩니다. 여기서 ρ는 레지스터의 상태에 해당 하는 밀도 행렬입니다.
이는 Tr (ρ) 및 Tr (| ψ ⟩ ⟨ ψ |)이 모두 1 (예: x ₁ = 1/2, y ₁ = 1/2) 이라는 가정 하에만 적용 됩니다.
그렇지 않은 경우 함수는 l ∞ distance between (x ₂-x ₁, x ₃-x ₁, x ₄-x ₁, x ₄ + x ₁) 및 (y ₂-y ₁, y ₃-y ₁ ₄, y ₁ + y ₄)이 허용 오차 매개 변수 보다 작음을 어설션 합니다.