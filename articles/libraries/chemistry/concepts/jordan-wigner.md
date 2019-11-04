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
# <a name="jordan-wigner-representation"></a><span data-ttu-id="ec1d2-103">요르단-Wigner 표현</span><span class="sxs-lookup"><span data-stu-id="ec1d2-103">Jordan-Wigner Representation</span></span>

<span data-ttu-id="ec1d2-104">두 번째 양자화 Hamiltonians는 $a ^ \aa$ (만들기)와 $a $ (annihilation) 측면에서 편리 하 게 표현 되지만, 이러한 작업은 퀀텀 컴퓨터에서 기본적인 작업이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-104">While second quantized Hamiltonians are conveniently represented in terms of $a^\dagger$ (creation) and $a$ (annihilation), these operations are not fundamental operations in quantum computers.</span></span>
<span data-ttu-id="ec1d2-105">따라서 퀀텀 컴퓨터에서 구현 하려는 경우에는 퀀텀 컴퓨터에서 구현 될 수 있는 단일 행렬에 연산자를 매핑해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-105">As a result, if we wish it implement them on a quantum computer we need to map the operators to unitary matrices that can be implemented on a quantum computer.</span></span>
<span data-ttu-id="ec1d2-106">요르단 – Wigner 표현은 이러한 맵 하나를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-106">The Jordan–Wigner representation gives one such map.</span></span>
<span data-ttu-id="ec1d2-107">그러나 Bravyi – Kitaev 표현과 같은 다른 사용자에 게는 고유한 장점과 단점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-107">However, others such as the Bravyi–Kitaev representation also exist and have their own relative advantages and disadvantages.</span></span>
<span data-ttu-id="ec1d2-108">Wigner 표현의 주요 이점은 간단 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-108">The main advantage of the Jordan-Wigner representation is its simplicity.</span></span>

<span data-ttu-id="ec1d2-109">Wigner 표현은 파생 시킬 직선입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-109">The Jordan-Wigner representation is straight forward to derive.</span></span>
<span data-ttu-id="ec1d2-110">상태 $ \ket{0}_j $는 spin 궤도 $j $가 비어 있고 $ \ket{1}_j $가 이미 있음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-110">Recall that a state $\ket{0}_j$ implies that spin orbital $j$ is empty and $\ket{1}_j$ implies that it is occupied.</span></span>
<span data-ttu-id="ec1d2-111">즉,이는 기본적으로 지정 된 spin 궤도의 직업을 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-111">This means that qubits can naturally store the occupation of a given spin orbital.</span></span>
<span data-ttu-id="ec1d2-112">그런 다음 $a ^ \dagger_j \ket{0}_j = \ket{1}_j $ 및 $a ^ \dagger_j \ket{1}_j = $0입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-112">We then have that $a^\dagger_j \ket{0}_j = \ket{1}_j$ and $a^\dagger_j \ket{1}_j = 0$.</span></span>
<span data-ttu-id="ec1d2-113">\Begin{align} a ^ \dagger_j & = \begin{bmatrix}0 & 1 \\\ 0 & 0 \end{bmatrix} = \frac{X_j + iY_j}{2}, \nonumber\\\\ a_j & = \begin{bmatrix}0 & 0 \\\ 1 & 0 \end{와 같이 쉽게 확인할 수 있습니다. bmatrix} = \frac{X_j-iY_j}{2}, \end{align} 여기서 $X _j $ 및 $Y _j $는 Pabit $Y $에서 작동 하는 Pauli $X $ 및-$j $ 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-113">It is easy to verify that \begin{align} a^\dagger_j &= \begin{bmatrix}0 & 1 \\\ 0 &0 \end{bmatrix}=\frac{X_j + iY_j}{2}, \nonumber\\\\ a_j &= \begin{bmatrix}0 & 0 \\\ 1 &0 \end{bmatrix}=\frac{X_j - iY_j}{2}, \end{align} where $X_j$ and $Y_j$ are the Pauli-$X$ and -$Y$ operators acting on qubit $j$.</span></span>
<span data-ttu-id="ec1d2-114">이는 단일 스핀 궤도의 경우 퀀텀 컴퓨터에서 인식 하는 단일 행렬을 기준으로 만들기 및 annihilation 연산자를 쉽게 나타낼 수 있음을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-114">This shows that for a single spin orbital it is easy to represent creation and annihilation operators in terms of unitary matrices that quantum computers understand.</span></span>
<span data-ttu-id="ec1d2-115">$X $ 및 $Y $는 단일 $a ^ \aa$ 및 $a $는 그렇지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-115">Note that while $X$ and $Y$ are unitary $a^\dagger$ and $a$ are not.</span></span>
<span data-ttu-id="ec1d2-116">나중에이 문제를 시뮬레이션 하는 데 문제가 발생 하지 않는다는 것을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-116">We will see later that this does not pose a challenge for simulation.</span></span>

<span data-ttu-id="ec1d2-117">한 가지 문제는 위의 구성이 단일 스핀 궤도에 대해 작동 하는 동안 두 개 이상의 spin orbitals를 포함 하는 시스템에 대해 실패 한다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-117">One problem that remains is that while the above construction works for a single spin orbital, it fails for systems with two or more spin orbitals.</span></span>
<span data-ttu-id="ec1d2-118">Fermions는 antisymmetic 이기 때문에 $j $ 및 $k $에 대해 ^ \dagger_j a ^ \dagger_k =-a ^ \dagger_k a ^ \dagger_j $를 $a 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-118">Since Fermions are antisymmetic, we know that $a^\dagger_j a^\dagger_k = - a^\dagger_k a^\dagger_j$ for any $j$ and $k$.</span></span>
<span data-ttu-id="ec1d2-119">그러나 $ $ \left (\frac{X_j-iY_j}{2}\left) \left (\frac{X_k-iY_k}{2}\left) = \left (\frac{X_k-iY_k}{2}\left) \left (\frac{X_j-iY_j}{2}\left).</span><span class="sxs-lookup"><span data-stu-id="ec1d2-119">However, $$ \left(\frac{X_j - iY_j}{2}\right)\left(\frac{X_k - iY_k}{2}\right) = \left(\frac{X_k - iY_k}{2}\right) \left(\frac{X_j - iY_j}{2}\right).</span></span>
<span data-ttu-id="ec1d2-120">$ $ 즉, 두 개의 생성 연산자는 필요에 따라 commute 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-120">$$ In other words, the two creation operators do not anti-commute as required.</span></span>
<span data-ttu-id="ec1d2-121">이는 inelegant 경우에만 간단 하 게 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-121">This can be remedied though in a straightforward, if inelegant fashion.</span></span>
<span data-ttu-id="ec1d2-122">이 문제를 해결 하기 위해 Pauli 연산자는 자연스럽 게 commute.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-122">The fix is to note that Pauli operators naturally anti-commute.</span></span>
<span data-ttu-id="ec1d2-123">특히 $XZ =-ZX $ 및 $YZ =-ZY $입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-123">In particular, $XZ = -ZX$ and $YZ=-ZY$.</span></span>
<span data-ttu-id="ec1d2-124">따라서 $Z $ operators를 연산자 생성으로 interspersing 하 여 올바른 통신를 에뮬레이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-124">Thus, by interspersing $Z$ operators into the construction of the operator, we can emulate the correct anti-commutation.</span></span>
<span data-ttu-id="ec1d2-125">전체 구성은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-125">The full construction is as follows:</span></span> 

<span data-ttu-id="ec1d2-126">\begin{align} a ^ \dagger_1 & = \left (\frac{X-iY}{2}\left) \otimes 1 \osts 1 \otimes 1 \otimes 1 \oatime 1,\\\\ ^ \dagger_2 & = Z\otimes\left (\frac{X-iY}{2}\left) \otime 1 \otimes 1 \otime 1 ,\\\\ ^ \dagger_3 & = Z\otimes Z\otimes \stststst\o{2}\frac{X-iY} 1,\\\\ & \v도트\\\\ a ^ \dagger_N & = Z\otimes z\otimes Z \otimes \cst\otimes Z\otimes \left (\frac{X-iY}{2}\right).</span><span class="sxs-lookup"><span data-stu-id="ec1d2-126">\begin{align} a^\dagger_1 &= \left(\frac{X-iY}{2}\right)\otimes 1 \otimes 1 \otimes 1 \otimes \cdots \otimes 1,\\\\ a^\dagger_2 &= Z\otimes\left(\frac{X-iY}{2}\right)\otimes 1\otimes 1 \otimes \cdots \otimes 1,\\\\ a^\dagger_3 &= Z\otimes Z\otimes \left(\frac{X-iY}{2}\right)\otimes 1 \otimes \cdots \otimes 1,\\\\ &\vdots\\\\ a^\dagger_N &= Z\otimes Z\otimes Z\otimes Z \otimes \cdots \otimes Z\otimes \left(\frac{X-iY}{2}\right).</span></span> <span data-ttu-id="ec1d2-127">\label{eq: JW} \end{align}</span><span class="sxs-lookup"><span data-stu-id="ec1d2-127">\label{eq:JW} \end{align}</span></span>

<span data-ttu-id="ec1d2-128">또한 Pauli 연산자를 기준으로 number 연산자, $n _j $를 표현 하는 것이 편리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-128">It is also convenient to express the number operators, $n_j$, in terms of Pauli operators.</span></span>
<span data-ttu-id="ec1d2-129">다행히 $ operators (Wigner 문자열 이라고 함) $Z 문자열이 취소 된 후이를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-129">Thankfully, the strings of $Z$ operators (known as Jordan-Wigner strings) cancel after one makes this substitution.</span></span>
<span data-ttu-id="ec1d2-130">이를 수행 하 고 $X _jY_j = iZ_j $)을 회수 한 후에는 \begin{st} n_j = a ^ \dagger_j a_j = \frac{(1-Z_j)}{2}있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-130">After carrying this out (and recalling that $X_jY_j=iZ_j$), we have \begin{equation} n_j = a^\dagger_j a_j = \frac{(1-Z_j)}{2}.</span></span>
<span data-ttu-id="ec1d2-131">\end{equation}</span><span class="sxs-lookup"><span data-stu-id="ec1d2-131">\end{equation}</span></span>


## <a name="constructing-hamiltonians-in-jordan-wigner-representation"></a><span data-ttu-id="ec1d2-132">Wigner 표현의 Hamiltonians 생성</span><span class="sxs-lookup"><span data-stu-id="ec1d2-132">Constructing Hamiltonians in Jordan-Wigner Representation</span></span>

<span data-ttu-id="ec1d2-133">Wigner 표현을 호출 하 고 나면 Hamiltonian를 Pauli 연산자의 합계로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-133">Once we have invoked the Jordan-Wigner representation translating the Hamiltonian to a sum of Pauli operators is straight forward.</span></span>
<span data-ttu-id="ec1d2-134">Fermionic Hamiltonian의 각 $a ^ \dagger $ 및 $a $ 연산자를 위에서 지정 된 Pauli 연산자 문자열로 바꾸어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-134">One simply has to replace each of the $a^\dagger$ and $a$ operators in the Fermionic Hamiltonian with the strings of Pauli-operators given above.</span></span>
<span data-ttu-id="ec1d2-135">이 대체를 수행 하는 경우 Hamiltonian 내에는 5 개의 용어만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-135">When one performs this substitution, there are only five classes of terms within the Hamiltonian.</span></span>
<span data-ttu-id="ec1d2-136">이러한 다섯 가지 클래스는 Hamiltonian의 한 본문에서 $p q $ 및 $p, q, r, s $를 선택할 수 있는 다양 한 방법에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-136">These five classes correspond to the different ways we can pick the $p,q$ and $p,q,r,s$ in the one-body and the two-body terms in the Hamiltonian.</span></span>
<span data-ttu-id="ec1d2-137">이러한 다섯 가지 클래스는 $p > q > r > s $ 및 실제 값 orbitals 인 경우</span><span class="sxs-lookup"><span data-stu-id="ec1d2-137">These five classes, for the case where $p>q>r>s$ and real-valued orbitals, are</span></span>

<span data-ttu-id="ec1d2-138">\begin{align} h_ {pp} a_p ^ \dagger & = \sum_r\frac{h_{pp}}{2}(1-Z_p)\\\\ h_ {pq} (a_p ^ \dagger \dagger_q + a ^ a_p \frac{h_{pq}}) & = \prod_{j{2}\dagger (Z_j = q + 1} ^ {p-1} \dagger) \ left (X_pX_q + Y_pY_q\right)\\\\ h_ {pqqp} n_p n_q & = \frac{h_{pqqp}}{4}\left (1-Z_p-Z_q + Z_pZ_q \left)\\\\ H_ {pqqr} & = \frac{h_{pqqr}}{2}\left (\prod_{j = r + 1} ^ {p-1} Z_j \right) \right (X_pX_r + Y_pY_r\right) \right (\frac{1-Z_q}{2}\right)\\\\ H_ {pqrs} & = \frac{h_{pqrs}}{8}\prod_{j = s + 1} ^ {r-1} Z_j\prod_ {k = q + 1} ^ {p-1} Z_k \Right (XXXX-XXYY + XYXY\nonumber\\\\ & \qquad\qquad\qquad\qquad\qquad + YXXY + YXYX-YYXX\nonumber\\\\ & \qquad\qquad\qquad\qquad\qquad + XYYX + YYYY\Big) \end{align}</span><span class="sxs-lookup"><span data-stu-id="ec1d2-138">\begin{align} h_{pp}a_p^\dagger a_p &= \sum_p \frac{h_{pp}}{2}(1 - Z_p)\\\\ h_{pq}(a_p^\dagger a_q + a^\dagger_q a_p) &= \frac{h_{pq}}{2}\left(\prod_{j=q+1}^{p-1} Z_j \right)\left( X_pX_q + Y_pY_q\right)\\\\ h_{pqqp} n_p n_q &=  \frac{h_{pqqp}}{4}\left(1-Z_p - Z_q +Z_pZ_q \right)\\\\ H_{pqqr} &= \frac{h_{pqqr}}{2}\left(\prod_{j=r+1}^{p-1} Z_j \right)\left( X_pX_r + Y_pY_r\right)\left(\frac{1-Z_q}{2}\right)\\\\ H_{pqrs} &= \frac{h_{pqrs}}{8}\prod_{j=s+1}^{r-1} Z_j\prod_{k=q+1}^{p-1} Z_k \Big(XXXX - XXYY+XYXY\nonumber\\\\ &\qquad\qquad\qquad\qquad\qquad+YXXY+YXYX-YYXX\nonumber\\\\ &\qquad\qquad\qquad\qquad\qquad+XYYX+YYYY\Big) \end{align}</span></span>

<span data-ttu-id="ec1d2-139">이러한 Hamiltonians을 직접 생성 하는 경우에만 이러한 교체 규칙을 적용 해야 하지만,이 작업을 수행 하는 경우 수백만 개의 Hamiltonian 용어로 구성 될 수 있는 large molecules은 불가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-139">While generating such Hamiltonians by hand only requires applying these replacement rules, doing so would be infeasible for large molecules which can consist of millions of Hamiltonian terms.</span></span>
<span data-ttu-id="ec1d2-140">또는 Hamiltonian의 `FermionHamiltonian` 표현을 제공 하 여 `JordanWignerEncoding`를 자동으로 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-140">As an alternative, we can automatically construct the `JordanWignerEncoding` given a `FermionHamiltonian` representation of the Hamiltonian.</span></span>

```csharp
    // We load the namespace containing fermion and Pauli objects. 
    using Microsoft.Quantum.Chemistry.Fermion;
    using Microsoft.Quantum.Chemistry.Pauli;
    
    // We create an example `FermionHamiltonian` instance.
    var fermionHamiltonian = new FermionHamiltonian();

    // We convert this Fermion Hamiltonian to a Jordan-Wigner representation.
    var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(QubitEncoding.JordanWigner);
```

<span data-ttu-id="ec1d2-141">Hamiltonians이 형식으로 생성 되 면 퀀텀 시뮬레이션 알고리즘의 호스트를 사용 하 여 $e ^ {-iHt} $에 의해 생성 된 dynamics를 일련의 기본 게이트 (일부 사용자 정의 가능한 오류 허용 범위 내)로 컴파일할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-141">Once the Hamiltonians are constructed in this form, we can use a host of quantum simulation algorithms to compile the dynamics generated by $e^{-iHt}$ into a sequence of elementary gates (within some user definable error tolerance).</span></span>
<span data-ttu-id="ec1d2-142">알고리즘 설명서에서 퀀텀 시뮬레이션에 대 한 가장 인기 있는 두 가지 메서드인 Trotter – Suzuki 수식을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-142">We discuss the two most popular methods for quantum simulation, qubitization and Trotter–Suzuki formulas, in the algorithmic documentation.</span></span> <span data-ttu-id="ec1d2-143">Hamiltonian 시뮬레이션 라이브러리의 두 메서드에 대 한 구현을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1d2-143">We provide implementations for both methods in the Hamiltonian simulation library.</span></span>
