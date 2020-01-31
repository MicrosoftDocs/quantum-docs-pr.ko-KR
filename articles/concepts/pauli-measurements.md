---
title: Pauli 측정
description: Pauli 측정
author: QuantumWriter
uid: microsoft.quantum.concepts.pauli
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 0a3ee595022ec389ecadcab081ccd126cb3252ae
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76819912"
---
# <a name="pauli-measurements"></a>Pauli 측정

위의 논의에서 계산 기준 측정에 중점을 두었습니다.
사실, 표기법 밑수 관점에서 계산 기준 측정 측면에서 편리 하 게 사용할 수 있는 퀀텀 컴퓨팅에서 발생 하는 다른 일반적인 측정이 있습니다.
Q #로 작업할 때 가장 일반적인 측정 종류는 다른 기본에 대 한 측정치를 포함 하는 계산 기준 측정을 일반화 하 고 다른 다양 한 비트 간의 패리티를 포함 하는 *Pauli 측정이*될 가능성이 높습니다.
이러한 경우에는 일반적으로 $X, Y, Z $ 또는 $Z \otimes Z, X\otimes X, X\otimes Y $ 등과 같은 연산자를 통해 Pauli 연산자 측정을 설명 하는 것이 일반적입니다.

> [!TIP]
> Q #에서 다기능 비트 Pauli 연산자는 일반적으로 `Pauli[]`형식의 배열로 표시 됩니다.
> 예를 들어 $X \otimes Z \otimes Y $를 나타내려면 배열 `[PauliX, PauliZ, PauliY]`를 사용할 수 있습니다.

Pauli 연산자를 기준으로 측정값을 논의 하는 것은 퀀텀 오류 수정의 하위 필드에서 특히 일반적입니다.
Q #에서는 비슷한 규칙을 따릅니다. 이제 측정의 대체 보기에 대해 설명 합니다.

Pauli를 측정 하는 방법에 대 한 세부 정보를 살펴보기 하기 전에 퀀텀 컴퓨터 내의 단일 요소를 퀀텀 상태로 측정 하는 것을 고려 하는 것이 유용 합니다.
$- Bit 퀀텀 상태 $n 있다고 가정 합니다. 그런 다음, 해당 상태가 될 수 있는 $2 ^ n $의 절반에 해당 하는 규칙을 즉시 측정 합니다.
즉, 측정은 퀀텀 상태를 두 개의 반 공간 중 하나로 프로젝션 합니다.
이 intuition을 반영 하기 위해 측정 하는 방식을 일반화할 수 있습니다.

이러한 하위 공간을 간결 하 게 식별 하기 위해 설명을 위한 언어가 필요 합니다.
두 개의 하위 공간을 설명 하는 한 가지 방법은 규칙에 따라 $ \pm $1이 되도록 하는 두 개의 고유한 eigenvalues만 있는 행렬을 통해 지정 하는 것입니다.
이러한 방식으로 하위 공간을 설명 하는 간단한 예제를 보려면 $Z $:

$ $ \begin{align} Z & = \begin{bmatrix} 1 & 0 \\\\ 0 &-1 \end{bmatrix}.
\end{align} $ $

고유 벡터 $ matrix $Z의 대각선 요소를 읽으면 $Z $에 해당 고유 값 $ \pm $1이 포함 된 두 개의 $ \ket{0}$ 및 $ \ket{1}$가 있는 것을 볼 수 있습니다.
따라서 \ket을 측정 하 고 `Zero` (state ${0}$)를 가져오는 경우이의 상태는 $Z $ 연산자의 $ + $1 eigenstate 임을 알 수 있습니다.
마찬가지로 `One`를 얻는 경우이의 상태는 $Z $의 $-$1 eigenstate 임을 알 수 있습니다.
이 프로세스는 "측정 Pauli $Z $" 라고 하는 Pauli 측정 언어에서 계산 기반 측정을 수행 하는 것과 완전히 동일 합니다.

모든 $2 \ times $2 매트릭스가 $Z $의 단일 변환 인 경우에도이 조건을 충족 합니다.
즉, 행렬 $A = U ^ \aaz U $를 사용할 수도 있습니다. 여기서 $U $은 다른 단일 매트릭스 이며, $ \dagger $1 고유 벡터에서 측정의 두 결과를 정의 하는 행렬을 제공 합니다.
Pauli 측정의 표기법은 $X, Y, Z $ 측정값을 해당 하는 것과 같은 측정값으로 식별 하 여이 단일 동등성을 참조 합니다.
이러한 측정은 편의를 위해 아래에 제공 됩니다.


|Pauli 측정  |단일 변환  |
|-------------------|------------------------|
| $Z $               | $ \boldone $             |
| $X $               | $H $                    |
| $Y $               | $HS ^ {\dagger} $         |

즉,이 언어를 사용 하는 경우 "measure $Y $"는 $HS ^ \dagger $를 적용 한 다음 계산 단위로 측정 하는 것과 같습니다. 여기서 [`S`](xref:microsoft.quantum.intrinsic.s) 은 "단계 게이트" 라고도 하는 내장 퀀텀 연산이 며 단일 행렬에 의해 시뮬레이션 될 수 있습니다.

$ $ \begin{align} S = \begin{bmatrix} 1 & 0 \\\\ 0 & i \end{bmatrix}.
\end{align} $ $

또한 $HS ^ \aa$를 퀀텀 상태 벡터에 적용 한 다음 $Z $를 측정 하 여 다음 작업을 `Measure([PauliY], [q]])`와 동일 하 게 하는 것과 같습니다.

```Q#
operation MeasureY(qubit : Qubit) : Result {
    mutable result = Zero;
    within {
        H(q);
        Adjoint S(q);
    } apply {
        set result = M(q);
    }
    return result;
}
```

그런 다음 계산 기준으로 다시 변환 하 여 올바른 상태를 찾을 수 있습니다 .이는 퀀텀 상태 벡터에 $SH $를 적용 하는 것입니다. 위의 코드 조각에서 계산 기준으로 다시 변환 하는 것은 `within … apply` 블록을 사용 하 여 자동으로 처리 됩니다.

Q #에서 결과---즉, 상태---와 상호 작용 하 여 추출 된 일반 정보는 \\{\texttt{Zero}, \texttt{One}\\} $에서 $j \uli 연산자의 $ (-1) ^ j $ eigenspace에 결과가 있는지를 나타내는 `Result` 값으로 제공 됩니다.


## <a name="multiple-qubit-measurements"></a>여러 비트 측정

다음에서 볼 수 있듯이 다중 기능 비트 Pauli 연산자의 측정은 유사 하 게 정의 됩니다.

$ $ Z\otimes Z = \begin{bmatrix}1 & 0 & 0 & 0\\\\ 0 &-1 & 0 & 0\\\\ 0 & 0 &-1 & 0\\\\ 0 & 0 & 0 & 1 \ end {bmatrix}.
$$

따라서 두 텐서 $ operators $Z 제품은 $ + $1 및 $-$1 eigenvalues로 구성 된 두 개의 공백으로 구성 된 행렬을 형성 합니다.
단일 수준 비트의 경우와 마찬가지로 두 가지 모두 반 공간을 구성 합니다 .이는 액세스 가능한 벡터 공간의 절반이 $ + $1 eigenspace와 $-$1 eigenspace의 나머지 절반에 속합니다.
일반적으로 텐서 제품의 정의에서 쉽게 확인할 수 있습니다. 텐서는 Pauli-$Z $ operators의 모든 제품 이며 id는이를 따르는 합니다.
예를 들면 다음과 같습니다.

$ $ \begin{align} Z \otimes \boldone = \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 &-1 & 0 \\\\ 0 & 0 & 0 &-1 \end{bmatrix}.
\end{align} $ $

이전 처럼 이러한 매트릭스의 모든 단일 변환은 $ \pm $1 eigenvalues로 레이블이 지정 된 두 개의 절반 공간에 대해서도 설명 합니다.
예를 들어 $Z = HXH $ 인 id에서 \otimes X = H\otimes H (Z\otimes Z) H\otimes H $를 $X 합니다.
1 배 비트의 경우와 마찬가지로, 모든 2 배 비트 Pauli 측정값을 $U ^ \Atimes (Z\otimes \dagger) U $ for $4 \ times $4 단일 매트릭스 $U $로 작성할 수 있습니다. 다음 표에서는 변환을 열거 합니다.

> [!NOTE]
> 아래 표에서 $ \operatorname{SWAP} $를 사용 하 여 행렬 $ $ \begin{align} \operatorname{SWAP} & = \left (\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{matrix}\right) \end{align} $ $를 사용 하 여 기본 작업 [`SWAP`](xref:microsoft.quantum.intrinsic)를 시뮬레이션 합니다.

|Pauli 측정     |단일 변환  |
|----------------------|------------------------|
| $Z \otimes \boldone $ | $ \boldone \otimes \boldone $ |
| $Z \otimes \boldone $ | $ \boldone\otimes \boldone $ |
| $X \otimes \boldone $ | $H \otimes \boldone $ |
| $Y \otimes \boldone $ | $HS ^ \dagger\otimes \boldone $ |
| $ \boldone \otimes Z $ | $ \operatorname{SWAP} $ |
| $ \boldone \otimes X $ | $ (H\otimes \boldone) \operatorname{SWAP} $ |
| $ \boldone \otimes Y $ | $ (HS ^ \dagger\otimes \boldone) \operatorname{SWAP} $ |
| $Z \otimes Z $ | $ \operatorname{CNOT}\_{10}$ |
| $X \otimes Z $ | $ \operatorname{CNOT}\_{10}(H\otimes \boldone) $ |
| $Y \otimes Z $ | $ \operatorname{CNOT}\_{10}(HS ^ \dagger\otimes \boldone) $ |
| $Z \otimes X $ | $ \operatorname{CNOT}\_{10}(\boldone\otimes H) $ |
| $X \otimes X $ | $ \operatorname{CNOT}\_{10}(H\otimes H) $ |
| $Y \otimes X $ | $ \operatorname{CNOT}\_{10}(HS ^ \dagger\otimes H) $ |
| $Z \otimes Y $ | $ \operatorname{CNOT}\_{10}(\boldone \otimes HS ^ \a) $ |
| $X \otimes Y $ | $ \operatorname{CNOT}\_{10}(H\otimes HS ^ \aatimes) $ |
| $Y \otimes Y $ | $ \operatorname{CNOT}\_{10}(HS ^ \dagger\otimes HS ^ \dagger) $ |

여기에서 다음과 같은 이유로 [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) 작업이 표시 됩니다.
$ \Boldone $ matrix를 포함 하지 않는 각 Pauli 측정값은 위의 추론에 의해 $Z \otimes Z Z까지 동일 합니다.
$Z \otimes Z $의 고유 값는 각 계산 기준 벡터를 구성 하는 eibit의 패리티에만 의존 하며 제어 되지 않는 작업은이 패리티를 계산 하 여 첫 번째 비트에 저장 하는 데 사용 됩니다.
그런 다음 첫 번째 비트를 측정 한 후에는 Pauli 연산자를 측정 하는 것과 동일한 결과의 절반 공간 id를 복구할 수 있습니다.

한 가지 추가 참고 사항: $Z \otimes Z $를 측정 하는 것은 $Z \otimes \mathbb{1}$ 및 $ \mathbb{1} \otimes Z $로 순차적으로 측정 하는 것으로 간주 될 수 있습니다 .이 가정은 false입니다.
그 이유는 $Z \otimes Z $를 측정 하는 것은 퀀텀 상태를 이러한 연산자의 $ + $1 또는 $-$1 eigenstate로 프로젝션 하는 것입니다.
$Z \otimes \mathbb{1}$를 측정 한 다음 $ \mathbb{1} \otimes Z $는 퀀텀 상태 벡터를 $Z \otimes \mathbb{1}$의 절반 공간에 먼저 추가한 다음, $ \mathbb{1} \otimes Z $의 절반 공간으로 프로젝션 합니다.
네 가지 계산 기준 벡터가 있으므로 두 측정값을 모두 수행 하면 상태가 1/4로 줄어들고 단일 계산 기준 벡터로 줄어듭니다.

## <a name="correlations-between-qubits"></a>이상 비트 간의 상관 관계
$X \otimes X $ 또는 $Z \otimes Z $와 같이 Pauli 매트릭스의 텐서 곱을 측정 하는 또 다른 방법은 이러한 측정을 사용 하 여 두 개의 두 비트 간 상관 관계에 저장 된 정보를 확인할 수 있다는 것입니다.
$X \otimes \id $를 측정 하면 첫 번째 비트에 로컬로 저장 된 정보를 볼 수 있습니다.
두 유형의 측정은 모두 퀀텀 컴퓨팅에서 동일 하 게 중요 하지만, 이전에는 퀀텀 컴퓨팅의 기능을 비춥니다.
이는 퀀텀 컴퓨팅에서 배워야 하는 정보는 단일의 모든 기능에 저장 되지 않지만, 한 번에 모든 ombit에 로컬로 저장 되는 것이 아니라 공동 측정 (예: $Z \otimes Z $)을 통해서만 볼 수 있음을 나타냅니다. 정보는 매니페스트가 됩니다.

예를 들어 오류 수정에서는 보호 하려는 상태에 대 한 정보를 확인 하는 동안 발생 한 오류를 배우는 경우가 많습니다.
[비트 대칭 코드 샘플](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) 은 $Z \Otimes z \otimes \otimes 및 $ \id\otimes z \otimes z $와 같은 측정값을 사용 하 여이 작업을 수행 하는 방법의 예를 보여 줍니다.
<!-- TODO: change this to a link to the samples browser as soon as the bit-flip code sample is on-boarded. -->

$X \otimes Y \otimes Z \otimes \boldone $와 같은 임의의 Pauli 연산자를 측정할 수도 있습니다.
모든 pauli 연산자의 텐서 제품에는 두 개의 고유 값 $ \pm $1만 있고 고유 값는 모두 벡터 공간의 반 공간을 구성 합니다.
따라서 위에 명시 된 요구 사항과 일치 합니다.

Q #에서 이러한 측정값은 측정값이 $ (-1) ^ j $ 기호에 대 한 결과를 생성 하는 경우 $ $j $로 반환 됩니다.
Q #의 기본 제공 기능으로 Pauli를 측정 하는 것은 이러한 연산자를 측정 하기 위해 diagonalizing $U $ gate를 $Z $ 및 $ \id $의 텐서 제품으로 표현 하는 데 필요한 $ gate를 설명 하기 위해 장기 변환 및 기준 변환의 긴 체인을 요구 하기 때문에 유용 합니다.
이러한 미리 정의 된 측정값 중 하나를 수행 하도록 지정할 수 있으므로 계산 기준 측정이 필요한 정보를 제공 하도록를 변환 하는 방법을 걱정 하지 않아도 됩니다.
Q #는 자동으로 필요한 모든 기본 변환을 처리 합니다.
자세한 내용은 [`Measure`](xref:microsoft.quantum.intrinsic.measure) 및 [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) 작업을 참조 하세요.

## <a name="the-no-cloning-theorem"></a>복제 안 함 정리

퀀텀 정보는 강력 합니다.
이를 통해 가장 잘 알려진 기존 알고리즘 보다 많은 수치를 지 원하는 것과 같은 놀라운 작업을 수행할 수 있습니다.
그러나 퀀텀 컴퓨팅의 기능에는 제한이 있습니다.
이러한 제한 사항 중 하나는 *복제 안 함 정리*에서 제공 됩니다.

복제 안 함 정리의 이름은 무엇입니다.
퀀텀 컴퓨터에의 한 일반 퀀텀 상태 복제를 허용 하지 않습니다.
정리 증명은 매우 간단 합니다.
이에 대 한 설명에는 복제 안 함 정리의 전체 증명을 사용 하는 것이 약간 기술적 이지만, 추가 보조 기능을 사용 하지 않는 경우에는 범위 내에 있습니다 (보조 비트는 계산 중에는 스크래치 공간에 사용 되 고 Q #에서 쉽게 사용 되며 관리 되는 경우 <xref:microsoft.quantum.techniques.qubits>참조).

이러한 퀀텀 컴퓨터의 경우 단일 행렬에서 복제 작업을 설명 해야 합니다.
복제 하려고 하는 퀀텀 상태를 손상 시킬 수 있으므로 측정이 허용 되지 않습니다.
복제 작업을 시뮬레이션 하기 위해 모든 상태 $ \ket{\psi} $에 대해 $ $ U \ket{\psi} \ket{0} = \ket{\psi} \ket{\psi} $ $의 속성을 사용 하는 데 사용 되는 단일 행렬을 원합니다.
행렬 곱셈의 선형 속성은 두 번째 퀀텀 상태 $ \ket{\phi} $에 대해

$ $ \begin{align} U \left [\frac{1}{\left{2}} \left (\ket{\phi} + \ket{\psi} \left) \left] \ket{0} & = \frac{1}{\left{2}} U\ket {\left} \ U\ket{0} + \frac{1}{\left{2}} {\ psi} \ k{0} \\\\ & = \frac{1}{\left{2}} \left (\ket{\phi} \ket{\phi} + \ket{\psi} \ket{\psi} \left) \\\\ & \ne \left (\frac{1}{\left{2}} \oml (\ket{\phi} + \ket{\psi} \left) \left) left (\frac{1}{\sqrt{2}} \left (\ket{\phi} + \ket{\psi} \right) \right).
\end{align} $ $

이는 복제 안 함 정리의 기본적인 intuition을 제공 합니다. 알 수 없는 퀀텀 상태를 복사 하는 모든 장치는 복사 하는 일부 상태에서 오류를 유도 해야 합니다.
Cloner는 입력 상태에서 선형으로 작동 하는 주요 가정을 추가 하 고 보조 비트를 측정 하 여 위반할 수 있습니다. 또한 이러한 상호 작용은 측정 통계를 통해 시스템에 대 한 정보를 누출 하 고 정확 하 게 방지 합니다. 이러한 경우에도 복제 합니다.
복제 안 함 정리에 대 한 자세한 [내용은](xref:microsoft.quantum.more-information)을 참조 하십시오.

퀀텀 상태 저렴를 복제할 수 있는 경우 퀀텀 상태를 정리 하는 근거리 및 마법 기능을 제공 하기 때문에 복제 안 함은 퀀텀 컴퓨팅에 대 한 정 성적을 이해 하는 데 중요 합니다.
정말 Heisenberg의 vaunted 불확실성 원칙을 위반할 수 있습니다.
또는 최적의 cloner를 사용 하 여 복잡 한 퀀텀 배포에서 단일 샘플을 가져오고 한 샘플에서 해당 배포에 대해 알아볼 수 있는 모든 것을 알아볼 수 있습니다.
이는 동전 및 관찰 헤드를 대칭 이동 하 고 응답 하는 결과에 대해 friend를 전달 하는 것과 같습니다. "Ah는 해당 동전의 분포는 $p = 0.512643 \ ldots $!"를 사용 하 여 베르누이 되어야 합니다.  한 가지 정보 (헤드 결과)가 상당한 이전 정보 없이 배포를 인코딩하는 데 필요한 많은 양의 정보를 제공할 수 없기 때문에 이러한 문은 sensical 되지 않습니다.
마찬가지로, 이전 정보가 없으면 $p $를 몰라도 이러한 동전의 앙상블를 준비할 수 없기 때문에 퀀텀 상태를 완벽 하 게 복제할 수 없습니다.

정보는 퀀텀 컴퓨팅에서 무료로 제공 됩니다.
측정 된 각는 단일 비트 정보를 제공 하 고, 복제 안 함 정리는 시스템 및 해당 시스템에 대해 발생 하는 파업에 대 한 정보 간의 기본적인 균형을 유지 하기 위해 악용할 수 있는 백도어가 없음을 보여 줍니다.
