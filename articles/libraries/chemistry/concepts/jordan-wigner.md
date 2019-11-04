---
title: 요르단-Wigner 표현 | Microsoft Docs
description: 요르단-Wigner 표현의 개념 문서
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.jordanwigner
ms.openlocfilehash: f34233bc17ff68a9e04256959f8d79be2682c34f
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/26/2019
ms.locfileid: "73184052"
---
# <a name="jordan-wigner-representation"></a>요르단-Wigner 표현

두 번째 양자화 Hamiltonians는 $a ^ \aa$ (만들기)와 $a $ (annihilation) 측면에서 편리 하 게 표현 되지만, 이러한 작업은 퀀텀 컴퓨터에서 기본적인 작업이 아닙니다.
따라서 퀀텀 컴퓨터에서 구현 하려는 경우에는 퀀텀 컴퓨터에서 구현 될 수 있는 단일 행렬에 연산자를 매핑해야 합니다.
요르단 – Wigner 표현은 이러한 맵 하나를 제공 합니다.
그러나 Bravyi – Kitaev 표현과 같은 다른 사용자에 게는 고유한 장점과 단점이 있습니다.
Wigner 표현의 주요 이점은 간단 합니다.

Wigner 표현은 파생 시킬 직선입니다.
상태 $ \ket{0}_j $는 spin 궤도 $j $가 비어 있고 $ \ket{1}_j $가 이미 있음을 의미 합니다.
즉,이는 기본적으로 지정 된 spin 궤도의 직업을 저장할 수 있습니다.
그런 다음 $a ^ \dagger_j \ket{0}_j = \ket{1}_j $ 및 $a ^ \dagger_j \ket{1}_j = $0입니다.
\Begin{align} a ^ \dagger_j & = \begin{bmatrix}0 & 1 \\\ 0 & 0 \end{bmatrix} = \frac{X_j + iY_j}{2}, \nonumber\\\\ a_j & = \begin{bmatrix}0 & 0 \\\ 1 & 0 \end{와 같이 쉽게 확인할 수 있습니다. bmatrix} = \frac{X_j-iY_j}{2}, \end{align} 여기서 $X _j $ 및 $Y _j $는 Pabit $Y $에서 작동 하는 Pauli $X $ 및-$j $ 연산자입니다.
이는 단일 스핀 궤도의 경우 퀀텀 컴퓨터에서 인식 하는 단일 행렬을 기준으로 만들기 및 annihilation 연산자를 쉽게 나타낼 수 있음을 보여 줍니다.
$X $ 및 $Y $는 단일 $a ^ \aa$ 및 $a $는 그렇지 않습니다.
나중에이 문제를 시뮬레이션 하는 데 문제가 발생 하지 않는다는 것을 알 수 있습니다.

한 가지 문제는 위의 구성이 단일 스핀 궤도에 대해 작동 하는 동안 두 개 이상의 spin orbitals를 포함 하는 시스템에 대해 실패 한다는 것입니다.
Fermions는 antisymmetic 이기 때문에 $j $ 및 $k $에 대해 ^ \dagger_j a ^ \dagger_k =-a ^ \dagger_k a ^ \dagger_j $를 $a 합니다.
그러나 $ $ \left (\frac{X_j-iY_j}{2}\left) \left (\frac{X_k-iY_k}{2}\left) = \left (\frac{X_k-iY_k}{2}\left) \left (\frac{X_j-iY_j}{2}\left).
$ $ 즉, 두 개의 생성 연산자는 필요에 따라 commute 되지 않습니다.
이는 inelegant 경우에만 간단 하 게 해결할 수 있습니다.
이 문제를 해결 하기 위해 Pauli 연산자는 자연스럽 게 commute.
특히 $XZ =-ZX $ 및 $YZ =-ZY $입니다.
따라서 $Z $ operators를 연산자 생성으로 interspersing 하 여 올바른 통신를 에뮬레이트할 수 있습니다.
전체 구성은 다음과 같습니다. 

\begin{align} a ^ \dagger_1 & = \left (\frac{X-iY}{2}\left) \otimes 1 \osts 1 \otimes 1 \otimes 1 \oatime 1,\\\\ ^ \dagger_2 & = Z\otimes\left (\frac{X-iY}{2}\left) \otime 1 \otimes 1 \otime 1 ,\\\\ ^ \dagger_3 & = Z\otimes Z\otimes \stststst\o{2}\frac{X-iY} 1,\\\\ & \v도트\\\\ a ^ \dagger_N & = Z\otimes z\otimes Z \otimes \cst\otimes Z\otimes \left (\frac{X-iY}{2}\right). \label{eq: JW} \end{align}

또한 Pauli 연산자를 기준으로 number 연산자, $n _j $를 표현 하는 것이 편리 합니다.
다행히 $ operators (Wigner 문자열 이라고 함) $Z 문자열이 취소 된 후이를 대체 합니다.
이를 수행 하 고 $X _jY_j = iZ_j $)을 회수 한 후에는 \begin{st} n_j = a ^ \dagger_j a_j = \frac{(1-Z_j)}{2}있습니다.
\end{equation}


## <a name="constructing-hamiltonians-in-jordan-wigner-representation"></a>Wigner 표현의 Hamiltonians 생성

Wigner 표현을 호출 하 고 나면 Hamiltonian를 Pauli 연산자의 합계로 변환 합니다.
Fermionic Hamiltonian의 각 $a ^ \dagger $ 및 $a $ 연산자를 위에서 지정 된 Pauli 연산자 문자열로 바꾸어야 합니다.
이 대체를 수행 하는 경우 Hamiltonian 내에는 5 개의 용어만 있습니다.
이러한 다섯 가지 클래스는 Hamiltonian의 한 본문에서 $p q $ 및 $p, q, r, s $를 선택할 수 있는 다양 한 방법에 해당 합니다.
이러한 다섯 가지 클래스는 $p > q > r > s $ 및 실제 값 orbitals 인 경우

\begin{align} h_ {pp} a_p ^ \dagger & = \sum_r\frac{h_{pp}}{2}(1-Z_p)\\\\ h_ {pq} (a_p ^ \dagger \dagger_q + a ^ a_p \frac{h_{pq}}) & = \prod_{j{2}\dagger (Z_j = q + 1} ^ {p-1} \dagger) \ left (X_pX_q + Y_pY_q\right)\\\\ h_ {pqqp} n_p n_q & = \frac{h_{pqqp}}{4}\left (1-Z_p-Z_q + Z_pZ_q \left)\\\\ H_ {pqqr} & = \frac{h_{pqqr}}{2}\left (\prod_{j = r + 1} ^ {p-1} Z_j \right) \right (X_pX_r + Y_pY_r\right) \right (\frac{1-Z_q}{2}\right)\\\\ H_ {pqrs} & = \frac{h_{pqrs}}{8}\prod_{j = s + 1} ^ {r-1} Z_j\prod_ {k = q + 1} ^ {p-1} Z_k \Right (XXXX-XXYY + XYXY\nonumber\\\\ & \qquad\qquad\qquad\qquad\qquad + YXXY + YXYX-YYXX\nonumber\\\\ & \qquad\qquad\qquad\qquad\qquad + XYYX + YYYY\Big) \end{align}

이러한 Hamiltonians을 직접 생성 하는 경우에만 이러한 교체 규칙을 적용 해야 하지만,이 작업을 수행 하는 경우 수백만 개의 Hamiltonian 용어로 구성 될 수 있는 large molecules은 불가능 합니다.
또는 Hamiltonian의 `FermionHamiltonian` 표현을 제공 하 여 `JordanWignerEncoding`를 자동으로 생성할 수 있습니다.

```csharp
    // We load the namespace containing fermion and Pauli objects. 
    using Microsoft.Quantum.Chemistry.Fermion;
    using Microsoft.Quantum.Chemistry.Pauli;
    
    // We create an example `FermionHamiltonian` instance.
    var fermionHamiltonian = new FermionHamiltonian();

    // We convert this Fermion Hamiltonian to a Jordan-Wigner representation.
    var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(QubitEncoding.JordanWigner);
```

Hamiltonians이 형식으로 생성 되 면 퀀텀 시뮬레이션 알고리즘의 호스트를 사용 하 여 $e ^ {-iHt} $에 의해 생성 된 dynamics를 일련의 기본 게이트 (일부 사용자 정의 가능한 오류 허용 범위 내)로 컴파일할 수 있습니다.
알고리즘 설명서에서 퀀텀 시뮬레이션에 대 한 가장 인기 있는 두 가지 메서드인 Trotter – Suzuki 수식을 설명 합니다. Hamiltonian 시뮬레이션 라이브러리의 두 메서드에 대 한 구현을 제공 합니다.
