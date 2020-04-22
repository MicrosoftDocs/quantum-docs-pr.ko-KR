---
title: 양자 컴퓨팅 용어집
description: 양자 컴퓨팅에 사용되는 일반적인 용어, 동작 및 개체의 용어집입니다.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.glossary
ms.openlocfilehash: ee78515a0f47730b7d3df10da0853c5b8a7f6624
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "81482215"
---
# <a name="quantum-computing-glossary"></a>양자 컴퓨팅 용어집

## <a name="adjoint"></a>아조인트

복잡한 컨쥬게이트는 [작업의](xref:microsoft.quantum.glossary#operation)전치입니다. [단일](xref:microsoft.quantum.glossary#unitary-operator) 연산자 구현 작업의 경우 인조는 작업의 역이며 단검 기호로 표시됩니다. 예를 들어 작업이 `U` $U$의 단일 연산자를 나타내는 경우 `Adjoint U` $U^\단검$을 나타냅니다. 자세한 내용은 [Adjoint](xref:microsoft.quantum.language.file-structure#adjoint)을 참조하십시오.

## <a name="ancilla"></a>안실라 (주)

양자 컴퓨터에 대한 임시 메모리 역할을 하며 필요에 따라 할당 및 제거되는 [큐빗입니다.](xref:microsoft.quantum.glossary#qubit)  자세한 내용은 [다중 큐빗 을](xref:microsoft.quantum.concepts.multiple-qubits)참조하십시오.

## <a name="bell-state"></a>벨 상태

두 큐비트의 [4개의](xref:microsoft.quantum.glossary#entanglement) 특정 한 가지 [양자 상태](xref:microsoft.quantum.glossary#quantum-state) 중 하나. 네 개의 상태는 $\ket{{beta_{ij}} = (\mathbb{I} \otimes X^iZ^j){00} {11}(\ket +{2}\ket) / \sqrt $입니다. 벨 상태는 [EPR 쌍이라고도 합니다.](xref:microsoft.quantum.glossary#epr-pair)

## <a name="bloch-sphere"></a>블로흐 구

3차원 단위 구체에서 점으로 서 단일[큐빗](xref:microsoft.quantum.glossary#qubit) [양자 상태의](xref:microsoft.quantum.glossary#quantum-state) 그래픽 표현. 자세한 내용은 [블로흐 구를 사용하여 큐빗 및 변환 시각화를](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere)참조하십시오.

## <a name="callable"></a>호출할

Q# 언어의 [작업](xref:microsoft.quantum.glossary#operation) 또는 [함수입니다.](xref:microsoft.quantum.glossary#function) 자세한 내용은 [작동 및 함수 유형을](xref:microsoft.quantum.language.type-model#operation-and-function-types)참조하십시오.

## <a name="clifford-group"></a>클리포드 그룹

[블로흐 구의](xref:microsoft.quantum.glossary#bloch-sphere) 팔각형과 [파울리 연산자의](xref:microsoft.quantum.glossary#pauli-operators)효과 순열을 차지하는 작업 집합입니다. 여기에는 [$X$](xref:microsoft.quantum.intrinsic.x)$Y [, $Z](xref:microsoft.quantum.intrinsic.y) [$](xref:microsoft.quantum.intrinsic.z)$H [및](xref:microsoft.quantum.intrinsic.h) $S [$](xref:microsoft.quantum.intrinsic.s)운영이 포함됩니다.

## <a name="controlled"></a>제어

대상 [작업에](xref:microsoft.quantum.glossary#operation) 대한 인에이블러로 하나 이상의 [큐빗을](xref:microsoft.quantum.glossary#qubit) 취하는 양자 작업입니다. 자세한 내용은 [제어](xref:microsoft.quantum.language.type-model#controlled)를 참조하십시오.

## <a name="dirac-notation"></a>디락 표기

*브라케트* 표기법이라고도 하는 [양자 상태의](xref:microsoft.quantum.glossary#quantum-state)표현을 단순화하는 상징적 약어입니다.  *브래지어* 부분은 행 벡터를 나타냅니다,예를 들어 $\bra{A} = \begin{bmatrix} A{_1} & A{_2} \end{bmatrix}$ 및 *케트* 부분은 열 벡터를 나타내고, \\ \\ $\ket{B} = \begin{bmatrix} B{_1} B{_2} \end{bmatrix}} 자세한 내용은 [Dirac 표기법을](xref:microsoft.quantum.concepts.dirac)참조하십시오.

## <a name="eigenvalue"></a>아이젠밸류

지정된 변환의 [고유 벡터의](xref:microsoft.quantum.glossary#eigenvector) 크기가 변환의 적용에 의해 변경되는 요인입니다.  정사각형 행렬 $M$$v,$Mv = cv$를 감안할 때, 여기서 $c$는 고유 가치이며 복잡한 수의 인수가 될 수 있습니다. 자세한 내용은 [고급 행렬 개념을](xref:microsoft.quantum.concepts.matrix-advanced)참조하십시오.

## <a name="eigenvector"></a>고유 벡터

지정된 변환에 의해 방향이 변경되지 않고 그 크기가 해당 벡터의 [고유 값에](xref:microsoft.quantum.glossary#eigenvalue)해당하는 요인에 의해 변경되는 벡터입니다. 정사각형 행렬 $M$과 $c$의 고유 값값을 감안할 때, $v$이 행렬의 고유 벡터이며 복잡한 수의 인수가 될 수 있는 cv$를 $Mv. 자세한 내용은 [고급 행렬 개념을](xref:microsoft.quantum.concepts.matrix-advanced)참조하십시오.

## <a name="entanglement"></a>얽 힘

양자 입자(예: [큐빗)는](xref:microsoft.quantum.glossary#qubit)서로 독립적으로 설명할 수 없도록 연결되거나 *얽히게* 될 수 있습니다. 측정 결과는 무한히 멀리 떨어져 있는 경우에도 상관관계가 있습니다. 얽힘은 큐빗의 [상태를](xref:microsoft.quantum.glossary#quantum-state) [측정하는](xref:microsoft.quantum.glossary#measurement) 데 필수적입니다.  자세한 내용은 [고급 행렬 개념을](xref:microsoft.quantum.concepts.matrix-advanced)참조하십시오.

## <a name="epr-pair"></a>EPR 쌍

두 [큐비트의](xref:microsoft.quantum.glossary#qubit)네 가지 특정 최대 얽힌 [양자 상태](xref:microsoft.quantum.glossary#quantum-state) 중 하나 . 네{1} 개의 상태는 $\ket{\beta_{ij}} = (\mathbb \otimes X^iZ^j) (\ket{00} + \ket){11}/ \sqrt{2}$입니다. EPR 쌍은 [벨 상태라고도](xref:microsoft.quantum.glossary#bell-state) 합니다.

## <a name="evolution"></a>진화

시간이 지남에 따라 [양자 상태가](xref:microsoft.quantum.glossary#quantum-state) 어떻게 변하는가. 자세한 내용은 [행렬 지수](xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials)를 참조하십시오.

## <a name="function"></a>기능
순전히 고전적(비양자)인 Q# 언어의 서브루틴 유형입니다. 함수는 양자 알고리즘 내에서 사용되지만 [큐빗](xref:microsoft.quantum.glossary#qubit) 또는 호출 [작업에](xref:microsoft.quantum.glossary#operation)대해 작동할 수 없습니다. 자세한 내용은 [작동 및 함수 유형을](xref:microsoft.quantum.language.type-model#operation-and-function-types)참조하십시오.

## <a name="gate"></a>게이트

고전 논리 게이트의 개념을 기반으로 양자 [작업에](xref:microsoft.quantum.glossary#operation)대한 레거시 용어. [양자 회로는](xref:microsoft.quantum.glossary#quantum-circuit-diagram) 고전적인 논리 회로의 유사한 개념을 기반으로 게이트 (또는 작업)의 네트워크입니다.

## <a name="global-phase"></a>글로벌 단계

두 [상태가](xref:microsoft.quantum.glossary#quantum-state) $e^{i\phi}$의 배수와 동일하면 전역 단계까지 차이가 있다고 합니다. 로컬 단계와 달리 글로벌 단계는 [측정을](xref:microsoft.quantum.glossary#measurement)통해 관찰할 수 없습니다. 자세한 내용은 [Qubit](xref:microsoft.quantum.concepts.qubit)을 참조하십시오.

## <a name="hadamard"></a>Hadamard

Hadamard 작업 (또한 하다마드 게이트 또는 변환이라고도 함)은 단일 [큐빗에서](xref:microsoft.quantum.glossary#qubit) 작동하며 큐빗이 처음에 $\ket{0}$ $ 상태에있는 경우 $ \ ket{0}$ 또는 $ \ket{1}$ 의 도 [중첩에](xref:microsoft.quantum.glossary#superposition) 놓습니다. Q#에서 이 작업은 미리 정의된 [`H`](xref:microsoft.quantum.intrinsic.h) 작업에 의해 적용됩니다.

## <a name="immutable"></a>변경 불가능

값을 변경할 수 없는 변수입니다. Q#의 변경할 수 없는 변수는 `let` 키워드를 사용하여 만들어집니다. 변경할 *수* 있는 변수를 선언하려면 [가변](xref:microsoft.quantum.glossary#immutable) 키워드를 사용하여 `set` 선언하고 키워드를 사용하여 값을 수정합니다. 

## <a name="measurement"></a>측정

관찰의 결과를 산출하는 [큐비트(또는](xref:microsoft.quantum.glossary#qubit) 큐빗 세트)를 조작하여 사실상 클래식 비트를 얻습니다. 자세한 내용은 [Qubit](xref:microsoft.quantum.concepts.qubit#measuring-a-qubit)을 참조하십시오.

## <a name="mutable"></a>변경 가능

값을 만든 후 변경할 수 있는 변수입니다. Q#의 가변 변수는 키워드를 `mutable` 사용하여 선언되고 `set` 키워드를 사용하여 수정됩니다. `let` 키워드로 만든 변수는 [변경할 수](xref:microsoft.quantum.glossary#immutable) 없으며 해당 값은 변경할 수 없습니다.

## <a name="namespace"></a>네임스페이스

관련 이름(예: [작업,](xref:microsoft.quantum.glossary#operation)함수 및 [사용자 정의 형식)의](xref:microsoft.quantum.glossary#user-defined-type) [컬렉션에](xref:microsoft.quantum.glossary#function)대한 레이블입니다. 예를 들어 네임스페이스 [Microsoft.Quantum.Preparation는](xref:microsoft.quantum.preparation) 초기 상태를 준비하는 데 도움이 되는 표준 라이브러리에 정의된 모든 기호를 레이블로 지정합니다.

## <a name="operation"></a>작업(Operation)

Q#의 양자 실행의 기본 단위입니다. C, C ++ 또는 파이썬의 함수 또는 C # 또는 Java의 정적 메서드와 거의 동일합니다. 자세한 내용은 [작동 및 함수 유형을](xref:microsoft.quantum.language.type-model#operation-and-function-types)참조하십시오.

## <a name="operator-application"></a>운영자 응용 프로그램

양자 조작 수행. 이는 전형적으로 현재 양자 상태 벡터에 단일 행렬을 적용합니다.

## <a name="oracle"></a>Oracle

런타임시 양자 알고리즘에 데이터 종속 정보를 제공하는 서브루틴입니다. 일반적으로 목표는 중첩에 있는 입력에 해당하는 출력의 [중첩을](xref:microsoft.quantum.glossary#superposition) 제공하는 것입니다. 자세한 내용은 [Oracle s](xref:microsoft.quantum.libraries.data-structures#oracles).

## <a name="partial-application"></a>부분 응용 프로그램

필요한 입력없이 [함수](xref:microsoft.quantum.glossary#function) 또는 [작업을](xref:microsoft.quantum.glossary#operation) 호출합니다. 이렇게 하면 향후 응용 프로그램 중에 누락된 매개 변수(밑줄로 표시)만 제공되어야 하는 새 [호출 가능](xref:microsoft.quantum.glossary#callable) 이 반환됩니다. 예를 들어 함수를 `MyFunc(x : int, y : int) : int {return x + y;}` 감안할 때 새 함수에 `let NewFunc = MyFunc(_, 3)`부분적으로 적용할 수 있습니다. 그런 다음 값 *5를*반환하는 누락 된 `NewFunc(2)` 매개 변수로 나중에 새 함수를 호출 할 수 있습니다.  자세한 내용은 [부분 응용 프로그램을](xref:microsoft.quantum.language.expressions#partial-application)참조하십시오.

## <a name="pauli-operators"></a>파울리 연산자

`X`및 `Y` `Z` 양자 작업으로 알려진 3개의 2 x 2 유니트리 행렬 집합입니다. id 행렬인 $I$도 집합에 포함되는 경우가 많습니다.  $I = \begin{bmatrix} \\ \\ 1 & 0 & 1 \end{bmatrix}, $X = \\ \\ \begin{bmatrix}0 & 1 1 & 0 \end{bmatrix}, $Y = \begin{bmatrix} 0 \\ \\ & -i & \\ \\ 0\end{bmatrix}, $Z = \begin{bmatrix} 1 & 0 & =1 &   자세한 내용은 [단일 큐빗 작업을](xref:microsoft.quantum.concepts.qubit#single-qubit-operations)참조하십시오.

## <a name="quantum-circuit-diagram"></a>양자 회로 다이어그램

간단한 양자 프로그램(예: ![샘플 회로도)에](~/media/qpe.png)대한 [작업](xref:microsoft.quantum.glossary#operation) 순서(또는 [게이트)를](xref:microsoft.quantum.glossary#gate)그래픽으로 나타내는 방법. 자세한 내용은 [퀀텀 회로를](xref:microsoft.quantum.concepts.circuits)참조하십시오.

## <a name="quantum-libraries"></a>양자 라이브러리

Q# 프로그램을 만들기 위한 [작업,](xref:microsoft.quantum.glossary#operation) [함수](xref:microsoft.quantum.glossary#function) 및 [사용자 정의 형식의](xref:microsoft.quantum.glossary#user-defined-type) 컬렉션입니다. [표준 라이브러리는](xref:microsoft.quantum.libraries.standard.intro) 기본적으로 설치됩니다. 다른 라이브러리는 [화학 라이브러리,](xref:microsoft.quantum.chemistry.concepts.intro) [숫자 라이브러리](xref:microsoft.quantum.numerics.intro) 및 [기계 학습 라이브러리입니다.](xref:microsoft.quantum.machine-learning.concepts.intro)

## <a name="quantum-state"></a>양자 상태

[측정](xref:microsoft.quantum.glossary#measurement) 확률을 추출할 수 있는 격리된 양자 시스템의 정확한 상태입니다. 양자 컴퓨팅에서 양자 시뮬레이터는 이 정보를 사용하여 큐빗이 작업에 어떻게 반응하는지 시뮬레이션합니다. 자세한 내용은 [Qubit](xref:microsoft.quantum.concepts.qubit)을 참조하십시오.

## <a name="qubit"></a>큐빗 (주)

양자 정보의 기본 단위, 고전 컴퓨팅에서 *비트와* 유사. 자세한 내용은 [Qubit](xref:microsoft.quantum.concepts.qubit)을 참조하십시오.

## <a name="repeat-until-success"></a>성공까지 반복

확률적으로 성공하는 양자 알고리즘. 실패하면 루틴이 성공(또는 제한에 도달할 때까지)이 다시 시도됩니다. 자세한 내용은 [성공(RUS)까지 반복을](xref:microsoft.quantum.techniques.qubits#measurements) 참조하십시오.

## <a name="standard-libraries"></a>표준 라이브러리

설치 하는 동안 Q# 컴파일러와 함께 설치 되는 [작업,](xref:microsoft.quantum.glossary#operation) [기능](xref:microsoft.quantum.glossary#function) 및 [사용자 정의 형식입니다.](xref:microsoft.quantum.glossary#user-defined-type) 표준 라이브러리 구현은 대상 컴퓨터와 관련이 없습니다. 자세한 내용은 [표준 라이브러리를](xref:microsoft.quantum.libraries.standard.intro)참조하십시오.

## <a name="superposition"></a>중첩

양자 컴퓨팅의 개념은 [qubit이](xref:microsoft.quantum.glossary#qubit) [측정될](xref:microsoft.quantum.glossary#measurement)때까지 $\ket{\0}$와 $\ket{1}$의 선형 조합이라는 개념입니다.  자세한 내용은 [양자 컴퓨팅이란 무엇입니까](xref:microsoft.quantum.overview.what)를 참조하십시오.

## <a name="target-machine"></a>대상 기계

추상 양자 프로그램을 하드웨어 또는 시뮬레이션으로 낮추는 컴파일 대상입니다. 여기에는 일반적으로 게이트 교체, 오류 수정을 위한 인코딩, 기하학적 레이아웃 등 다양한 용도로 재작성이 포함됩니다. 자세한 내용은 [퀀텀 시뮬레이터 및 호스트 응용 프로그램을](xref:microsoft.quantum.machines)참조하십시오.

## <a name="teleportation"></a>순간 이동

[얽힘](xref:microsoft.quantum.glossary#entanglement) 및 [측정을](xref:microsoft.quantum.glossary#measurement)사용하여 한 장소에서 다른 장소로 한 [큐빗의](xref:microsoft.quantum.glossary#qubit) 데이터 또는 [양자 상태를](xref:microsoft.quantum.glossary#quantum-state)재생하는 방법.  자세한 내용은 [퀀텀 회로및](xref:microsoft.quantum.concepts.circuits) 이 모든 것을 [함께 넣는 것을](xref:microsoft.quantum.techniques.puttingittogether)참조하십시오.

## <a name="tuple"></a>Tuple

단일 값으로 작동하는 쉼표로 구분된 값의 컬렉션입니다. 튜플의 *유형은* 튜플에 포함된 값의 유형에 의해 정의됩니다. Q#에서 튜플은 [변경할 수 없으며](xref:microsoft.quantum.glossary#immutable) 중첩되거나 배열을 포함하거나 배열에 사용할 수 있습니다. 자세한 내용은 [튜플 유형을](xref:microsoft.quantum.language.type-model#tuple-types)참조하십시오.

## <a name="unitary-operator"></a>단일 연산자

역이 [해당 관절과](xref:microsoft.quantum.glossary#adjoint)같을 수 있는 연산자( 즉, $UU^{\단검} = \id$입니다.

## <a name="user-defined-type"></a>사용자 정의 형식

단일 단위로 지칭될 수 있는 기본 제공 또는 이전에 정의된 형식의 컬렉션입니다. 자세한 내용은 [사용자 정의 형식을](xref:microsoft.quantum.language.type-model#user-defined-types)참조하십시오.