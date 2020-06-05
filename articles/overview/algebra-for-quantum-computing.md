---
title: 양자 컴퓨팅을 위한 선형 대수
description: 양자 컴퓨팅을 이해하는 데 필요한 기본 선형 대수 개념에 대해 알아봅니다.
author: bradben
ms.author: bradben
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.algebra
ms.openlocfilehash: 4750643d16ad8af6240df42c1b93353565561429
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327597"
---
# <a name="linear-algebra-for-quantum-computing"></a>양자 컴퓨팅을 위한 선형 대수

선형 대수는 양자 컴퓨팅의 언어입니다. 양자 프로그램을 구현하거나 작성하기 위해 알 필요는 없지만, 큐비트 상태와 양자 연산을 설명하고 양자 컴퓨터가 일련의 명령에 응답하여 수행하는 작업을 예측하는 데 널리 사용됩니다.

[양자 물리학의 기본 개념](xref:microsoft.quantum.overview.understanding)을 익히는 것이 양자 컴퓨팅을 이해하는데 도움이 되는 것처럼 몇 가지 기본적인 선형 대수를 알면 양자 알고리즘의 작동 방식을 이해하는 데 도움이 됩니다. 적어도 **벡터** 및 **행렬 곱**에 익숙해져야 합니다. 이러한 대수 개념에 대한 지식을 새로 고쳐야 하는 경우 기본 사항을 다루고 있는 몇 가지 자습서는 다음과 같습니다.

- [선형 대수에 대한 Jupyter Notebook 자습서](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/LinearAlgebra)
- [복소수 연산에 대한 Jupyter Notebook 자습서](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ComplexArithmetic)
- [양자 계산을 위한 선형 대수](https://cds.cern.ch/record/1522001/files/978-1-4614-6336-8_BookBackMatter.pdf)
- [선형 대수의 기본 사항](https://www.math.ubc.ca/~carrell/NB.pdf)
- [양자 계산 입문](https://www.codeproject.com/Articles/5155638/Quantum-Computation-Primer-Part-1#exploring-quantum-superposition)

## <a name="vectors-and-matrices-in-quantum-computing"></a>양자 컴퓨팅의 벡터 및 행렬

[양자 컴퓨팅 이해](xref:microsoft.quantum.overview.understanding) 항목에서 큐비트가 1 또는 0 상태이거나 중첩이거나 둘 다일 수 있음을 확인했습니다. 선형 대수를 사용하면 큐비트 상태가 벡터로 설명되며 $\begin{bmatrix} a \\\\  b \end{bmatrix}$ 단일 열 **행렬**로 표시됩니다. 또한 **양자 상태 벡터**라고도 하며 $|a|^2 + |b|^2 = 1$라는 요구 사항을 충족해야 합니다.  

행렬의 요소는 큐비트가 한 방향 또는 다른 방향으로 붕괴될 확률을 나타내며, $|a|^2$는 0으로 붕괴될 확률이고 $|b|^2$는 1로 붕괴될 확률입니다. 다음 행렬은 모두 유효한 양자 상태 벡터를 나타냅니다.

$$\begin{bmatrix} 1 \\\\  0 \end{bmatrix}, \begin{bmatrix} 0 \\\\  1 \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{1}{\sqrt{2}} \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{-1}{\sqrt{2}} \end{bmatrix}, \text{ and }\begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{i}{\sqrt{2}} \end{bmatrix}.$$

[양자 컴퓨터 및 양자 시뮬레이터](xref:microsoft.quantum.overview.simulators)에서도 양자 연산이 큐비트 상태를 수정하는 데 사용됨을 확인했습니다.  또한 양자 연산은 행렬로 나타낼 수 있습니다. 양자 연산이 큐비트에 적용되면 이를 나타내는 두 개의 행렬을 곱하고 결과 답에서 연산 후의 새 큐비트 상태를 나타냅니다.  

다음은 행렬 곱으로 나타내는 두 가지 일반적인 양자 연산입니다.


[`X` 연산](xref:microsoft.quantum.intrinsic.x)은 $X$ Pauli 행렬로 나타냅니다.

$$X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix},$$
    
그리고 큐비트 상태를 0에서 1로(또는 반대로) 대칭 이동하는 데 사용됩니다. 예를 들어 다음과 같습니다.

$$\begin{bmatrix}0 &1\\\\ 1 &0\end{bmatrix}\begin{bmatrix} 1 \\\\  0 \end{bmatrix} = \begin{bmatrix} 0 \\\\  1 \end{bmatrix}.$$

['H' 연산](xref:microsoft.quantum.intrinsic.h)은 $H$ Hadamard 변환으로 나타냅니다.

$$H = \dfrac{1}{\sqrt{2}}\begin{bmatrix}1 &1\\\\ 1 &-1\end{bmatrix},$$

 그리고 아래와 같이 큐비트를 어느 한 쪽으로 붕괴될 확률이 동일한 중첩 상태로 전환합니다.

$$\frac{1}{\sqrt{2}}\begin{bmatrix}1 &1\\\\ 1 &-1\end{bmatrix}\begin{bmatrix} 1 \\\\  0 \end{bmatrix}=\frac{1}{\sqrt{2}}\begin{bmatrix} 1 \\\\  1 \end{bmatrix}=\left(\frac{1}{\sqrt{2}}\right)^2=\frac{1}{2}.$$

양자 연산을 나타내는 행렬에는 **단위** 행렬이어야 한다는 한 가지 요구 사항이 있습니다. **역** 행렬이 행렬의 **켤레 전치(conjugate transpose)** 와 같으면 해당 행렬은 단위 행렬입니다.

## <a name="representing-two-qubit-states"></a>2개 큐비트 상태 표현

위의 예에서 한 큐비트의 상태는 $\begin{bmatrix} a \\\\  b \end{bmatrix}$ 단일 열 행렬을 사용하여 설명했으며, 연산을 적용하는 것은 두 행렬을 곱하여 설명했습니다. 그러나 양자 컴퓨터는 둘 이상의 큐비트를 사용하므로 두 큐비트의 결합된 상태는 어떻게 설명할까요? 

각 큐비트는 벡터 공간이므로 곱할 수는 없습니다. 대신 개별 벡터 공간에서 새 벡터 공간을 만들고 $\otimes$ 기호로 표현되는 관련 연산인 **텐서 곱**을 사용합니다. 예를 들어 두 개의 큐비트 상태($\begin{bmatrix} a \\\\  b \end{bmatrix}$ 및 $\begin{bmatrix} c \\\\  d \end{bmatrix}$)의 텐서 곱이 계산됩니다.

$$ \begin{bmatrix} a \\\\  b \end{bmatrix} \otimes \begin{bmatrix} c \\\\  d \end{bmatrix} =\begin{bmatrix} a \begin{bmatrix} c \\\\  d \end{bmatrix} \\\\ b \begin{bmatrix}c \\\\  d \end{bmatrix} \end{bmatrix} = \begin{bmatrix} ac \\\\  ad \\\\  bc \\\\  bd \end{bmatrix}.
$$

결과는 각 요소에서 확률을 나타내는 4차원 행렬입니다. 예를 들어 $ac$는 두 큐비트가 0과 0으로 붕괴될 확률이고, $ad$는 0과 1의 확률 등입니다. 

양자 상태를 나타내기 위해 $\begin{bmatrix} a \\\\  b \end{bmatrix}$ 단일 큐비트 상태에서 $|a|^2 + |b|^2 = 1$라는 요구 사항을 충족해야 하는 것처럼 $\begin{bmatrix} ac \\\\  ad \\\\  bc \\\\  bd \end{bmatrix}$ 2개 큐비트 상태는 $|ac|^2 + |ad|^2 + |bc|^2+ |bd|^2 = 1$라는 요구 사항을 충족해야 합니다.

## <a name="summary"></a>요약

선형 대수는 양자 컴퓨팅과 양자 물리학을 설명하기 위한 표준 언어입니다. Microsoft Quantum Development Kit에 포함된 [라이브러리](xref:microsoft.quantum.libraries)는 기본 수학을 자세히 숙지하지 않고도 고급 양자 알고리즘을 실행하는 데 도움이 되지만, 기본 사항을 이해하면 빠르게 시작하고 견고한 기반을 구축할 수 있습니다.

## <a name="next-steps"></a>다음 단계

[QDK 설치](xref:microsoft.quantum.install)