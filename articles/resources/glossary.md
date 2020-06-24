---
title: 퀀텀 컴퓨팅 용어집
description: 퀀텀 컴퓨팅에 사용 되는 일반적인 용어, 작업 및 개체의 용어집입니다.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.glossary
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
ms.openlocfilehash: ba4d171d84d808f082b919dcc6156d9c65df7c05
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275366"
---
# <a name="quantum-computing-glossary"></a><span data-ttu-id="6006c-103">퀀텀 컴퓨팅 용어집</span><span class="sxs-lookup"><span data-stu-id="6006c-103">Quantum computing glossary</span></span>

## <a name="adjoint"></a><span data-ttu-id="6006c-104">Adjoint</span><span class="sxs-lookup"><span data-stu-id="6006c-104">Adjoint</span></span>

<span data-ttu-id="6006c-105">[작업](xref:microsoft.quantum.glossary#operation)의 복소수 복소수입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-105">The complex conjugate transpose of an [operation](xref:microsoft.quantum.glossary#operation).</span></span> <span data-ttu-id="6006c-106">[단일](xref:microsoft.quantum.glossary#unitary-operator) 연산자를 구현 하는 작업의 경우 adjoint는 작업의 역함수 이며 칼 기호로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-106">For operations that implement a [unitary](xref:microsoft.quantum.glossary#unitary-operator) operator, the adjoint is the inverse of the operation and is indicated by a dagger symbol.</span></span> <span data-ttu-id="6006c-107">예를 들어 연산이 `U` 단일 연산자 $U를 나타내는 경우은 $ (는) `Adjoint U` $U ^ \a 를 나타냅니다 $ .</span><span class="sxs-lookup"><span data-stu-id="6006c-107">For example, if the operation `U` represents the unitary operator $U$, then `Adjoint U` represents $U^\dagger$.</span></span> <span data-ttu-id="6006c-108">자세한 내용은 [Adjoint](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-108">For more information, see [Adjoint](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations).</span></span>

## <a name="ancilla"></a><span data-ttu-id="6006c-109">Ancilla</span><span class="sxs-lookup"><span data-stu-id="6006c-109">Ancilla</span></span>

<span data-ttu-id="6006c-110">퀀텀 컴퓨터의 임시 메모리로 사용 되며 필요에 따라 할당 및 할당 취소 되는 [기능입니다.](xref:microsoft.quantum.glossary#qubit)</span><span class="sxs-lookup"><span data-stu-id="6006c-110">A [qubit](xref:microsoft.quantum.glossary#qubit) that serves as temporary memory for a quantum computer and is allocated and de-allocated as needed.</span></span>  <span data-ttu-id="6006c-111">자세한 내용은 [여러 개의 추가 비트](xref:microsoft.quantum.concepts.multiple-qubits)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-111">For more information, see [Multiple qubits](xref:microsoft.quantum.concepts.multiple-qubits).</span></span>

## <a name="bell-state"></a><span data-ttu-id="6006c-112">종 상태</span><span class="sxs-lookup"><span data-stu-id="6006c-112">Bell state</span></span>

<span data-ttu-id="6006c-113">두 개의 최대 [entangled](xref:microsoft.quantum.glossary#entanglement) [퀀텀 상태](xref:microsoft.quantum.glossary#quantum-state) 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-113">One of four specific maximally [entangled](xref:microsoft.quantum.glossary#entanglement) [quantum states](xref:microsoft.quantum.glossary#quantum-state) of two qubits.</span></span> <span data-ttu-id="6006c-114">네 가지 상태는 $ \ket { \ beta_ {ij } } = (\mathbb{I } \Otimes X ^ iZ ^ j) (\ket{00 } + \ket{11 } )/\sqrt{2 $ } 로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-114">The four states are defined $\ket{\beta_{ij}} = (\mathbb{I} \otimes X^iZ^j) (\ket{00} + \ket{11}) / \sqrt{2}$.</span></span> <span data-ttu-id="6006c-115">종 상태는 [EPR 쌍](xref:microsoft.quantum.glossary#epr-pair)이 라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-115">A Bell state is also known as an [EPR pair](xref:microsoft.quantum.glossary#epr-pair).</span></span>

## <a name="bloch-sphere"></a><span data-ttu-id="6006c-116">Bloch 구</span><span class="sxs-lookup"><span data-stu-id="6006c-116">Bloch sphere</span></span>

<span data-ttu-id="6006c-117">3 차원 단위 구의 점으로 서 단일[비트](xref:microsoft.quantum.glossary#qubit) [퀀텀 상태](xref:microsoft.quantum.glossary#quantum-state) 를 그래픽으로 표현한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-117">A graphical representation of a single-[qubit](xref:microsoft.quantum.glossary#qubit) [quantum state](xref:microsoft.quantum.glossary#quantum-state) as a point in a three-dimensional unit sphere.</span></span> <span data-ttu-id="6006c-118">자세한 내용은 [Bloch 구를 사용 하 여 다양 한 비트 및 변형 시각화](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-118">For more information, see  [Visualizing Qubits and Transformations using the Bloch Sphere](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).</span></span>

## <a name="callable"></a><span data-ttu-id="6006c-119">호출</span><span class="sxs-lookup"><span data-stu-id="6006c-119">Callable</span></span>

<span data-ttu-id="6006c-120">Q # 언어의 [작업](xref:microsoft.quantum.glossary#operation) 또는 [함수](xref:microsoft.quantum.glossary#function) 입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-120">An [operation](xref:microsoft.quantum.glossary#operation) or [function](xref:microsoft.quantum.glossary#function) in the Q# language.</span></span> <span data-ttu-id="6006c-121">자세한 내용은 [작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-121">For more information, see [Operations and functions](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

## <a name="clifford-group"></a><span data-ttu-id="6006c-122">Clifford 그룹</span><span class="sxs-lookup"><span data-stu-id="6006c-122">Clifford group</span></span>

<span data-ttu-id="6006c-123">[Bloch 구의](xref:microsoft.quantum.glossary#bloch-sphere) octants을 차지 하는 작업 집합과 [pauli 연산자](xref:microsoft.quantum.glossary#pauli-operators)의 효과 순열</span><span class="sxs-lookup"><span data-stu-id="6006c-123">The set of operations that occupy the octants of the [Bloch sphere](xref:microsoft.quantum.glossary#bloch-sphere) and effect permutations of the [Pauli operators](xref:microsoft.quantum.glossary#pauli-operators).</span></span> <span data-ttu-id="6006c-124">여기에는 작업 [$X $ ](xref:microsoft.quantum.intrinsic.x), [$Y $ ](xref:microsoft.quantum.intrinsic.y), [$Z $ ](xref:microsoft.quantum.intrinsic.z), [$H $ ](xref:microsoft.quantum.intrinsic.h) 및 [$S $ ](xref:microsoft.quantum.intrinsic.s)가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-124">These include the operations [$X$](xref:microsoft.quantum.intrinsic.x), [$Y$](xref:microsoft.quantum.intrinsic.y), [$Z$](xref:microsoft.quantum.intrinsic.z), [$H$](xref:microsoft.quantum.intrinsic.h) and [$S$](xref:microsoft.quantum.intrinsic.s).</span></span>

## <a name="controlled"></a><span data-ttu-id="6006c-125">제어</span><span class="sxs-lookup"><span data-stu-id="6006c-125">Controlled</span></span>

<span data-ttu-id="6006c-126">대상 작업에 대 한 조력자로 하나 이상의 이상 [비트](xref:microsoft.quantum.glossary#qubit) 를 사용 하는 퀀텀 [작업](xref:microsoft.quantum.glossary#operation) 입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-126">A quantum [operation](xref:microsoft.quantum.glossary#operation) that takes one or more [qubits](xref:microsoft.quantum.glossary#qubit) as enablers for the target operation.</span></span> <span data-ttu-id="6006c-127">자세한 내용은 [제어 및 adjoint 작업](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-127">For more information, see [Controlled and adjoint operations](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations).</span></span>

## <a name="dirac-notation"></a><span data-ttu-id="6006c-128">기타 ac 표기법</span><span class="sxs-lookup"><span data-stu-id="6006c-128">Dirac Notation</span></span>

<span data-ttu-id="6006c-129">*Bra-k* 표기법이 라고도 하는 [퀀텀 상태의](xref:microsoft.quantum.glossary#quantum-state)표현을 간소화 하는 기호화 된 축약형입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-129">A symbolic shorthand that simplifies the representation of [quantum states](xref:microsoft.quantum.glossary#quantum-state), also called *bra-ket* notation.</span></span>  <span data-ttu-id="6006c-130">*Bra* 부분은 행 벡터를 나타냅니다. 예를 들어 $ \bra{A } = \begin{ bmatrix } a {_1 } & a {_2 } \end{ bmatrix } $ 및 *k* 부분은 열 벡터, $ \ket{B } = \begin{ bmatrix } B {_1 } \\ \\ B {_2 } \begin{ bmatrix } $를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-130">The *bra* portion represents a row vector, for example  $\bra{A} = \begin{bmatrix} A{_1} & A{_2} \end{bmatrix}$ and the *ket* portion represents a column vector, $\ket{B} = \begin{bmatrix} B{_1} \\\\ B{_2} \end{bmatrix}$.</span></span> <span data-ttu-id="6006c-131">자세한 내용은 [Diac 표기법](xref:microsoft.quantum.concepts.dirac)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6006c-131">For more information, see [Dirac Notation](xref:microsoft.quantum.concepts.dirac).</span></span>

## <a name="eigenvalue"></a><span data-ttu-id="6006c-132">Eigenvalue</span><span class="sxs-lookup"><span data-stu-id="6006c-132">Eigenvalue</span></span>

<span data-ttu-id="6006c-133">변환 응용 프로그램에서 지정 된 변환의 [eigenvector](xref:microsoft.quantum.glossary#eigenvector) 크기를 변경 하는 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-133">The factor by which the magnitude of an [eigenvector](xref:microsoft.quantum.glossary#eigenvector) of a given transformation is changed by the application of the transformation.</span></span>  <span data-ttu-id="6006c-134">사각형 행렬 $M $ 및 eigenvector $v를 지정 하 고 $ $Mv = cv를 지정 합니다 $ . 여기서 $c $ 은 eigenvalue 이며 임의의 인수 수 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-134">Given a square matrix $M$ and an eigenvector $v$, then $Mv = cv$, where $c$ is the eigenvalue and can be a complex number of any argument.</span></span> <span data-ttu-id="6006c-135">자세한 내용은 [고급 행렬 개념](xref:microsoft.quantum.concepts.matrix-advanced)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-135">For more information, see [Advanced matrix concepts](xref:microsoft.quantum.concepts.matrix-advanced).</span></span>

## <a name="eigenvector"></a><span data-ttu-id="6006c-136">Eigenvector</span><span class="sxs-lookup"><span data-stu-id="6006c-136">Eigenvector</span></span>

<span data-ttu-id="6006c-137">지정 된 변환에서 방향이 변경 되지 않으며 해당 벡터의 [eigenvalue](xref:microsoft.quantum.glossary#eigenvalue)에 해당 하는 요소에 의해 크기가 변경 되는 벡터입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-137">A vector whose direction is unchanged by a given transformation and whose magnitude is changed by a factor corresponding to that vector's [eigenvalue](xref:microsoft.quantum.glossary#eigenvalue).</span></span> <span data-ttu-id="6006c-138">사각형 행렬 $M $ 와 eigenvalue를 $c 한 $ 다음 $Mv = cv를 지정 $ $ 합니다. 여기서 $v은 행렬의 eigenvector이 고 임의의 인수 수 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-138">Given a square matrix $M$ and an eigenvalue $c$, then $Mv = cv$, where $v$ is an eigenvector of the matrix and can be a complex number of any argument.</span></span> <span data-ttu-id="6006c-139">자세한 내용은 [고급 행렬 개념](xref:microsoft.quantum.concepts.matrix-advanced)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-139">For more information, see [Advanced matrix concepts](xref:microsoft.quantum.concepts.matrix-advanced).</span></span>

## <a name="entanglement"></a><span data-ttu-id="6006c-140">얽힘</span><span class="sxs-lookup"><span data-stu-id="6006c-140">Entanglement</span></span>

<span data-ttu-id="6006c-141">다양 한 방식으로 개별적 [으로 설명할](xref:microsoft.quantum.glossary#qubit)수 없도록 하려는 경우에는 다양 한 것 *과 같은 퀀텀* 파티클을 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-141">Quantum particles, such as [qubits](xref:microsoft.quantum.glossary#qubit), can be connected or *entangled* such that they cannot be described independently from each other.</span></span> <span data-ttu-id="6006c-142">측정 결과는 무한정 떨어져 있는 경우에도 상관 관계가 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-142">Their measurement results are correlated even when they are separated infinitely far away.</span></span> <span data-ttu-id="6006c-143">되거나 얽 히는 해당 [상태](xref:microsoft.quantum.glossary#quantum-state) 를 [측정](xref:microsoft.quantum.glossary#measurement) 하는 데 필수적입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-143">Entanglement is essential to [measuring](xref:microsoft.quantum.glossary#measurement) the [state](xref:microsoft.quantum.glossary#quantum-state) of a qubit.</span></span>  <span data-ttu-id="6006c-144">자세한 내용은 [고급 행렬 개념](xref:microsoft.quantum.concepts.matrix-advanced)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-144">For more information, see [Advanced matrix concepts](xref:microsoft.quantum.concepts.matrix-advanced).</span></span>

## <a name="epr-pair"></a><span data-ttu-id="6006c-145">EPR 쌍</span><span class="sxs-lookup"><span data-stu-id="6006c-145">EPR pair</span></span>

<span data-ttu-id="6006c-146">두 개의 최대 entangled [퀀텀 상태](xref:microsoft.quantum.glossary#quantum-state) 중 [하나입니다.](xref:microsoft.quantum.glossary#qubit)</span><span class="sxs-lookup"><span data-stu-id="6006c-146">One of four specific maximally entangled [quantum states](xref:microsoft.quantum.glossary#quantum-state) of two [qubits](xref:microsoft.quantum.glossary#qubit).</span></span> <span data-ttu-id="6006c-147">네 가지 상태는 $ \ket { \ beta_ {ij } } = (\mathbb{1 } \Otimes X ^ iZ ^ j) (\ket{00 } + \ket{11 } )/\sqrt{2 $ } 로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-147">The four states are defined $\ket{\beta_{ij}} = (\mathbb{1} \otimes X^iZ^j) (\ket{00} + \ket{11}) / \sqrt{2}$.</span></span> <span data-ttu-id="6006c-148">EPR 쌍은 [종 상태](xref:microsoft.quantum.glossary#bell-state) 라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-148">An EPR pair is also known as a [Bell state](xref:microsoft.quantum.glossary#bell-state)</span></span>

## <a name="evolution"></a><span data-ttu-id="6006c-149">진화</span><span class="sxs-lookup"><span data-stu-id="6006c-149">Evolution</span></span>

<span data-ttu-id="6006c-150">시간이 지남에 따라 [퀀텀 상태](xref:microsoft.quantum.glossary#quantum-state) 를 변경 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-150">How a [quantum state](xref:microsoft.quantum.glossary#quantum-state) changes over time.</span></span> <span data-ttu-id="6006c-151">자세한 내용은 [Matrix 지 수](xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials)을 (를) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-151">For more information, see [Matrix exponentials](xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials).</span></span>

## <a name="function"></a><span data-ttu-id="6006c-152">기능</span><span class="sxs-lookup"><span data-stu-id="6006c-152">Function</span></span>
<span data-ttu-id="6006c-153">순수 하 게 고전 (비 양자) 인 Q # 언어의 서브루틴 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-153">A type of subroutine in the Q# language that is purely classical (non-quantum).</span></span> <span data-ttu-id="6006c-154">퀀텀 알고리즘 내에서 함수를 사용 하는 [동안에는](xref:microsoft.quantum.glossary#qubit) 이 함수를 사용 하 여 [작업](xref:microsoft.quantum.glossary#operation)을 호출할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-154">While functions are used within quantum algorithms, they cannot act on [qubits](xref:microsoft.quantum.glossary#qubit) or call [operations](xref:microsoft.quantum.glossary#operation).</span></span> <span data-ttu-id="6006c-155">자세한 내용은 [작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-155">For more information, see [Operations and functions](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

## <a name="gate"></a><span data-ttu-id="6006c-156">라는</span><span class="sxs-lookup"><span data-stu-id="6006c-156">Gate</span></span>

<span data-ttu-id="6006c-157">기존 논리 게이트의 개념에 따라 퀀텀 [작업](xref:microsoft.quantum.glossary#operation)에 대 한 레거시 용어입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-157">A legacy term for a quantum [operation](xref:microsoft.quantum.glossary#operation), based on the concept of classical logic gates.</span></span> <span data-ttu-id="6006c-158">[퀀텀 회로](xref:microsoft.quantum.glossary#quantum-circuit-diagram) 는 기존 논리 회로의 유사한 개념에 따라 게이트 (또는 작업)의 네트워크입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-158">A [quantum circuit](xref:microsoft.quantum.glossary#quantum-circuit-diagram) is a network of gates (or operations), based on the similar concept of classical logic circuits.</span></span>

## <a name="global-phase"></a><span data-ttu-id="6006c-159">글로벌 단계</span><span class="sxs-lookup"><span data-stu-id="6006c-159">Global phase</span></span>

<span data-ttu-id="6006c-160">두 [상태가](xref:microsoft.quantum.glossary#quantum-state) ^ {i $ $e 복소수와 동일 하 게 일치 하는 것으로 간주 되는 경우에는 \phi } 전역 단계와 차이가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-160">When two [states](xref:microsoft.quantum.glossary#quantum-state) are identical up to a multiple of a complex number $e^{i\phi}$, they are said to differ up to a global phase.</span></span> <span data-ttu-id="6006c-161">로컬 단계와 달리 전역 단계는 [measurment](xref:microsoft.quantum.glossary#measurement)을 통해 관찰할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-161">Unlike local phases, global phases cannot be observed through any [measurment](xref:microsoft.quantum.glossary#measurement).</span></span> <span data-ttu-id="6006c-162">자세한 내용은 [다음을 참조 하세요.](xref:microsoft.quantum.concepts.qubit)</span><span class="sxs-lookup"><span data-stu-id="6006c-162">For more information, see [The Qubit](xref:microsoft.quantum.concepts.qubit).</span></span>

## <a name="hadamard"></a><span data-ttu-id="6006c-163">Hadamard</span><span class="sxs-lookup"><span data-stu-id="6006c-163">Hadamard</span></span>

<span data-ttu-id="6006c-164">Hadamard 작업 (Hadamard 게이트 또는 변환이 라고도 함)은 단일의 [비트](xref:microsoft.quantum.glossary#qubit) 에서 작동 하 고, [superposition](xref:microsoft.quantum.glossary#superposition) } } 가 처음에 $ \ket{1 $ 상태에 있는 경우 $ \ket{0 $ 또는 $ \ket{0 $의 짝수 superposition에 배치 합니다 } .</span><span class="sxs-lookup"><span data-stu-id="6006c-164">The Hadamard operation (also referred to as the Hadamard gate or transform) acts on a single [qubit](xref:microsoft.quantum.glossary#qubit) and puts it in an even [superposition](xref:microsoft.quantum.glossary#superposition) of $\ket{0}$ or $\ket{1}$ if the qubit is initially in the $\ket{0}$ state.</span></span> <span data-ttu-id="6006c-165">Q #에서이 작업은 미리 정의 된 작업에 의해 적용 됩니다 [`H`](xref:microsoft.quantum.intrinsic.h) .</span><span class="sxs-lookup"><span data-stu-id="6006c-165">In Q#, this operation is applied by the pre-defined [`H`](xref:microsoft.quantum.intrinsic.h) operation.</span></span>

## <a name="immutable"></a><span data-ttu-id="6006c-166">변경할 수 없음</span><span class="sxs-lookup"><span data-stu-id="6006c-166">Immutable</span></span>

<span data-ttu-id="6006c-167">값을 변경할 수 없는 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-167">A variable whose value cannot be changed.</span></span> <span data-ttu-id="6006c-168">Q #의 변경할 수 없는 변수는 키워드를 사용 하 여 생성 됩니다 `let` .</span><span class="sxs-lookup"><span data-stu-id="6006c-168">An immutable variable in Q# is created using the `let` keyword.</span></span> <span data-ttu-id="6006c-169">변경할 *수* 있는 변수를 선언 하려면 [mutable](xref:microsoft.quantum.glossary#immutable) 키워드를 사용 하 여를 선언 하 고 키워드를 사용 하 여 `set` 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-169">To declare variables that *can* be changed, use the [mutable](xref:microsoft.quantum.glossary#immutable) keyword to declare and the `set` keyword to modify the value.</span></span> 

## <a name="measurement"></a><span data-ttu-id="6006c-170">측정</span><span class="sxs-lookup"><span data-stu-id="6006c-170">Measurement</span></span>

<span data-ttu-id="6006c-171">관찰 결과를 생성 하는 데에는 고전적인 비트를 가져오는 것과 같은 이상 [비트](xref:microsoft.quantum.glossary#qubit) (또는 원하는 비트 집합)의 조작입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-171">A manipulation of a [qubit](xref:microsoft.quantum.glossary#qubit) (or set of qubits) that yields the result of an observation, in effect obtaining a classical bit.</span></span> <span data-ttu-id="6006c-172">자세한 내용은 [다음을 참조 하세요.](xref:microsoft.quantum.concepts.qubit#measuring-a-qubit)</span><span class="sxs-lookup"><span data-stu-id="6006c-172">For more information, see [The Qubit](xref:microsoft.quantum.concepts.qubit#measuring-a-qubit).</span></span>

## <a name="mutable"></a><span data-ttu-id="6006c-173">변경 가능</span><span class="sxs-lookup"><span data-stu-id="6006c-173">Mutable</span></span>

<span data-ttu-id="6006c-174">값을 만든 후 해당 값을 변경할 수 있는 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-174">A variable whose value may be changed after it is created.</span></span> <span data-ttu-id="6006c-175">Q #의 변경 가능한 변수는 키워드를 사용 하 여 선언 되 `mutable` 고 키워드를 사용 하 여 수정 됩니다 `set` .</span><span class="sxs-lookup"><span data-stu-id="6006c-175">A mutable variable in Q# is declared using the `mutable` keyword and modified using the `set` keyword.</span></span> <span data-ttu-id="6006c-176">키워드를 사용 하 여 만든 변수 `let` 는 [변경할](xref:microsoft.quantum.glossary#immutable) 수 없으며 해당 값은 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-176">Variables created with the `let` keyword are [immutable](xref:microsoft.quantum.glossary#immutable) and their value cannot be changed.</span></span>

## <a name="namespace"></a><span data-ttu-id="6006c-177">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="6006c-177">Namespace</span></span>

<span data-ttu-id="6006c-178">관련 이름 (예: [작업](xref:microsoft.quantum.glossary#operation), [함수](xref:microsoft.quantum.glossary#function)및 [사용자 정의 형식](xref:microsoft.quantum.glossary#user-defined-type))의 컬렉션에 대 한 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-178">A label for a collection of related names (i.e., [operations](xref:microsoft.quantum.glossary#operation), [functions](xref:microsoft.quantum.glossary#function), and [user-defined types](xref:microsoft.quantum.glossary#user-defined-type)).</span></span> <span data-ttu-id="6006c-179">예를 들어, [네임 스페이스](xref:microsoft.quantum.preparation) 는 초기 상태를 준비 하는 데 도움이 되는 표준 라이브러리에 정의 된 모든 기호에 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-179">For instance the namespace [Microsoft.Quantum.Preparation](xref:microsoft.quantum.preparation) labels all of the symbols defined in the standard library that help with preparing initial states.</span></span>

## <a name="operation"></a><span data-ttu-id="6006c-180">작업(Operation)</span><span class="sxs-lookup"><span data-stu-id="6006c-180">Operation</span></span>

<span data-ttu-id="6006c-181">Q #에서 퀀텀 실행의 기본 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-181">The basic unit of quantum execution in Q#.</span></span> <span data-ttu-id="6006c-182">C, c + + 또는 Python의 함수 또는 c # 또는 Java의 정적 메서드와 거의 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-182">It is roughly equivalent to a function in C, C++ or Python, or a static method in C# or Java.</span></span> <span data-ttu-id="6006c-183">자세한 내용은 [작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-183">For more information, see [Operations and functions](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

## <a name="operator-application"></a><span data-ttu-id="6006c-184">운영자 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="6006c-184">Operator application</span></span>

<span data-ttu-id="6006c-185">퀀텀 작업을 수행 하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-185">Performing a quantum operation.</span></span> <span data-ttu-id="6006c-186">이는 일반적으로 단일 행렬을 현재 퀀텀 상태 벡터에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-186">This typically applies a unitary matrix to the current quantum state vector.</span></span>

## <a name="oracle"></a><span data-ttu-id="6006c-187">Oracle</span><span class="sxs-lookup"><span data-stu-id="6006c-187">Oracle</span></span>

<span data-ttu-id="6006c-188">런타임에 퀀텀 알고리즘에 데이터 종속 정보를 제공 하는 서브루틴입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-188">A subroutine that provides data-dependent information to a quantum algorithm at runtime.</span></span> <span data-ttu-id="6006c-189">일반적으로 superposition에 있는 입력에 해당 하는 출력의 [superposition](xref:microsoft.quantum.glossary#superposition) 을 제공 하는 것이 목표입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-189">Typically, the goal is to provide a [superposition](xref:microsoft.quantum.glossary#superposition) of outputs corresponding to inputs that are in superposition.</span></span> <span data-ttu-id="6006c-190">자세한 내용은 [Oracles](xref:microsoft.quantum.libraries.data-structures#oracles)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-190">For more information, see [Oracles](xref:microsoft.quantum.libraries.data-structures#oracles).</span></span>

## <a name="partial-application"></a><span data-ttu-id="6006c-191">부분 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="6006c-191">Partial application</span></span>

<span data-ttu-id="6006c-192">모든 필수 입력 없이 [함수](xref:microsoft.quantum.glossary#function) 또는 [작업](xref:microsoft.quantum.glossary#operation) 을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-192">Calling a [function](xref:microsoft.quantum.glossary#function) or [operation](xref:microsoft.quantum.glossary#operation) without all the required inputs.</span></span> <span data-ttu-id="6006c-193">그러면 나중에 응용 프로그램에서 제공 하는 누락 된 매개 변수 (밑줄로 표시 됨)만 필요한 새 [호출 가능](xref:microsoft.quantum.glossary#callable) 이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-193">This returns a new [callable](xref:microsoft.quantum.glossary#callable) that only needs the missing parameters (indicated by an underscore) to be supplied during a future application.</span></span> <span data-ttu-id="6006c-194">예를 들어 함수를 지정 `MyFunc(x : int, y : int) : int {return x + y;}` 하면 해당 함수를 새 함수에 부분적으로 적용할 수 있습니다 `let NewFunc = MyFunc(_, 3)` .</span><span class="sxs-lookup"><span data-stu-id="6006c-194">For example, given the function `MyFunc(x : int, y : int) : int {return x + y;}` you can partially apply it to a new function `let NewFunc = MyFunc(_, 3)`.</span></span> <span data-ttu-id="6006c-195">그런 다음 `NewFunc(2)` 값 *5*를 반환 하는 누락 된 매개 변수를 사용 하 여 나중에 새 함수를 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-195">You can then call the new function at a later time with the missing parameter `NewFunc(2)` which returns the value *5*.</span></span>  <span data-ttu-id="6006c-196">자세한 내용은 [부분 응용 프로그램](xref:microsoft.quantum.guide.operationsfunctions#partial-application)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-196">For more information, see [Partial application](xref:microsoft.quantum.guide.operationsfunctions#partial-application).</span></span>

## <a name="pauli-operators"></a><span data-ttu-id="6006c-197">Pauli 연산자</span><span class="sxs-lookup"><span data-stu-id="6006c-197">Pauli operators</span></span>

<span data-ttu-id="6006c-198">`X`, `Y` 및 퀀텀 작업으로 알려진 3 개의 2 x 2 단일 매트릭스 집합입니다 `Z` .</span><span class="sxs-lookup"><span data-stu-id="6006c-198">A set of three 2 x 2 unitary matrices known as the `X`, `Y` and `Z` quantum operations.</span></span> <span data-ttu-id="6006c-199">Id 매트릭스 $I는 $ 집합에도 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-199">The identity matrix, $I$, is often included in the set as well.</span></span>  <span data-ttu-id="6006c-200">$I = \begin{ bmatrix } 1 & 0 \\ \\ 0 & 1 \begin{ bmatrix } $, $X = \begin{ bmatrix } 0 & 1 \\ \\ 1 & 0 \begin{ bmatrix } $, $Y = \begin{ bmatrix } 0 &-i \\ \\ & 0 \begin{ bmatrix } $, $Z = \begin{ bmatrix } 1 & 0 \\ \\ 0 &-1 \begin{ bmatrix } $.</span><span class="sxs-lookup"><span data-stu-id="6006c-200">$I = \begin{bmatrix} 1 & 0 \\\\ 0 & 1 \end{bmatrix}$, $X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix}$, $Y = \begin{bmatrix} 0 & -i \\\\ i & 0 \end{bmatrix}$, $Z = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix}$.</span></span>   <span data-ttu-id="6006c-201">자세한 내용은 [단일 기능 비트 작업](xref:microsoft.quantum.concepts.qubit#single-qubit-operations)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-201">For more information, see [Single-qubit operations](xref:microsoft.quantum.concepts.qubit#single-qubit-operations).</span></span>

## <a name="quantum-circuit-diagram"></a><span data-ttu-id="6006c-202">퀀텀 회로 다이어그램</span><span class="sxs-lookup"><span data-stu-id="6006c-202">Quantum circuit diagram</span></span>

<span data-ttu-id="6006c-203">간단한 퀀텀 프로그램의 [작업](xref:microsoft.quantum.glossary#operation) 순서 (또는 [게이트](xref:microsoft.quantum.glossary#gate))를 그래픽으로 나타내는 메서드 (예:)</span><span class="sxs-lookup"><span data-stu-id="6006c-203">A method to graphically represent the sequence of [operations](xref:microsoft.quantum.glossary#operation) (or [gates](xref:microsoft.quantum.glossary#gate)) for simple quantum programs, for example</span></span> 

![샘플 회로 다이어그램](~/media/qpe.png)<span data-ttu-id="6006c-205">.</span><span class="sxs-lookup"><span data-stu-id="6006c-205">.</span></span> 

<span data-ttu-id="6006c-206">자세한 내용은 [퀀텀 회로](xref:microsoft.quantum.concepts.circuits)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-206">For more information, see [Quantum circuits](xref:microsoft.quantum.concepts.circuits).</span></span>

## <a name="quantum-libraries"></a><span data-ttu-id="6006c-207">퀀텀 라이브러리</span><span class="sxs-lookup"><span data-stu-id="6006c-207">Quantum libraries</span></span>

<span data-ttu-id="6006c-208">Q # 프로그램을 만들기 위한 [작업](xref:microsoft.quantum.glossary#operation), [함수](xref:microsoft.quantum.glossary#function) 및 [사용자 정의 형식의](xref:microsoft.quantum.glossary#user-defined-type) 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-208">Collections of [operations](xref:microsoft.quantum.glossary#operation), [functions](xref:microsoft.quantum.glossary#function) and [user-defined types](xref:microsoft.quantum.glossary#user-defined-type) for creating Q# programs.</span></span> <span data-ttu-id="6006c-209">[표준 라이브러리](xref:microsoft.quantum.libraries.standard.intro) 는 기본적으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-209">The [Standard library](xref:microsoft.quantum.libraries.standard.intro) is installed by default.</span></span> <span data-ttu-id="6006c-210">사용할 수 있는 다른 라이브러리는 [화학 라이브러리](xref:microsoft.quantum.chemistry.concepts.intro), [숫자 라이브러리](xref:microsoft.quantum.numerics.intro) 및 [Machine learning 라이브러리](xref:microsoft.quantum.machine-learning.concepts.intro)입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-210">Other libraries available are the [Chemistry library](xref:microsoft.quantum.chemistry.concepts.intro), the [Numerics library](xref:microsoft.quantum.numerics.intro) and the [Machine learning library](xref:microsoft.quantum.machine-learning.concepts.intro).</span></span>

## <a name="quantum-state"></a><span data-ttu-id="6006c-211">퀀텀 상태</span><span class="sxs-lookup"><span data-stu-id="6006c-211">Quantum state</span></span>

<span data-ttu-id="6006c-212">[측정](xref:microsoft.quantum.glossary#measurement) 확률을 추출할 수 있는 격리 된 퀀텀 시스템의 정확한 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-212">The precise state of an isolated quantum system, from which [measurement](xref:microsoft.quantum.glossary#measurement) probabilities can be extracted.</span></span> <span data-ttu-id="6006c-213">퀀텀 컴퓨팅에서 퀀텀 시뮬레이터는이 정보를 사용 하 여이 작업에 응답 하는 방법을 시뮬레이션 합니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-213">In quantum computing, the quantum simulator uses this information to simulate how qubits respond to operations.</span></span> <span data-ttu-id="6006c-214">자세한 내용은 [다음을 참조 하세요.](xref:microsoft.quantum.concepts.qubit)</span><span class="sxs-lookup"><span data-stu-id="6006c-214">For more information, see [The Qubit](xref:microsoft.quantum.concepts.qubit).</span></span>

## <a name="qubit"></a><span data-ttu-id="6006c-215">고 비트</span><span class="sxs-lookup"><span data-stu-id="6006c-215">Qubit</span></span>

<span data-ttu-id="6006c-216">기존 컴퓨팅의 *비트* 와 유사한 퀀텀 정보의 기본 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-216">A basic unit of quantum information, analogous to a *bit* in classical computing.</span></span> <span data-ttu-id="6006c-217">자세한 내용은 [다음을 참조 하세요.](xref:microsoft.quantum.concepts.qubit)</span><span class="sxs-lookup"><span data-stu-id="6006c-217">For more information, see [The Qubit](xref:microsoft.quantum.concepts.qubit).</span></span>

## <a name="repeat-until-success"></a><span data-ttu-id="6006c-218">반복-성공-성공</span><span class="sxs-lookup"><span data-stu-id="6006c-218">Repeat-until-success</span></span>

<span data-ttu-id="6006c-219">확률적가 성공 하는 퀀텀 알고리즘입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-219">A quantum algorithm that probabilistically succeeds.</span></span> <span data-ttu-id="6006c-220">오류가 발생 하면 루틴이 성공 하거나 제한에 도달할 때까지 다시 시도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-220">Upon failure, the routine will retry until successful (or a limit has been reached).</span></span> <span data-ttu-id="6006c-221">자세한 내용은 [성공까지 반복 (RUS)](xref:microsoft.quantum.guide.controlflow#repeat-until-success-loop) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-221">For more information, see [Repeat Until Success (RUS)](xref:microsoft.quantum.guide.controlflow#repeat-until-success-loop)</span></span>

## <a name="standard-libraries"></a><span data-ttu-id="6006c-222">표준 라이브러리</span><span class="sxs-lookup"><span data-stu-id="6006c-222">Standard libraries</span></span>

<span data-ttu-id="6006c-223">설치 하는 동안 Q # 컴파일러와 함께 설치 되는 [작업](xref:microsoft.quantum.glossary#operation), [함수](xref:microsoft.quantum.glossary#function) 및 [사용자 정의 형식](xref:microsoft.quantum.glossary#user-defined-type) 입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-223">[Operations](xref:microsoft.quantum.glossary#operation), [functions](xref:microsoft.quantum.glossary#function) and [user-defined types](xref:microsoft.quantum.glossary#user-defined-type) that are installed along with the Q# compiler during installation.</span></span> <span data-ttu-id="6006c-224">표준 라이브러리 구현은 대상 컴퓨터와는 독립적입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-224">The standard library implementation is agnostic with respect to target machines.</span></span> <span data-ttu-id="6006c-225">자세한 내용은 [표준 라이브러리](xref:microsoft.quantum.libraries.standard.intro)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-225">For more information, see [Standard libraries](xref:microsoft.quantum.libraries.standard.intro).</span></span>

## <a name="superposition"></a><span data-ttu-id="6006c-226">Superposition</span><span class="sxs-lookup"><span data-stu-id="6006c-226">Superposition</span></span>

<span data-ttu-id="6006c-227">퀀텀 계산의 [개념은](xref:microsoft.quantum.glossary#qubit) } } [측정](xref:microsoft.quantum.glossary#measurement)될 때까지 $ \ket{0 $ 및 $ \ket{1 $ 이라는 두 가지 상태의 선형 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-227">The concept in quantum computing that a [qubit](xref:microsoft.quantum.glossary#qubit) is a linear combination of two states, $\ket{0}$ and $\ket{1}$, until it is [measured](xref:microsoft.quantum.glossary#measurement).</span></span>  <span data-ttu-id="6006c-228">자세한 내용은 [퀀텀 컴퓨팅 이해](xref:microsoft.quantum.overview.understanding)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-228">For more information, see [Understanding quantum computing](xref:microsoft.quantum.overview.understanding).</span></span>

## <a name="target-machine"></a><span data-ttu-id="6006c-229">대상 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="6006c-229">Target machine</span></span>

<span data-ttu-id="6006c-230">추상 퀀텀 프로그램을 하드웨어 또는 시뮬레이션으로 낮추는 컴파일 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-230">A compilation target that lowers an abstract quantum program towards hardware or simulation.</span></span> <span data-ttu-id="6006c-231">여기에는 일반적으로 게이트 교체, 오류 수정 인코딩, 기 하 도형 레이아웃 등을 비롯 한 많은 용도로 다시 쓰기가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-231">This typically include re-writes for many purposes including gate replacement, encoding for error correction, geometric layout and others.</span></span> <span data-ttu-id="6006c-232">자세한 내용은 [퀀텀 시뮬레이터 및 호스트 응용 프로그램](xref:microsoft.quantum.machines)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-232">For more information, see [Quantum simulators and host applications](xref:microsoft.quantum.machines).</span></span>

## <a name="teleportation"></a><span data-ttu-id="6006c-233">순간 이동</span><span class="sxs-lookup"><span data-stu-id="6006c-233">Teleportation</span></span>

<span data-ttu-id="6006c-234">[되거나 얽 히](xref:microsoft.quantum.glossary#entanglement) 및 [측정](xref:microsoft.quantum.glossary#measurement)을 사용 하 여 물리적으로 이동 하지 [않고 한 곳에서 다른](xref:microsoft.quantum.glossary#qubit) 위치로 데이터를 다시 생성 하거나 [퀀텀 상태](xref:microsoft.quantum.glossary#quantum-state)를 다시 생성 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-234">A method for regenerating data, or the [quantum state](xref:microsoft.quantum.glossary#quantum-state), of one [qubit](xref:microsoft.quantum.glossary#qubit) from one place to another without physically moving the qubit, using [entanglement](xref:microsoft.quantum.glossary#entanglement) and [measurement](xref:microsoft.quantum.glossary#measurement).</span></span>  <span data-ttu-id="6006c-235">자세한 내용은 [퀀텀 회로](xref:microsoft.quantum.concepts.circuits) 및 [퀀텀 Katas](xref:microsoft.quantum.overview.katas)의 각 kata를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-235">For more information, see [Quantum circuits](xref:microsoft.quantum.concepts.circuits) and the respective kata at [Quantum Katas](xref:microsoft.quantum.overview.katas).</span></span>

## <a name="tuple"></a><span data-ttu-id="6006c-236">Tuple</span><span class="sxs-lookup"><span data-stu-id="6006c-236">Tuple</span></span>

<span data-ttu-id="6006c-237">단일 값으로 작동 하는 쉼표로 구분 된 값의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-237">A collection of comma-separated values that acts as a single value.</span></span> <span data-ttu-id="6006c-238">튜플의 *형식은* 포함 하는 값 형식에 의해 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-238">The *type* of a tuple is defined by the types of values it contains.</span></span> <span data-ttu-id="6006c-239">Q #에서 튜플은 [변경할](xref:microsoft.quantum.glossary#immutable) 수 없으며 중첩 되거나, 배열을 포함 하거나, 배열에 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-239">In Q#, tuples are [immutable](xref:microsoft.quantum.glossary#immutable) and can be nested, contain arrays, or used in an array.</span></span> <span data-ttu-id="6006c-240">자세한 내용은 [튜플 형식](xref:microsoft.quantum.guide.types#tuple-types)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-240">For more information, see [Tuple types](xref:microsoft.quantum.guide.types#tuple-types).</span></span>

## <a name="unitary-operator"></a><span data-ttu-id="6006c-241">단일 연산자</span><span class="sxs-lookup"><span data-stu-id="6006c-241">Unitary operator</span></span>

<span data-ttu-id="6006c-242">역이 [adjoint](xref:microsoft.quantum.glossary#adjoint)와 같은 연산자 (예 $UU: ^ {\aa= } \dagger)입니다. $</span><span class="sxs-lookup"><span data-stu-id="6006c-242">An operator whose inverse is equal to its [adjoint](xref:microsoft.quantum.glossary#adjoint), i.e., $UU^{\dagger} = \id$.</span></span>

## <a name="user-defined-type"></a><span data-ttu-id="6006c-243">사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="6006c-243">User-defined type</span></span>

<span data-ttu-id="6006c-244">단일 단위로 참조 될 수 있는 기본 제공 또는 이전에 정의 된 형식의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="6006c-244">A collection of built-in or previously defined types that may be referred to as a single unit.</span></span> <span data-ttu-id="6006c-245">자세한 내용은 [사용자 정의 형식](xref:microsoft.quantum.guide.types#user-defined-types)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6006c-245">For more information, see [User-defined types](xref:microsoft.quantum.guide.types#user-defined-types).</span></span>