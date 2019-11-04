---
title: Pauli 측정 | Microsoft Docs
description: Pauli 측정
author: QuantumWriter
uid: microsoft.quantum.concepts.pauli
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 7bea821be7e26e72f2860278486d35be676ca63d
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183712"
---
# <a name="pauli-measurements"></a>Pauli 측정

위의 논의에서 계산 기준 측정에 중점을 두었습니다.  사실 퀀텀 컴퓨팅에서 발생 하는 다른 일반적인 측정은 표기법 밑수 관점에서 계산 기준 측정 측면에서 편리 하 게 표현할 수 있습니다.  이러한 측정의 가장 일반적인 집합은 *Pauli를 측정*한 것입니다.  이러한 경우에는 일반적으로 $X, Y, Z $ 또는 $Z \otimes Z, X\otimes X, X\otimes Y $ 등의 연산자를 통해 Pauli 연산자 측정을 설명 하는 것이 일반적입니다.  Pauli 연산자를 기준으로 측정값을 논의 하는 것은 퀀텀 오류 수정의 하위 필드에서 특히 일반적입니다. Q #에서는 비슷한 규칙을 따릅니다. 이제 측정의 대체 보기에 대해 설명 합니다.

Pauli를 측정 하는 방법에 대 한 세부 정보를 살펴보기 하기 전에 퀀텀 컴퓨터 내의 단일 요소를 퀀텀 상태로 측정 하는 것을 고려 하는 것이 유용 합니다.  $- Bit 퀀텀 상태 $n 있다고 가정 합니다. 그런 다음, 해당 상태가 될 수 있는 $2 ^ n $의 절반에 해당 하는 규칙을 즉시 측정 합니다.  즉, 측정은 퀀텀 상태를 두 개의 반 공간 중 하나로 프로젝션 합니다.  이를 반영 하기 위해 측정에 대해 생각 하는 방식을 일반화할 수 있습니다.

이러한 하위 공간을 간결 하 게 식별 하기 위해 설명을 위한 언어가 필요 합니다.  이 작업을 수행 하는 한 가지 방법은 규칙에 따라 $ \pm $1이 되는 두 개의 고유한 eigenvalues가 있는 행렬을 통해 두 개의 하위 공간을 지정 하 여 설명 하는 것입니다.  이에 대 한 가장 간단한 예는 다음과 같습니다.

$ $ Z = \begin{bmatrix} 1 & 0 \\\\ 0 &-1 \end{bmatrix}.
$$

Pauli-$Z $ 행렬에는 고유 값 $ \pm $1을 포함 하는 두 개의 고유 벡터 $ \ket{0}$ 및 $ \ket{1}$가 명확 하 게 포함 되어 있습니다.  따라서, 고유 벡터를 측정 하 고 $ \ket{0}를 얻는 경우이 연산자의 $ + $1 eigenspace (긍정 또는 단지 음수 eigenspace만 있는의 합계를 포함 하는 모든 벡터 집합)와 $ \ket{1}$를 측정 하는 경우 $-$1 ei에 있습니다. $Z $의 genspace입니다.  이 프로세스는 "측정 Pauli $Z $" 라고 하는 Pauli 측정 언어에서 계산 기반 측정을 수행 하는 것과 완전히 동일 합니다.

물론 $Z $의 단일 변환 인 $2 \ times $2 매트릭스가이 조건을 충족 합니다.  이는 모든 단일 행렬 $U $에 대해 행렬 $A = U ^ \a턴 Z U $를 고려 하 여 $ \dagger $1 고유 벡터에서 측정의 두 가지 결과를 정의 하는 행렬을 제공할 수 있다는 것입니다.  Pauli 측정의 표기법은 $X, Y, Z $ 측정값을 동일한 측정값으로 식별 하 여이를 참조 합니다.  이러한 측정은 편의를 위해 아래에 제공 됩니다.

$ $ \begin{array}{| c | c |} \Begin{array}{측정} & U\\\\ Z & \boldone\\\\ X & H\\\\ Y & HS ^ \\\\\ \end{array} $ $

즉,이 언어를 사용 하는 경우 "measure $Y $"는 $HS ^ \dagger $를 적용 한 다음 계산 단위로 측정 하는 것과 같습니다. 여기서 $S $은로 지정 된 단계 게이트입니다.

$ $ \begin{bmatrix}1 & 0\\\\ 0 & i\end {bmatrix}.
$$

또한 $HS ^ \aate$를 퀀텀 상태 벡터에 적용 한 다음 $Z $를 측정 하는 것과 같습니다.  그런 다음 계산 기준으로 다시 변환 하 여 올바른 상태를 찾을 수 있습니다 .이는 퀀텀 상태 벡터에 $SH $를 적용 하는 것입니다.

## <a name="q-outcome-classical-information-obtained-from-quantum-state"></a>Q # 퀀텀 상태에서 가져온 기존 정보
Q #에서 결과, 즉 상태와의 상호 작용에서 추출 된 기존의 정보는 $ (-1) ^ j 연산자의 $ (-1) ^ j $ eigenspace로 측정 된 경우 집합 $\{0, 1\}$에 있는 $ $j $입니다.

다음에서 볼 수 있듯이 다중 기능 비트 Pauli 연산자의 측정은 유사 하 게 정의 됩니다.

$ $ Z\otimes Z = \begin{bmatrix}1 & 0 & 0 & 0\\\\ 0 &-1 & 0 & 0\\\\ 0 & 0 &-1 & 0\\\\ 0 & 0 & 0 & 1 \ end {bmatrix}.
$$

따라서 두 텐서 $ operators $Z 제품은 $ + $1 및 $-$1 eigenvalues로 구성 된 두 개의 공백으로 구성 된 행렬을 형성 합니다.  단일 수준 비트의 경우와 마찬가지로 두 가지 모두 반 공간을 구성 합니다 .이는 액세스 가능한 벡터 공간의 절반이 $ + $1 eigenspace와 $-$1 eigenspace의 나머지 절반에 속합니다.  일반적으로 텐서 제품의 정의에서 쉽게 확인할 수 있습니다. 텐서는 Pauli-$Z $ operators의 모든 제품 이며 id는이를 따르는 합니다.  예를 들면 다음과 같습니다.

$ $ Z\otimes\boldone = \begin{bmatrix} 1 & 0 & 0 & 0\\\\ 0 & 1 & 0 & 0\\\\ 0 & 0 &-1 & 0\\\\ 0 & 0 & 0 &-1 \ end {bmatrix}.
$$

이전 처럼 이러한 매트릭스의 모든 단일 변환은 $ \pm $1 eigenvalues로 레이블이 지정 된 두 개의 절반 공간에 대해서도 설명 합니다.  예를 들어 $Z = HXH $ 인 id에서 \otimes X = H\otimes H (Z\otimes Z) H\otimes H $를 $X 합니다.  1 배 비트의 경우와 마찬가지로, 모든 2 배 비트 Pauli 측정값을 $U ^ \Atimes (Z\otimes \dagger) U $ for $4 \ times $4 단일 매트릭스 $U $로 작성할 수 있습니다.  다음 표의 변환을 열거 합니다. 여기서는 \operatorname{CNOT} $0 $ 및 $1 $: $ \operatorname{SWAP} =\_{01}\operatorname{CNOT}\_{10}\operatorname{를 교환 하는 교환 게이트를 편리 하 게 소개 합니다. CNOT}\_{01}$:

$ $ \begin{array}{| c | c |} \Begin{array}{측정} & U\\\\ \hline Z\otimes \boldone & \boldone\otimes \boldone\\\\ X\otimes \boldone & H\otimes \boldone\\\\ Y\otimes \boldone & HS ^ \dagger\ otimes \boldone\\\\ \boldone \otimes Z & \operatorname{SWAP}\\\\ \boldone \otimes X & (H\otimes \boldone) \operatorname{SWAP}\\\\ \boldone \otimes Y & (HS ^ \dagger\otimes \boldone) \ a m e {SWAP}\\\\ Z\otimes Z & \operatorname{CNOT}\_{10}\\\\ X\otimes Z & \operatorname{CNOT}\_{10}(H\otimes \boldone)\\\\ Y\otimes Z & \ a m e {CNOT}\_{10}(HS ^ \dagger\otimes \boldone)\\\\ Z\otimes X & \operatorname{CNOT}\_{10}(\boldone\otimes H)\\\\ X\otimes X & \operatorname{CNOT}\_@no__t _31_ (h\otimes H)\\\\ Y\otimes X & \operatorname{CNOT}\_{10}(HS ^ \dagger\otimes H)\\\\ Z\otimes Y & \operatorname{CNOT}\_{10}(\boldone \otimes HS s ^ \)\\41_ x\otimes Y & \operatorname{CNOT}\_{10}(H\otimes HS ^ \aatimes)\\\\ Y\otimes Y & \operatorname{CNOT}\_{10}(HS ^ \dagger\otimes HS ^ \aas)\\\\ \end{array} $ $

여기서 $ \operatorname{CNOT}\_{10}$ 문이 다음과 같은 이유로 나타납니다.  $ \Boldone $ matrix를 포함 하지 않는 각 Pauli 측정값은 위의 추론에 의해 $Z \otimes Z Z까지 동일 합니다.  $Z \otimes Z $의 고유 값는 각 계산 기준 벡터를 구성 하는 eibit의 패리티에만 의존 하며이 목록에 표시 되는 제어 되지 않는 작업은이 패리티를 계산 하 여 첫 번째 비트에 저장 하는 데 사용 됩니다.  그런 다음 첫 번째 비트를 측정 한 후에는 Pauli 연산자를 측정 하는 것과 동일한 결과 반 공간의 id를 복구할 수 있습니다.

추가 참고 사항 중 하나는 $Z \otimes Z $를 측정 하 여 $Z \otimes \id $로 측정 하 고 $ \id\otimes Z $를 측정 하는 것으로 가정 하는 것입니다 .이 가정은 false가 될 수 있습니다.  그 이유는 $Z \otimes Z $를 측정 하는 것은 퀀텀 상태를 이러한 연산자의 $ + $1 또는 $-$1 eigenstate로 프로젝션 하는 것입니다.  $Z \otimes \id $를 측정 한 다음 $ \id \otimes Z $는 퀀텀 상태 벡터를 먼저 $Z \otimes \oatimes $로, 그 다음에는 절반의 절반 공간에 $ \id\otimes Z $로 프로젝션 합니다.  네 가지 계산 기준 벡터가 있으므로 두 측정값을 모두 수행 하면 상태가 1/4로 줄어들고 단일 계산 기준 벡터로 줄어듭니다.


## <a name="correlations-between-qubits"></a>이상 비트 간의 상관 관계
$X \otimes X $ 또는 $Z \otimes Z $와 같이 Paulis의 텐서 제품을 측정 하는 또 다른 방법은 이러한 측정을 사용 하 여 두 개의 두 비트 간 상관 관계에 저장 된 정보를 확인 하는 것입니다.  $X \otimes \id $를 측정 하면 첫 번째 비트에 로컬로 저장 된 정보를 볼 수 있습니다.  두 유형의 측정은 모두 퀀텀 컴퓨팅에서 동일 하 게 중요 하지만, 이전에는 퀀텀 컴퓨팅의 기능을 비춥니다. 이 정보는 퀀텀 컴퓨팅에서 배워야 하는 정보가 단일의 모든 비트에 저장 되지 않고 한 번에 모든 ombits에 로컬로 저장 되는 것이 아니라 $Z \otimes Z $를 사용 하 여이 정보를 확인 하는 경우에만이 정보를 볼 수 있음을 나타냅니다. manifest.xml.

$X \otimes Y \otimes Z \otimes \boldone $와 같은 임의의 Pauli 연산자를 측정할 수도 있습니다.  모든 pauli 연산자의 텐서 제품에는 두 개의 고유 값 $ \pm $1만 있고 고유 값는 모두 벡터 공간의 반 공간을 구성 합니다.  따라서 위에 명시 된 요구 사항과 일치 합니다.

Q #에서 이러한 측정값은 측정값이 $ (-1) ^ j $ 기호에 대 한 결과를 생성 하는 경우 $ $j $로 반환 됩니다.  이를 Q #의 기본 제공 기능으로 사용 하면 이러한 연산자를 측정 하는 데에는 $Z $ 및 $ \id $의 텐서 제품으로 작업을 표현 하는 데 필요한 diagonalizing $U $ gate를 설명 하기 위해 이러한 연산자를 측정 하는 데 사용 되는 긴 변환 및 기준 변환의 긴 체인이 필요 하므로 도움이 됩니다  이러한 미리 정의 된 측정값 중 하나를 수행 하도록 지정할 수 있으면 계산 기준 측정이 필요한 정보를 제공 하도록 하는 방법을 걱정 하지 않아도 됩니다.  Q #는 자동으로 필요한 모든 기본 변환을 처리 합니다. [Pauli 측정에 대 한 Q # 라이브러리 참조를](/qsharp/api/canon/microsoft.quantum.canon.measurepaulis) 참조 하세요.

## <a name="the-no-cloning-theorem"></a>복제 안 함 정리
퀀텀 정보는 강력 합니다.  이를 통해 가장 잘 알려진 기존 알고리즘 보다 많은 수치를 지 원하는 것과 같은 놀라운 작업을 수행할 수 있습니다.  그러나 퀀텀 컴퓨팅의 기능에는 제한이 있습니다.  이러한 제한 사항 중 하나는 *복제 안 함 정리*에서 제공 됩니다.

복제 안 함 정리의 이름은 무엇입니다.
퀀텀 컴퓨터에의 한 일반 퀀텀 상태 복제를 허용 하지 않습니다.
정리 증명은 매우 간단 합니다.
이에 대 한 설명에는 복제 안 함 정리의 전체 증명을 사용 하는 것이 약간 기술적 이지만, 해당 하는 퀀텀 컴퓨터의 정리에 추가 ancilla가 없는 경우에는 해당 범위 내에 있습니다. Q #에서 계산 하 고 쉽게 사용 하 고 관리할 수 있는 공간입니다. <xref:microsoft.quantum.techniques.qubits>)를 참조 하세요.
이러한 퀀텀 컴퓨터의 경우 복제 작업은 단일 행렬 이어야 합니다. 복제 하려고 하는 퀀텀 상태를 손상 시킬 수 있으므로 측정이 허용 되지 않습니다. 원하는 단일 행렬에는 모든 상태 $ \ket{\psi} $에 대해 $ $ U \ket{\psi} \ket{0} = \ket{\psi} \ket{\psi}, $ $ 인 속성이 있어야 합니다.
행렬 곱셈의 선형 속성은 두 번째 퀀텀 상태 $ \ket{\phi} $에 대해

\begin{align} & U\left [\frac{1}{\sqrt{2}} \left (\ket{\phi} + \ket{\psi} \right) \right] \ket{0}= \frac{1}{\sqrt{2}} U\ket {\ l} \ k{0}+ \frac{1}{\sqrt{2}} U\ket {\ psi} \ k{0}@no__ t_9_ \\ & \qquad\qquad = \frac{1}{\sqrt{2}} \left (\ket{\phi}\ket{\phi} + \ket{\psi}\ket{\psi}\right)\\\\ & \qquad\qquad\ne \left (\frac{1}{\sqrt{2}} \\omp (\ket{\phi} + \ket{\psi} \) right) \otimes\left (\frac{1}{\right{2}} \right (\ket{\phi} + \ket{\psi} \right) \right).
\end{align}

이는 복제 안 함 정리의 기본적인 intuition을 제공 합니다. 알 수 없는 퀀텀 상태를 복사 하는 모든 장치는 복사 하는 일부 상태에서 오류를 유도 해야 합니다.  Cloner는 입력 상태에서 선형으로 동작 하는 것으로 가정 하는 반면 ancilla의 ancilla 및 측정을 추가 하 여 해당 상호 작용은 측정 통계를 통해 시스템에 대 한 정보를 누설 하 고 방지 합니다. 이러한 경우에도 정확한 복제  복제 안 함 정리에 대 한 자세한 [내용은](xref:microsoft.quantum.more-information)을 참조 하십시오.

퀀텀 상태 저렴를 복제할 수 있는 경우 퀀텀 상태를 정리 하는 근거리 및 마법 기능을 제공 하기 때문에 복제 안 함은 퀀텀 컴퓨팅에 대 한 정 성적을 이해 하는 데 중요 합니다.  정말 Heisenberg의 vaunted 불확실성 원칙을 위반할 수 있습니다.  또는 최적의 cloner를 사용 하 여 복잡 한 퀀텀 배포에서 단일 샘플을 가져오고 한 샘플에서 해당 배포에 대해 알아볼 수 있는 모든 것을 알아볼 수 있습니다.  이는 동전 및 관찰 헤드를 대칭 이동 하 고 응답 하는 결과에 대해 friend를 전달 하는 것과 같습니다. "Ah는 해당 동전의 분포는 $p = 0.512643 \ ldots $!"를 사용 하 여 베르누이 되어야 합니다.  한 가지 정보 (헤드 결과)가 상당한 이전 정보 없이 배포를 인코딩하는 데 필요한 많은 양의 정보를 제공할 수 없기 때문에 이러한 문은 sensical 되지 않습니다.  마찬가지로, 이전 정보가 없으면 $p $를 몰라도 이러한 동전의 앙상블를 준비할 수 없기 때문에 퀀텀 상태를 완벽 하 게 복제할 수 없습니다.

정보는 퀀텀 컴퓨팅에서 무료로 제공 됩니다.  측정 된 각는 단일 비트 정보를 제공 하 고, 복제 안 함 정리는 시스템 및 해당 시스템에 대해 발생 하는 파업에 대 한 정보 간의 기본적인 균형을 유지 하기 위해 악용할 수 있는 백도어가 없음을 보여 줍니다.

