---
제목: 퀀텀 컴퓨팅 용어집 설명: 퀀텀 컴퓨팅에 사용 되는 일반적인 용어, 작업 및 개체의 용어집입니다.
작성자: bradben: benbra m. 날짜: 9/1/2020 밀리초. 토픽: 참조 uid: microsoft 양자:
- "Q#"
- "$$v"
- "$$"
- "$$"
- "$"
- "$"
- "$"
- "$$"
- "\cdots"
- "bmatrix"
- "\ddots"
- "\equiv"
- "\sum"
- "\begin"
- "\end"
- "\sqrt"
- "\otimes"
- "{"
- "}"
- "\text"
- "\phi"
- "\kappa"
- "\psi"
- "\alpha"
- "\beta"
- "\gamma"
- "\delta"
- "\omega"
- "\bra"
- "\ket"
- "\boldone"
- "\\\\"
- "\\"
- "="
- "\frac"
- "\text"
- "\mapsto"
- "\dagger"
- "\to"
- "\begin{cases}"
- "\end{cases}"
- "\operatorname"
- "\braket"
- "\id"
- "\expect"
- "\defeq"
- "\variance"
- "\dd"
- "&"
- "\begin{align}"
- "\end{align}"
- "\Lambda"
- "\lambda"
- "\Omega"
- "\mathrm"
- "\left"
- "\right"
- "\qquad"
- "\times"
- "\big"
- "\langle"
- "\rangle"
- "\bigg"
- "\Big"
- "|"
- "\mathbb"
- "\vec"
- "\in"
- "\texttt"
- "\ne"
- "<"
- ">"
- "\leq"
- "\geq"
- "~~"
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- "\_"

---

# <a name="quantum-computing-glossary"></a>퀀텀 컴퓨팅 용어집

## <a name="adjoint"></a>Adjoint

[작업](xref:microsoft.quantum.glossary#operation)의 복소수 복소수입니다. [단일](xref:microsoft.quantum.glossary#unitary-operator) 연산자를 구현 하는 작업의 경우 adjoint는 작업의 역함수 이며 칼 기호로 표시 됩니다. 예를 들어 연산이 `U` 단일 연산자 u를 나타내면 $ $ 는 `Adjoint U` u ^를 나타냅니다 $ \dagger $ . 자세한 내용은 [함수 응용 프로그램](xref:microsoft.quantum.qsharp.functorapplication#functor-application)을 참조 하세요.

## <a name="ancilla"></a>Ancilla

퀀텀 컴퓨터의 임시 메모리로 사용 되며 필요에 따라 할당 및 할당 취소 되는 [기능입니다.](xref:microsoft.quantum.glossary#qubit)  자세한 내용은 [여러 개의 추가 비트](xref:microsoft.quantum.concepts.multiple-qubits)를 참조 하세요.

## <a name="bell-state"></a>종 상태

두 개의 최대 [entangled](xref:microsoft.quantum.glossary#entanglement) [퀀텀 상태](xref:microsoft.quantum.glossary#quantum-state) 중 하나입니다. 네 가지 상태는 $ \ket { \beta _ { ij } } = ( \mathbb { I } \otimes X ^ iZ ^ j) ( \ket { 00 }  +  \ket { 11 } )/ \sqrt { 2 } $ 로 정의 됩니다. 종 상태는 [EPR 쌍](xref:microsoft.quantum.glossary#epr-pair)이 라고도 합니다.

## <a name="bloch-sphere"></a>Bloch 구

3 차원 단위 구의 점으로 서 단일[비트](xref:microsoft.quantum.glossary#qubit) [퀀텀 상태](xref:microsoft.quantum.glossary#quantum-state) 를 그래픽으로 표현한 것입니다. 자세한 내용은  [Bloch 구를 사용 하 여 다양 한 비트 및 변형 시각화](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere)를 참조 하세요.

## <a name="callable"></a>호출

[ Q# 언어](https://github.com/microsoft/qsharp-language/tree/main/Specifications/Language#q-language)의 [작업](xref:microsoft.quantum.glossary#operation) 또는 [함수](xref:microsoft.quantum.glossary#function) 입니다.
자세한 내용은 [ Q# 프로그램](xref:microsoft.quantum.guide.programs) 을 참조 하세요.

## <a name="clifford-group"></a>Clifford 그룹

[Bloch 구의](xref:microsoft.quantum.glossary#bloch-sphere) octants을 차지 하는 작업 집합과 [pauli 연산자](xref:microsoft.quantum.glossary#pauli-operators)의 효과 순열 여기에는 작업 [ $ X $ ](xref:Microsoft.Quantum.Intrinsic.X), [ $ Y $ ](xref:Microsoft.Quantum.Intrinsic.Y), [ $ Z $ ](xref:Microsoft.Quantum.Intrinsic.Z), [ $ H $ ](xref:Microsoft.Quantum.Intrinsic.H) 및 [ $ S $ ](xref:Microsoft.Quantum.Intrinsic.S)가 포함 됩니다.

## <a name="controlled"></a>제어

대상 작업에 대 한 조력자로 하나 이상의 이상 [비트](xref:microsoft.quantum.glossary#qubit) 를 사용 하는 퀀텀 [작업](xref:microsoft.quantum.glossary#operation) 입니다. 자세한 내용은 [함수 응용 프로그램](xref:microsoft.quantum.qsharp.functorapplication#functor-application)을 참조 하세요.

## <a name="dirac-notation"></a>기타 ac 표기법

*Bra-k* 표기법이 라고도 하는 [퀀텀 상태의](xref:microsoft.quantum.glossary#quantum-state)표현을 간소화 하는 기호화 된 축약형입니다.  *Bra* 부분은 행 벡터 (예: $ \bra { } = \begin{bmatrix} { _1 a _2)를 나타내며 } & { } \end{bmatrix} $ *k* 부분은 열 벡터 $ \ket { b b } = \begin{bmatrix} { _1 } \\\\ b { _2 } \end{bmatrix} $ 를 나타냅니다. 자세한 내용은 [Diac 표기법](xref:microsoft.quantum.concepts.dirac)을 참조 하십시오.

## <a name="eigenvalue"></a>Eigenvalue

변환 응용 프로그램에서 지정 된 변환의 [eigenvector](xref:microsoft.quantum.glossary#eigenvector) 크기를 변경 하는 인수입니다.  사각형 매트릭스가 지정 된 $ 경우 $ $ $ $ Mv = cv를 지정 합니다 $ $ . 여기서 c $ 는 eigenvalue이 고 임의의 인수 수는 eigenvector 수 있습니다. 자세한 내용은 [고급 행렬 개념](xref:microsoft.quantum.concepts.matrix-advanced)을 참조 하세요.

## <a name="eigenvector"></a>Eigenvector

지정 된 변환에서 방향이 변경 되지 않으며 해당 벡터의 [eigenvalue](xref:microsoft.quantum.glossary#eigenvalue)에 해당 하는 요소에 의해 크기가 변경 되는 벡터입니다. 사각형 행렬 $ M $ 과 eigenvalue c를 지정 하 고 $ $ , $ Mv = cv $ 를 지정 $ $ 합니다. 여기서 v는 행렬의 eigenvector이 고 임의의 인수 수를 사용할 수 있습니다. 자세한 내용은 [고급 행렬 개념](xref:microsoft.quantum.concepts.matrix-advanced)을 참조 하세요.

## <a name="entanglement"></a>얽힘

다양 한 방식으로 개별적 [으로 설명할](xref:microsoft.quantum.glossary#qubit)수 없도록 하려는 경우에는 다양 한 것 *과 같은 퀀텀* 파티클을 연결할 수 있습니다. 측정 결과는 무한정 떨어져 있는 경우에도 상관 관계가 지정 됩니다. 되거나 얽 히는 해당 [상태](xref:microsoft.quantum.glossary#quantum-state) 를 [측정](xref:microsoft.quantum.glossary#measurement) 하는 데 필수적입니다.  자세한 내용은 [고급 행렬 개념](xref:microsoft.quantum.concepts.matrix-advanced)을 참조 하세요.

## <a name="epr-pair"></a>EPR 쌍

두 개의 최대 entangled [퀀텀 상태](xref:microsoft.quantum.glossary#quantum-state) 중 [하나입니다.](xref:microsoft.quantum.glossary#qubit) 네 가지 상태는 $ \ket { \beta _ { ij } } = ( \mathbb { 1 } \otimes X ^ iZ ^ j) ( \ket { 00 }  +  \ket { 11 } )/ \sqrt { 2 } $ 로 정의 됩니다. EPR 쌍은 [종 상태](xref:microsoft.quantum.glossary#bell-state) 라고도 합니다.

## <a name="evolution"></a>진화

시간이 지남에 따라 [퀀텀 상태](xref:microsoft.quantum.glossary#quantum-state) 를 변경 하는 방법입니다. 자세한 내용은 [Matrix 지 수](xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials)을 (를) 참조 하세요.

## <a name="function"></a>기능
Q#순수 하 게 결정적 인 언어의 서브루틴 유형입니다. 퀀텀 알고리즘 내에서 함수를 사용 하는 [동안에는](xref:microsoft.quantum.glossary#qubit) 이 함수를 사용 하 여 [작업](xref:microsoft.quantum.glossary#operation)을 호출할 수 없습니다. 자세한 내용은 [ Q# 프로그램](xref:microsoft.quantum.guide.programs) 을 참조 하세요.

## <a name="gate"></a>라는

클래식 논리 게이트의 개념에 따라 특정 한 내장 퀀텀 [작업](xref:microsoft.quantum.glossary#operation)에 대 한 레거시 용어입니다. [퀀텀 회로](xref:microsoft.quantum.glossary#quantum-circuit-diagram) 는 기존 논리 회로의 유사한 개념에 따라 게이트의 네트워크입니다.

## <a name="global-phase"></a>글로벌 단계

두 [상태가](xref:microsoft.quantum.glossary#quantum-state) 복합 숫자 e ^ i의 배수와 동일 하 게 동일한 경우에는 $ { \phi } $ 글로벌 단계에 따라 달라 집니다. 로컬 단계와 달리 전역 단계는 [measurment](xref:microsoft.quantum.glossary#measurement)을 통해 관찰할 수 없습니다. 자세한 내용은 [다음을 참조 하세요.](xref:microsoft.quantum.concepts.qubit)

## <a name="hadamard"></a>Hadamard

Hadamard 연산 (Hadamard gate 또는 transform이 라고도 함)은 단일의 [비트](xref:microsoft.quantum.glossary#qubit) 에서 작동 하 고, [](xref:microsoft.quantum.glossary#superposition) $ \ket { } $ $ \ket { } $ 가 처음에 $ \ket { 0 } $ 상태에 있는 경우에는 0 또는 1의 짝수 superposition에 배치 합니다. 에서 Q# 이 작업은 미리 정의 된 작업에 의해 적용 됩니다 [`H`](xref:Microsoft.Quantum.Intrinsic.H) .

## <a name="immutable"></a>변경할 수 없음

값을 변경할 수 없는 변수입니다. 의 변경할 수 없는 변수는 Q# 키워드를 사용 하 여 생성 됩니다 `let` . 변경할 *수* 있는 변수를 선언 하려면 [mutable](xref:microsoft.quantum.glossary#immutable) 키워드를 사용 하 여를 선언 하 고 키워드를 사용 하 여 `set` 값을 수정 합니다. 

## <a name="measurement"></a>측정

관찰 결과를 생성 하는 데에는 고전적인 비트를 가져오는 것과 같은 이상 [비트](xref:microsoft.quantum.glossary#qubit) (또는 원하는 비트 집합)의 조작입니다. 자세한 내용은 [다음을 참조 하세요.](xref:microsoft.quantum.concepts.qubit#measuring-a-qubit)

## <a name="mutable"></a>변경 가능

값을 만든 후 해당 값을 변경할 수 있는 변수입니다. 에서 변경 가능한 변수는 키워드를 Q# 사용 하 여 선언 되 `mutable` 고 키워드를 사용 하 여 수정 됩니다 `set` . 키워드를 사용 하 여 만든 변수 `let` 는 [변경할](xref:microsoft.quantum.glossary#immutable) 수 없으며 해당 값은 변경할 수 없습니다.

## <a name="namespace"></a>네임스페이스

관련 이름 (예: [작업](xref:microsoft.quantum.glossary#operation), [함수](xref:microsoft.quantum.glossary#function)및 [사용자 정의 형식](xref:microsoft.quantum.glossary#user-defined-type))의 컬렉션에 대 한 레이블입니다. 예를 들어, [네임 스페이스](xref:Microsoft.Quantum.Preparation) 는 초기 상태를 준비 하는 데 도움이 되는 표준 라이브러리에 정의 된 모든 기호에 레이블을 지정 합니다.

## <a name="operation"></a>작업

에서 퀀텀 계산의 기본 단위 Q# 입니다. C, c + + 또는 Python의 함수 또는 c # 또는 Java의 정적 메서드와 거의 동일 합니다. 자세한 내용은 [ Q# 프로그램](xref:microsoft.quantum.guide.programs)을 참조 하세요.

## <a name="oracle"></a>Oracle

런타임에 퀀텀 알고리즘에 데이터 종속 정보를 제공 하는 서브루틴입니다. 일반적으로 superposition에 있는 입력에 해당 하는 출력의 [superposition](xref:microsoft.quantum.glossary#superposition) 을 제공 하는 것이 목표입니다. 자세한 내용은 [Oracles](xref:microsoft.quantum.libraries.data-structures#oracles)를 참조 하세요.

## <a name="partial-application"></a>부분 애플리케이션

모든 필수 입력 없이 [함수](xref:microsoft.quantum.glossary#function) 또는 [작업](xref:microsoft.quantum.glossary#operation) 을 호출 합니다. 그러면 나중에 응용 프로그램에서 제공 하는 누락 된 매개 변수 (밑줄로 표시 됨)만 필요한 새 [호출 가능](xref:microsoft.quantum.glossary#callable) 이 반환 됩니다. 자세한 내용은 [부분 응용 프로그램](xref:microsoft.quantum.qsharp.partialapplication)을 참조 하세요.

## <a name="pauli-operators"></a>Pauli 연산자

`X`, `Y` 및 퀀텀 작업 이라고 하는 3 2 x 2 단일 행렬 집합입니다 `Z` . Id 매트릭스 I는 $ $ 집합에도 포함 되는 경우가 많습니다.  $I = \begin{bmatrix} 1 & 0 \\\\ 0 & 1 \end{bmatrix} $ , $ X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} $ , $ Y = \begin{bmatrix} 0 & -i \\\\ i & 0 \end{bmatrix} $ , $ Z = \begin{bmatrix} 1 & 0 \\\\ & -1 \end{bmatrix} $ .   자세한 내용은 [단일 기능 비트 작업](xref:microsoft.quantum.concepts.qubit#single-qubit-operations)을 참조 하세요.

## <a name="quantum-circuit-diagram"></a>퀀텀 회로 다이어그램

간단한 퀀텀 프로그램의 [게이트](xref:microsoft.quantum.glossary#gate) 시퀀스를 그래픽으로 나타내는 메서드 (예:) 

![샘플 회로 다이어그램](~/media/qpe.png). 

자세한 내용은 [퀀텀 회로](xref:microsoft.quantum.concepts.circuits)를 참조 하세요.

## <a name="quantum-libraries"></a>퀀텀 라이브러리

프로그램을 만들기 위한 [작업](xref:microsoft.quantum.glossary#operation), [함수](xref:microsoft.quantum.glossary#function) 및 [사용자 정의 형식의](xref:microsoft.quantum.glossary#user-defined-type) 컬렉션입니다 Q# . [표준 라이브러리](xref:microsoft.quantum.libraries.standard.intro) 는 기본적으로 설치 됩니다. 사용할 수 있는 다른 라이브러리는 [화학 라이브러리](xref:microsoft.quantum.chemistry.concepts.intro), [숫자 라이브러리](xref:microsoft.quantum.numerics.intro) 및 [Machine learning 라이브러리](xref:microsoft.quantum.machine-learning.concepts.intro)입니다.

## <a name="quantum-state"></a>퀀텀 상태

[측정](xref:microsoft.quantum.glossary#measurement) 확률을 추출할 수 있는 격리 된 퀀텀 시스템의 정확한 상태입니다. 퀀텀 컴퓨팅에서 퀀텀 시뮬레이터는이 정보를 사용 하 여이 작업에 응답 하는 방법을 시뮬레이션 합니다. 자세한 내용은 [다음을 참조 하세요.](xref:microsoft.quantum.concepts.qubit)

## <a name="qubit"></a>고 비트

기존 컴퓨팅의 *비트* 와 유사한 퀀텀 정보의 기본 단위입니다. 자세한 내용은 [다음을 참조 하세요.](xref:microsoft.quantum.concepts.qubit)

## <a name="repeat-until-success"></a>반복-성공-성공

특정 조건이 충족 될 때까지 계산을 반복적으로 적용 하는 것으로 구성 된 퀀텀 알고리즘에서 자주 사용 되는 개념입니다. 조건이 충족 되지 않으면 다음 반복을 시작 하 여 다시 시도 하기 전에 수정이 필요한 경우가 많습니다. 자세한 내용은 [ Q# 사용자 가이드](xref:microsoft.quantum.guide) 를 참조 하세요.

## <a name="standard-libraries"></a>표준 라이브러리

설치 하는 동안 컴파일러와 함께 설치 되는 [작업](xref:microsoft.quantum.glossary#operation), [함수](xref:microsoft.quantum.glossary#function) 및 [사용자 정의 형식](xref:microsoft.quantum.glossary#user-defined-type) 입니다 Q# . 표준 라이브러리 구현은 대상 컴퓨터와는 독립적입니다. 자세한 내용은 [표준 라이브러리](xref:microsoft.quantum.libraries.standard.intro)를 참조 하세요.

## <a name="superposition"></a>Superposition

양자 계산의 [개념은 계산](xref:microsoft.quantum.glossary#qubit) $ \ket { } $ $ \ket { } $ 될 때 [](xref:microsoft.quantum.glossary#measurement)까지 두 상태 (0과 1)의 선형 조합입니다.  자세한 내용은 [퀀텀 컴퓨팅 이해](xref:microsoft.quantum.overview.understanding)를 참조 하세요.

## <a name="target-machine"></a>대상 컴퓨터

추상 퀀텀 프로그램을 하드웨어 또는 시뮬레이션으로 낮추는 컴파일 대상입니다. 여기에는 일반적으로 게이트 교체, 오류 수정 인코딩, 기 하 도형 레이아웃 등을 비롯 한 많은 용도로 다시 쓰기가 포함 됩니다. 자세한 내용은 [퀀텀 시뮬레이터 및 호스트 응용 프로그램](xref:microsoft.quantum.machines)을 참조 하세요.

## <a name="teleportation"></a>순간 이동

[되거나 얽 히](xref:microsoft.quantum.glossary#entanglement) 및 [측정](xref:microsoft.quantum.glossary#measurement)을 사용 하 여 물리적으로 이동 하지 [않고 한 곳에서 다른](xref:microsoft.quantum.glossary#qubit) 위치로 데이터를 다시 생성 하거나 [퀀텀 상태](xref:microsoft.quantum.glossary#quantum-state)를 다시 생성 하는 방법입니다.  자세한 내용은 [퀀텀 회로](xref:microsoft.quantum.concepts.circuits) 및 [퀀텀 Katas](xref:microsoft.quantum.overview.katas)의 각 kata를 참조 하세요.

## <a name="tuple"></a>Tuple

단일 값으로 작동 하는 쉼표로 구분 된 값의 컬렉션입니다. 튜플의 *형식은* 포함 하는 값 형식에 의해 정의 됩니다. 에서 Q# 튜플은 [변경할](xref:microsoft.quantum.glossary#immutable) 수 없으며 중첩 되거나, 배열을 포함 하거나, 배열에 사용 될 수 있습니다. 자세한 내용은 [튜플](xref:microsoft.quantum.qsharp.valueliterals#tuple-literals)을 참조하세요.

## <a name="unitary-operator"></a>단일 연산자

역이 [adjoint](xref:microsoft.quantum.glossary#adjoint)(즉, $ UU ^)와 같은 연산자 { 입니다. \dagger } = \id $

## <a name="user-defined-type"></a>사용자 정의 형식

하나 이상의 명명 된 항목 또는 익명 항목을 포함할 수 있는 사용자 지정 형식입니다. 자세한 내용은 [형식 선언] typedeclarations # 형식 선언을 참조 하세요.
