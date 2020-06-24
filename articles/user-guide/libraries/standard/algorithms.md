---
title: 'Q의 퀀텀 알고리즘 #'
description: 진폭 증폭, 푸리에 변환, Draper 및 Beauregard adders 및 단계 예측을 비롯 한 기본 퀀텀 컴퓨팅 알고리즘에 대해 알아봅니다.
author: QuantumWriter
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.libraries.standard.algorithms
ms.openlocfilehash: 8b8a9019e8bc419f42b0c6f7558354d19a157917
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275769"
---
# <a name="quantum-algorithms"></a>퀀텀 알고리즘 #

## <a name="amplitude-amplification"></a>진폭 증폭 ##

*진폭 증폭* 은 퀀텀 컴퓨팅의 기본 도구 중 하나입니다. Grover의 검색, 진폭 예측 및 많은 퀀텀 기계 학습 알고리즘의 기반이 되는 기본 개념입니다.  많은 변형이 있으며, Q #에서는 응용 프로그램의 가장 넓은 영역을 허용 하는 부분 반사를 사용 하는 명확한 진폭 증폭을 기반으로 하는 일반 버전을 제공 합니다.

진폭 증폭의 중심 개념은 리플렉션 시퀀스를 수행 하 여 원하는 결과가 발생 하는 확률을 강화 하는 것입니다.  이러한 반사는 주로 표시 된 상태 라고 하는 원하는 대상 상태에 가까운 초기 상태를 회전 합니다.  특히 초기 상태를 표시 된 상태에 있는 것으로 측정할 확률이 $ \sin ^ 2 (\sin) $ 인 경우 진폭 $m 증폭을 적용 한 후 $ \sin ^ 2 ((2m + 1) \sin) $가 됩니다.  즉, $ \theta = \ pi/[2 (2n + 1)] $의 일부 값 $n $ then 경우 진폭 증폭은 \\ 진폭 증폭의 $ 반복 $n 후 성공 확률을 $100% $로 상승 시킬 수 있습니다.  $ \Theta = \theta ^ {-1} (\Sqrt{\pr (success)}) $이는 성공 여부를 확인 하는 데 필요한 반복 횟수가 무작위 샘플링을 사용 하 여 명확 하지 않은 상태로 표시 되는 상태를 확인 하는 데 필요한 예상 수보다 quadratically 것을 의미 합니다.

진폭 증폭의 각 반복에서는 두 개의 리플렉션 연산자를 지정 해야 합니다. 특히 $Q $가 진폭 증폭 반복이 고 _0 $ $P 초기 하위 공간에 대 한 프로젝터 연산자이 고, $P _1 $이 프로젝터를 표시 된 하위 공간에 $Q =-(\boldone-2P_0) (\boldone-2P_1) $입니다.  Hermitian는 고유 값 $ + $1 및 $0 $를 포함 하는 연산자이 고, 결과 $ (2P_0 \boldone) $는 unity의 루트 (이 경우 $ \pm $1)가 있는 고유 값를 포함 하기 때문에 고유 합니다. 예를 들어 초기 상태 $H ^ {\otimes n} \ket {0} $ 및 표시 된 상태 $ \ket{m} $, $P _0 = H ^ {\otimes n} \ket {0} \bra {0} H ^ {\otimes n} $ 및 $P _1 = \Ket{m}\bra{m} $ 인 Grover 검색의 경우를 고려 합니다.  진폭 증폭 $P _0 $의 대부분 응용 프로그램에서는 초기 상태에 대 한 프로젝터가 됩니다. 즉, 일부 vector $ \ket{\psi} $ k의 $P _0 = \boldone \ {\ psi} \ bra {\ psi} $입니다. 그러나 명확한 진폭 amplication $P _0 $의 경우 일반적으로 다 수의 퀀텀 상태가 됩니다. 즉, $ + $1 eigenvalue value의 다중성이 $1 $ 보다 큽니다.

진폭 증폭 뒤의 논리는 $Q $의 eigen 분석에서 직접 수행 됩니다.  특히, 초기 상태에서 0이 아닌 고유 벡터를 지 원하는 $ $Q의은 $ + $1 고유 벡터 $P _0 $ 및 $P _1 $의 선형 조합으로 표시 될 수 있습니다.  특히 진폭 증폭의 초기 상태 ($ + $1 $P eigenvector)는 $ $ \ket{\psi} = \frac{-i}{\sqrt {2} } \left (e ^ {i\theta} \ k {\ psi_ +} + e ^ {-i\theta} \ k {\ psi_-} \left)로 작성할 수 있습니다. $ $ where $ \ket{\ psi_ \pm} $는 $Q $에서 고유 값 $e ^ {\left 2i \ 테타} $ 이며 $P _0 $ 및 $P _1 $의 $ + $1 고유 벡터만 지원 합니다.  고유 값 $e ^ {\pm i \theta} $는 연산자 $Q $가 두 개의 프로젝터에 지정 된 2 차원 하위 공간에서 회전을 수행 하 고 회전 각도가 $2 \ 테타 $ 인 초기 상태를 나타냅니다.  그 이유는 $ $Q의 $ 반복 $m 후 성공 확률은 $ \sin ^ 2 ([2m + 1] \sin) $입니다.

이에서 제공 하는 또 다른 유용한 속성은 eigenvalue $ \theta $가 초기 상태가 표시 될 확률과 직접적으로 관련 된다는 것입니다 ($P _0 $이 초기 상태에만 프로젝터 인 경우).  $Q $의 eigenphases $2 \ 테타 = 2 \ sin ^ {-1} (\Sqrt{\pr (success)}) $ 이기 때문에, $Q $에 단계 예측을 적용 하면 단일 퀀텀 프로시저에 대 한 성공 확률을 알 수 있습니다.  이는 필요한 경우 보다 성공 확률을 quadratically 퀀텀 절차의 응용 프로그램을 더 덜 필요로 하기 때문에 유용 합니다.

Q #에서는 진폭 증폭을 명확한 진폭 증폭의 특수화로 도입 했습니다.  명확한 진폭 증폭은 프로젝터를 초기 eigenspace가 초기 상태로 만들지 않아도 되므로이 모니커를 획득 합니다.  이러한 점에서 프로토콜은 초기 상태로 명확한 됩니다.  명확한 진폭 증폭의 주요 응용 프로그램은 단일 Hamiltonian 시뮬레이션 방법의 특정 *선형 조합* 으로, 초기 상태를 알 수 없지만 시뮬레이션 프로토콜에서 ancilla 레지스터를 사용 하 여 레지스터를 사용 합니다.  이 ancilla 레지스터가 고정 값으로 측정 되어야 하는 경우 (예: $0 $) 이러한 시뮬레이션 메서드는 원하는 단일 변환을 나머지의 나머지 비트 (시스템 레지스터 라고 함)에 적용 합니다.  그러나 다른 모든 측정 결과는 실패를 야기 합니다.  명확한 진폭 증폭은 \\ 위의 이유를 사용 하 여이 측정의 성공 확률을 $100% $로 높일 수 있습니다.  또한 일반 진폭 증폭은 시스템 레지스터가 비어 있는 경우에 해당 합니다.  그 이유는 Q #에서 명확한 진폭 증폭을 기본 진폭 증폭 서브루틴으로 사용 하는 이유입니다.

일반 루틴 ( `AmpAmpObliviousByReflectionPhases` )에는 및를 호출 하는 레지스터가 두 개 있습니다 `ancillaRegister` `systemRegister` . 또한 필요한 반사에 대해 두 개의 oracles를 허용 합니다. 는 `ReflectionOracle` 두 레지스터를 공동으로 수행 하는 동안에만 작동 합니다 `ancillaRegister` `ObliviousOracle` . 에 대 한 입력은 `ancillaRegister` 첫 번째 리플렉션 operator $ \boldone-2P_1 $의-1 eigenstate로 초기화 되어야 합니다.

일반적으로 oracle은 계산 기준 $ \ket{0...0} $의 상태를 준비 합니다. 구현에서 `ancillaRegister` `flagQubit` 원하는 ancillas의 및 나머지를 제어 하는 1 개의 consistes ()입니다 `stateOracle` . 는 `stateOracle` `flagQubit` $ \ket $ 일 때 적용 됩니다 {1} .

또한 `StateOracle` `ObliviousOracle` 에 대 한 호출을 통해 리플렉션 대신 oracles를 제공할 수 있습니다 `AmpAmpObliviousByOraclePhases` .

앞에서 설명한 것 처럼 기존 진폭 증폭은 이러한 루틴의 특별 한 경우입니다. 여기서 `ObliviousOracle` 는 identity 연산자이 고 시스템의 비트 (즉, `systemRegister` 비어 있음)는 없습니다. 부분 반사를 위한 단계 (예: Grover 검색의 경우)를 얻으려면 함수를 `AmpAmpPhasesStandard` 사용할 수 있습니다. `DatabaseSearch.qs`Grover 알고리즘의 샘플 구현에 대해서는를 참조 하세요.

[G.H. Low, Chuang](https://arxiv.org/abs/1707.05391)에 설명 된 대로 단일 기능 비트 회전 단계를 리플렉션 연산자 단계와 연결 합니다. 사용 되는 고정 소수점 단계는 [low, Yoder 및 Chuang](https://arxiv.org/abs/1603.03996)단계와 함께 [Yoder, Low 및 Chuang](https://arxiv.org/abs/1409.3305) 에 자세히 설명 되어 있습니다.

배경의 경우 [표준 진폭 증폭](https://arxiv.org/abs/quant-ph/0005055) 에서 시작 하 여 [명확한 진폭 증폭](https://arxiv.org/abs/1312.1414) 을 소개 하 고, 마지막으로 [Low 및 Chuang](https://arxiv.org/abs/1610.06546)에 제공 된 일반화로 이동할 수 있습니다. Hamiltonian 시뮬레이션에 관련 된이 전체 영역에 대 한 유용한 개요는 [Dominic Berry](http://www.dominicberry.org/presentations/Durban.pdf)에 의해 제공 됩니다.

## <a name="quantum-fourier-transform"></a>퀀텀 푸리에 변환 ##

푸리에 변환은 기존 분석의 기본 도구로 서, 퀀텀 계산의 경우에만 중요 합니다.
또한 qft ( *퀀텀 푸리에 변환* )의 효율성은 기존 컴퓨터에서 가능한 작업을 초과 퀀텀 알고리즘을 디자인할 때 선택한 첫 번째 도구 중 하나를 만들 수 있습니다.

QFT의 대략적인 일반화로, <xref:microsoft.quantum.canon.approximateqft> 원하는 알고리즘 정확도에 꼭 필요 하지 않은 회전을 정리 하 여 추가 최적화를 허용 하는 작업을 제공 합니다.
대략적인 QFT는 dyadic $Z $-rotation 작업 뿐만 아니라 <xref:microsoft.quantum.intrinsic.rfrac> 작업을 필요로 합니다 <xref:microsoft.quantum.intrinsic.h> .
입력 및 출력은 big endian 인코딩---인코딩된 것으로 간주 됩니다. 즉, 인덱스가 있는 이상 비트는 `0` 이진 정수 표현의 맨 왼쪽 (가장 높은 비트)으로 인코딩됩니다.
이는 [k 표기법](xref:microsoft.quantum.concepts.dirac)에 맞게 정렬 됩니다. $ \ket $q $ 상태에 있는 세 가지의 레지스터는 $ {100} \ket $ 상태에 있으며, {1} $q _1 $ 및 $q _2 $은 모두 state $ \ket {0} $입니다.
근사값 매개 변수 $a $는 $Z $-회전 (예: $a \in [0 ... n] $)의 정리 수준을 결정 합니다.
이 경우 $ $k > $-회전 $2\ pi/2 ^ k $ $Z QFT 회로에서 제거 됩니다.
$K \ge \ log_2 (n) + \ log_2 (1/\ge) + $3에 대해 알려져 있습니다. 하나는 $ \\ | \operatorname{QFT}-\operatorname{AQFT} \\ | < \epsilon $에 바인딩될 수 있습니다.
여기서 $ \\ | \cdot \\ | $는이 경우 $ (\Operatorname{QFT}-\operatorname{AQFT}) (\Operatorname{QFT}-\operatorname{AQFT}) ^ \ $의 가장 큰 [eigenvalue](xref:microsoft.quantum.concepts.matrix-advanced) 의 제곱근에 해당 하는 일반적인 연산자입니다.

## <a name="arithmetic"></a>산술 ##

산술 연산은 기존 컴퓨팅에서 중앙 역할을 수행 하는 것과 마찬가지로 퀀텀 컴퓨팅 에서도 필수적인 역할을 합니다.  Shor의 팩터링 알고리즘, 퀀텀 시뮬레이션 메서드 및 많은 oracular 알고리즘 등의 알고리즘은 일관 된 산술 연산을 사용 합니다.  대부분의 산술 방식은 퀀텀 adder 회로를 기반으로 작성 됩니다.  가장 간단한 adder는 기존 입력 $b $를 사용 하 고 정수 $ \ket{a} $를 보유 하는 퀀텀 상태에 값을 추가 합니다.  수학적으로 adder (기존 입력 $b $의 $ \operatorname{Add} (b) $)에는 속성이 있습니다.

$ $ \operatorname{Add} (b) \ket{a} = \ket{a + b}.
$ $이 기본 adder 회로는 adder 보다 incrementer입니다.
$ $ \Operatorname{Add}\ket{a}\ket{b} = \ket{a}\ket{a + b}, $ $n $를 통해 두 개의 퀀텀 입력을 포함 하는 adder로 변환 될 수 있습니다. \begin{align} \operatorname{Add} \ket{a} \ket{b} & = \Lambda \_ {a \_ 0} \lambda (\operatorname{Add} (1) \lambda) \lambda (1) \lambda) \lambda \_ {a \_ 1} \ left (\operatorname{Add} (2) \Lambda) \lambda \_ {a \_ 2} \lambda (\operatorname{Add} (4) \Lambda) \cst\\operatorname{Add} ({{n-1}} \_ \_ ) \lambda (({{1}}) \lambda) \ket{a}\ket{b} \\ \\ & = \ket{a} \ket{b + a}, $n $ bit 정수 $a $ 및 $b $ 및 더하기 모듈로 $2 ^ n $에 대 한 \end{align}.  $ \Lambda \_ x (A) $ 표기법은 $와 같은 모든 $A 작업에 대해 $를 $x 사용 하 여 해당 작업의 제어 되는 버전을 제어 하는 것으로 간주 합니다.

이와 유사 하 게 제어 되는 일련의 제어 된 추가를 사용 하 여 일반적으로 제어 되는 곱하기 (Shor의 팩터링 알고리즘에 필수적인 모듈식 형태)를 수행할 수 있습니다. \begin{align} \operatorname{Mult} (a) \ket{x}\ket{b} & = \Lambda \_ {x \_ 0} \Lambda (\operatorname{Add} (2 ^ 0 a) \lambda) \lambda (2 ^ 0 a) \lambda) \lambda (2 ^ \_ \_ 1a) \lambda) \lambda \_ {a \_ 2} \lambda (\operatorname{Add} (2 ^ 2 a) \Lambda) \c도트 \lambda \_ {x \_ {n-1}} \lambda (\operatorname{Add} ({2 ^ {n-1}} a) \lambda) \ket{x}\ket{b} \\ \\ & = \ket{x}\ket{b + ax}.
\end{align}는 위의 $ \operatorname{Mult} $ 정의에서 확인할 수 있는, 퀀텀 컴퓨터에 대 한 곱셈 미묘한 있습니다.  이와 달리이 회로의 퀀텀 버전은 입력 레지스터가 아니라 보조 레지스터에 입력 제품을 저장 합니다.  이 예제에서 레지스터는 $b 값을 사용 하 여 초기화 되지만 일반적으로 값 0을 유지 하기 시작 합니다.  일반적으로 일반 $a $ 및 $x $에 대 한 곱하기 역이 아니기 때문에이는에 필요 합니다.  모든 퀀텀 작업, 측정 저장은 해독 가능 하므로 곱하기를 반전 하기 위한 충분 한 정보를 유지 해야 합니다.  이러한 이유로 결과가 별도의 배열에 저장 됩니다.  곱하기와 같이, 되돌릴 수 없는 작업의 출력을 별도의 레지스터에 저장 하는이 트릭은 Chartwnett가 있는 "배치 Nett 트릭" 이라고 하며,이는 되돌릴 수 있는 작업과 퀀텀 컴퓨팅 모두에서 기본 도구입니다.

많은 퀀텀 회로는 추가를 위해 제안 되었으며 각각은 필요한 게이트 비트 (공간)의 수와 필요한 게이트 작업 (시간)의 수를 기준으로 다른 균형을 탐색 합니다.  Draper adder 및 Beauregard adder 이라는 두 개의 매우 효율적인 공간 효율적인 adder를 검토 합니다.

### <a name="draper-adder"></a>Draper Adder ###

Draper adder는 추가를 수행 하기 위해 퀀텀 속성을 직접 호출 하기 때문에 가장 세련 된 퀀텀 항목 중 하나입니다.  Draper adder에 대 한 통찰력은 푸리에 변환을 사용 하 여 위상 이동을 비트 시프트로 변환할 수 있다는 것입니다.  그런 다음 푸리에 변환을 적용 하 고 적절 한 단계를 적용 한 다음 푸리에 변환을 실행 취소 하 여 adder를 구현할 수 있습니다.  제안 된 다른 많은 adder와는 달리 Draper adder는 퀀텀 푸리에 변환을 통해 도입 된 퀀텀 효과를 명시적으로 사용 합니다.  자연 스러운 기존 항목이 없습니다.  Draper adder의 특정 단계는 다음과 같습니다.

$ 및 $b $a $ $a 정수를 저장 하는 두 개의 $n $ $ $ \operatorname{QFT}\ket{a} = \frac {1} {\sqrt{2 ^ n}} \sum \_ {j = 0} ^ {2 ^ n-1} e ^ {i2\pi (aj)/2 ^ n} \ket{j}.를 저장 한다고 가정 합니다.
$ $ $ $ \Ket{\phi \_ k (a)} = \frac {1} {\sqrt {2} } \left (\ket {0} + e ^ {i2\pi a/2 ^ k} \ket {1} \right)를 정의 하는 경우 $ $는 일부 대 수 후 $ $ \operatorname{QFT}\ket{a} = \ket{\phi \_ 1 (a)} \frac \co\otime \ket{\phi \_ n (a)}을 확인할 수 있습니다.
$ $ Adder를 수행 하는 경로는 입력의 합계가 $ $ \ket{a + b} = \operatorname{QFT} ^ {-1} \ket{\phi \_ 1 (a + b)} \otimes \cst\otimes \ket{\phi \_ n (a + b)}으로 작성 될 수 있다는 것을 관찰 한 후에 분명 하 게 드러납니다.
$ $ $B $ 및 $a $ 정수는 $b $의 비트를 컨트롤로 사용 하 여 분해의 각 성능에서 제어 단계 회전을 수행 하 여 추가할 수 있습니다.

이 확장은 정수 $j $ 및 실수 $x $, $e ^ {i2\pi (x + j)} = e ^ {i2\pi x} $에 대 한 것을 확인할 수 있습니다.  이는 원에서 $360 ^ {\circ} $ degrees ($ 2 \ pi $ 라디안)를 회전 하는 경우 시작 하는 위치에서 정확 하 게 종료 되기 때문입니다.  따라서 $e ^ {i2\pi x} $에 대 한 $x $의 유일한 중요 한 부분은 $ $x의 소수 부분입니다.  특히 $x = y +0 형식의 이진 확장이 있는 경우입니다. x \_ 0x \_ 2 \ ldots x \_ n $ 다음 $e ^ {i2\pi x} = e ^ {i2\pi (0. x \_ 0x \_ 2 \ ldots x \_ {n-1})} $이 고 $ $ \ket{\phi k \_ (a + b)} = \frac { {1} \sqrt} {2} \left (\ket + {0} e ^ {i2\pi [a/2 ^ k +0)입니다. b. \_ k\ldots b 1 \_ ]} \ket {1} \Right). $ $ 즉, $ \ket{a} $의 푸리에 변형 확장에서 각 텐서 요소를 증가 시켜 추가를 수행 하는 경우에는 회전 횟수가 $ 감소할 때 축소 됩니다. $k  이렇게 하면 adder에 필요한 퀀텀 게이트 수가 크게 줄어듭니다.  Draper adder를 $ \operatorname{QFT} ^ {-1} \left ( \\ \\\Operatorname{ADD}\right) \operatorname{QFT} $로 구성 하는 푸리에 변환, 단계 덧셈 및 역 푸리에 변환 단계를 나타냅니다 \! . 이 단순화를 사용 하 여 전체 프로세스를 구현 하는 퀀텀 회로는 아래에서 볼 수 있습니다.

![회로 다이어그램으로 표시 된 Draper adder](~/media/draper.svg)

회로에서 제어 되는 각 $e ^ {i2 \ pi/k} $ gate는 제어 단계 게이트를 나타냅니다.  이러한 게이트는 작동 하는 stbits 쌍에 해당 하는 속성을 가집니다. $ \ket {00} \maps\ket {00} $ 하지만 $ \ket {11} \mapse ^ {i2 \ pi/k} \ k {11} $입니다.  이 회로를 사용 하면 입력 및 출력을 저장 하는 데 필요한 것과는 별도로 추가 기능을 사용 하 여 추가 기능을 수행할 수 있습니다.

### <a name="beauregard-adder"></a>Beauregard Adder ###

Beauregard adder는 Draper adder를 사용 하는 퀀텀 모듈식 adder는 임의의 값 양의 정수 $N $에 대해 더하기 모듈로 $N $를 수행 하는 데 사용 됩니다.  Beauregard adder와 같은 퀀텀 모듈형 adders의 중요 한 것은 인수를 팩터링 하기 위해 Shor의 알고리즘 내에서 모듈형 지 수 단계에서 사용 하는 것과 다를 수 있습니다.  퀀텀 모듈식 adder는 퀀텀 입력 $ \ket{b} $ 및 클래식 입력 $a $에 대해 다음과 같은 작업을 수행 합니다. 여기에서 $a $ 및 $b $은 정수 mod $N $로 약속 됩니다.

$ $ \ket{b}\rightarrow \ket{b + a \text{mod} N} = \begin{cases} \ket{b + a}, & b + a < N \\ \\ \ket{b + a-n}, & (b + a) \Ge N \end{cases}.
$$

Beauregard adder는 Draper adder 또는 보다 구체적으로 $ \\a\operatorname{ADD} $를 사용 하 여 \\ \! 단계에서 $ 및 $b $ $a를 추가 합니다.  그런 다음 동일한 작업을 사용 하 여 $a + b <N $ $N $를 뺀 다음 $a + b-N<$0 인지 테스트 합니다.  회로는이 정보를 보조 비트에 저장 한 다음 $a + b<N $ 인 경우 레지스터 $N $ back 추가 합니다.  그런 다음이 보조 비트를 계산 하 여 종료 합니다. (이 단계는 adder를 호출한 후 ancilla를 할당 취소할 수 있도록 하기 위해 필요 합니다.)  Beauregard adder에 대 한 회로는 아래에 제공 됩니다.

![회로 다이어그램으로 표시 된 Beauregard adder](~/media/beau.svg)

여기서 $ \\ \! \S\operatorname{ADD} $은 $ \\A\operatorname{ADD} $와 동일한 형식을 사용 합니다 \\ \! . 단,이 컨텍스트에서는 입력이 퀀텀이 아닌 고전입니다.  이를 통해 $ \\\Operatorname{ADD} $의 제어 된 단계가 \\ \! 단계 게이트로 대체 될 수 있습니다. 그러면 adder에 필요한 수와 게이트 수를 모두 줄이기 위해 작업 수가 줄어듭니다.

자세한 내용은 [Coppersmith 및 D.](https://arxiv.org/abs/quant-ph/0201067)n e [M.](http://doi.org/10.1007/s00200-008-0072-2 ) n e D.

### <a name="quantum-phase-estimation"></a>양자 단계 예측 ###

퀀텀 푸리에 변환의 특히 중요 한 응용 프로그램은 단일 연산자의 고유 값를 학습 하는 것입니다. 여기에는 *단계 예측*이라고 알려진 문제가 있습니다.
단일 $U $ 및 상태 $ \ket{\phi} $를 고려해 보세요. $ \ket{\phi} $은 알 수 없는 eigenstate $ \a$, \begin{nation} U\ket {\ l} = \phi\ket{\phi}. $U의 eigenstate입니다.
\end{equation} oracle as $U에만 액세스할 수 있는 경우 제어 되는 작업의 대상에 적용 된 $ 회전이 컨트롤에 다시 전파 되는 $Z를 활용 하 여 $ \\a$ 단계를 배울 수 있습니다.

$V $는 $U $의 제어 된 응용 프로그램입니다 .이 응용 프로그램은 \begin{align} V (\ket {0} \otimes \ket{\phi}) & = \ket {0} \otimes \ket{\phi} \\ \\ \textrm{and} V (\ket {1} \otimes \ket{\phi}) & = e ^ {i \phi} \ket {1} \otimes \ket{\phi}.
그런 다음 \end{align}, \begin{align} V (\ket{+} \otimes \ket{\phi}) & = \frac{(\ket {0} \otimes \ket{\phi}) + e ^ {i \phi} (\ket {1} \otimes \ket{\phi})} {\sqrt}를 입력 {2} 합니다.
\end{align} \begin{align} V (\ket{+} \otimes \ket{\phi}) & = \frac{\ket {0} + e ^ {i \phi} \ket {1} } {\sqrt {2} } \otimes \ket{\phi} \\ \\ & = (R_1 (\emi\ket{) \ket{\phi} +}) \otimes \end{align}, where ($R _1 $은 작업에서 적용 한 단일 <xref:microsoft.quantum.intrinsic.r1> 항목)를 찾는 용어를 수집할 수 있습니다.
$V $를 적용 하는 효과는 oracle로 $V $에만 액세스할 수 있는 경우에도 $R _1 $를 알 수 없는 각도로 적용 하는 것과 정확 하 게 동일 합니다.
따라서이 문서의 나머지 부분에서는 *kickback 단계*를 사용 하 여 구현 하는 $R _1 (\\ax) $을 기준으로 단계 예측에 대해 설명 합니다.

이 프로세스를 수행한 후에는 컨트롤과 대상 레지스터가 untangled 상태로 남아 있으므로 $ \ket{\phi} $를 $U ^ $2의 제어 되는 응용 프로그램의 대상으로 사용 하 여 $R _1 (2 \phi) \ket{+} $ 상태에서 두 번째 컨트롤을 준비할 수 있습니다.
이러한 방식으로 계속 하 여 \begin{align} \ket{\psi} & = \ sum_ {j = 0} ^ n R_1 (2 ^ j \as) \ket{+} \\ \\ & \propto \ bigotimes_ {j = 0} ^ {n} \phi (\ket + \phi) 형식의 등록을 가져올 수 있습니다. {0} (i 2 ^ {j} \\\ket) {1} \\ \\ & \propto \ sum_ {k = 0} ^ {2 ^ n-1} \phi (\\aak) \ket{k} \end{align} 여기서 $n $은 필요한 전체 자릿수의 비트 수입니다. $ {} \propto {} $를 사용 하 여 $1/\sqrt{2 ^ n} $의 정규화 요소를 표시 하지 않았음을 나타낼 수 있습니다.

정수 $p $에 대해 $ \phi = 2 \phi p/2 ^ k $를 사용할 경우 $ \ket{\psi} = \operatorname{QFT} \ket{p_0 p_1 \phi} $로 인식 됩니다. 여기서 $p _j $은 $j ^ {\textrm{th}} $ 비트가 $2 \phi \phi n $입니다.
따라서 퀀텀 푸리에 변환의 adjoint를 적용 하면 퀀텀 상태로 인코딩된 단계의 이진 표현을 가져옵니다.

Q #에서이 <xref:microsoft.quantum.characterization.quantumphaseestimation> 작업은 <xref:microsoft.quantum.oracles.discreteoracle> $U ^ m $을 구현 하는 응용 프로그램을 양의 정수의 함수로 사용 하는 작업에 의해 구현 됩니다 $m $.
