---
title: 양자 오라클
description: 다른 알고리즘의 입력으로 사용 되는 퀀텀 oracles 블랙 박스 작업을 사용 하 고 정의 하는 방법에 대해 알아봅니다.
author: cgranade
uid: microsoft.quantum.concepts.oracles
ms.author: Christopher.Granade@microsoft.com
ms.date: 07/11/2018
ms.topic: article
no-loc:
- $
- $
- $
- $
- $
- $
- '\cdots'
- bmatrix
- '\ddots'
- '\equiv'
- '\sum'
- '\begin'
- '\end'
- '\sqrt'
- '\otimes'
- '{'
- '}'
- '\text'
- '\phi'
- '\kappa'
- '\psi'
- '\alpha'
- '\beta'
- '\gamma'
- '\delta'
- '\omega'
- '\bra'
- '\ket'
- '\boldone'
- '\\\\'
- '\\'
- =
- '\frac'
- '\text'
- '\mapsto'
- '\dagger'
- '\to'
- "\begin{cases}"
- "\end{cases}"
- '\operatorname'
- '\braket'
- '\id'
- '\expect'
- '\defeq'
- '\variance'
- '\dd'
- '&'
- "\begin{align}"
- "\end{align}"
- '\Lambda'
- '\lambda'
- '\Omega'
- '\mathrm'
- '\left'
- '\right'
- '\qquad'
- '\times'
- '\big'
- '\langle'
- '\rangle'
- '\bigg'
- '\Big'
- '|'
- '\mathbb'
- '\vec'
- '\in'
- '\texttt'
- '\ne'
- <
- '>'
- '\leq'
- '\geq'
- ~~
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- '\_'
ms.openlocfilehash: 747c08df110f1f10efe552628d15e3500509b690
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85269561"
---
# <a name="quantum-oracles"></a>퀀텀 Oracles

Oracle $O는 $ 다른 알고리즘에 대 한 입력으로 사용 되는 "블랙 박스" 작업입니다.
일반적으로 이러한 작업은 $f 기존 함수를 사용 하 여 정의 됩니다. \\ {0, 1 \\ } ^ n \to \\ {0, 1 \\ } ^ m $ $n $ 비트 이진 입력을 사용 하 고 $m $ 비트 이진 출력을 생성 합니다.
이렇게 하려면 특정 이진 입력 $x = (x_ {0 } , x_ {1 } , \dots, x_ {n-1) $를 고려 하십시오 } .
Stbit 상태를 $ \ket { \vec{x } } = \ket{x_ {0 } } \otimes \ket{x_ {1 } } \otimes \cst\otimes \ket{x_ {n-1 } } $로 레이블을 지정할 수 있습니다.

$ \ket {X } = \ket{f (x)} $를 $O 하기 위해 먼저 $O를 정의할 수 있지만 여기에는 몇 가지 문제가 있습니다.
첫째, $f는 $ 다른 크기의 입력 및 출력 ($n \ne m)을 가질 수 있습니다 $ .이 경우 $O를 적용 하면 레지스터의 원하는 $ 비트 수가 변경 됩니다.
둘째, $n = m 인 경우에도 $ 함수는 반전할 수 없습니다. 일부 $x \ne y에 대해 $f (x) = f (y) $ 이면 $ \ket {x } = O \ket {y } $ 이지만 $O ^ \aao { \ket x } \ne o ^ \aao { \ket y } $를 $O 합니다.
즉, adjoint $O 작업을 생성할 수 없고 $ oracles에 대해 adjoint를 정의 해야 합니다.

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a>계산 기준 상태에 영향을 미치는 oracle 정의
이러한 두 가지 문제를 해결할 수 있습니다. 이러한 문제는 $ 답변을 유지 하기 위해 두 번째 $m의 레지스터를 도입 하는 것입니다.
그런 다음 모든 계산 기반 상태에 oracle의 효과를 정의 합니다. 모든 $x \in \\ {0, 1 \\ } ^ n $ 및 $y \in \\ {0, 1 \\ } ^ m $ ,

$ $ \begin{align}
    O (\ket{x } \otimes \ket{y } ) = \ket{x } \otimes \ket{y \otimes f (x)}.
\end{align}
$$

이제는 생성을 통해 $O = O ^ \dagger 모양으로 $ 되어 있으므로 이전 문제를 모두 해결 했습니다.

> [!TIP]
> $O = O ^ {\dagger } l n $를 보려면 $O ^ 2 = \boldone $ $a부터 $ 모든 $a에 대 한 b = a, b \oplus b = a \{ \}
> 결과적으로 \ket{x } \ket{y \oplus f (x)} = \ket{x } \ket{y \oplus f (x) \oplus f (x)} = \ket{x } \ket{y $를 $O 합니다 } .

중요 한 것은 각 계산 기준 상태 $ \ket{x \ket{y $에 대해 oracle을 정의 } } 하는 것은 $ 다른 모든 상태에 대해 $O 작동 하는 방법을 정의 합니다.
이는 $ 모든 퀀텀 작업과 같이 작업을 수행 하는 상태에서 선형으로 수행 된다는 $O 점에서 즉시 수행 됩니다.
예를 들어 $H \ket{0 } = \ket { +} $ 및 $H \ket{1 } = \ket { -} $로 정의 된 Hadamard 작업을 고려 합니다.
$H $ 가 $ \ket +} $에서 작동 하는 방식을 알고 싶으면 { 이 $H를 선형으로 사용할 수 있습니다. $

$ $ \begin{align}
H \ket { +} & = \frac{1 } {\sqrt{2 } } H (\ket{0 } + \ket{1 } ) = \frac{1 } {\sqrt{2 } } (H \ket {0 } + H \ket {1 } ) \\ \\ & = \frac{1 } {\sqrt{2 } } (\ket + { } + \ket { -}) = \frac12 (\ket{0 } + \ket{1 } + \ket{0 } -\ket{1 } ) = \ket{0 } .
\end{align}
$$

Oracle $O를 정의 하는 경우에는 $ 모든 상태 $ \ket { \psi } $ on $n + m을 사용 하 여 다음 $ 으로 작성할 수 있습니다.

$ $ \begin{align}
\ket { \psi } & = \ sum_ {x \psi {0, \\ 1} \\ ^ n, y \psi \\ {0, 1 \\ } ^ m } \psi (x, y) \ket{x } \ket{y}
\end{align}
$$

여기서 $ \alpha: \\ {0, 1 \\ } ^ n \alpha \\ {0, 1 \\ } ^ m \alpha \mathbb{C } $는 state $ \ket \alpha $의 계수를 나타냅니다 { } . 그러므로

$ $ \begin{align}
O \ket { \psi } & = o \ sum_ {x \psi {0, 1} ^ \\ \\ n, y \psi { \\ 0, 1 \\ } ^ m } \psi (x, y) \ket{x } \ket{y } \\ \\ & = \ sum_ {x \psi \\ {0, 1 \\ } ^ n, y \psi \\ {0, 1 \\ } ^ m } \psi (x, y) O \ket{x } \ket{y } \\ \\ & = \ sum_ {x \psi {0, 1} ^ \\ \\ n, y \psi { \\ 0, 1 \\ } ^ m } \psi (x, y) \ket{x } \ket{y \oplus f (x)}.
\end{align}
$$

## <a name="phase-oracles"></a>Oracles 단계
또는 $ $ $O에 대 한 입력에 따라 _단계_ 를 적용 하 여 oracle $O로 $f을 인코딩할 수 있습니다 $ .
예를 들어 $ $ $ \begin{align과 같은 $O를 정의할 수 있습니다.}
    O \ket{x } = (-1) ^ {f (x)} \ket{x } .
\end{align}
$ $ 단계 oracle이 처음에 계산 기준 상태 $ \ket{x $로 등록에 대해 작동 하는 경우 } 이 단계는 전역 단계 이므로 관찰 가능 하지 않습니다.
그러나 이러한 oracle은 superposition에 적용 되거나 제어 된 작업으로 적용 되는 경우 매우 강력한 리소스가 될 수 있습니다.
예를 들어 $ $f 단일의 비트 함수에 대 한 단계 orcale $O _f을 고려 $ 합니다.
그런 다음 $ $ \begin{align}
    O_f \ket { +} & = O_f (\ket{0 } + \ket{1 } )/\sqrt{2 } \\ \\ & = ((-1) ^ {f (0)} \ket{0 } + (-1) ^ {f (1)} \ket{1 } )/\sqrt{2 } \\ \\ & = (-1) ^ {f (0)} (\ket{0 } + (-1) ^ {f (1)-f (0)} \ket{1 } )/\sqrt{2 } \\ \\ & = (-1) ^ {f (0)} Z ^ {f (0)-f (1)} \ket { +}.
\end{align}
$$

보다 일반적으로는 oracles의 두 뷰를 넓혔습니다 하 여 단일 비트만이 아닌 실수를 반환 하는 클래식 함수를 나타낼 수 있습니다.

Oracle을 구현 하는 가장 좋은 방법은 지정 된 알고리즘 내에서이 oracle을 사용 하는 방법에 따라 크게 달라 집니다.
예를 들어 [Deutsch-Jozsa 알고리즘](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) 은 첫 번째 방법으로 구현 된 oracle을 사용 하는 반면 [Grover의 알고리즘](https://en.wikipedia.org/wiki/Grover's_algorithm) 은 두 번째 방법으로 구현 된 oracle에 의존 합니다.


자세한 내용은 [Gilyén *et al*. 1711.00465](https://arxiv.org/abs/1711.00465)에 설명 되어 있습니다.
