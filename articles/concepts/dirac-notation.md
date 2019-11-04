---
title: Diac 표기법 | Microsoft Docs
description: 기타 ac 표기법
author: QuantumWriter
uid: microsoft.quantum.concepts.dirac
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 33d964d079c94bd947e35d2c09516b29df1bba11
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2019
ms.locfileid: "73184766"
---
# <a name="dirac-notation"></a>기타 ac 표기법

열 벡터 표기법이 선형 대 수에서 사용 되는 반면 특히 여러 비트를 처리할 때 특히 양자를 계산 하는 것은 복잡 합니다.  예를 들어 $ \psi $를 벡터로 정의 하는 경우 $ \psi $가 행 또는 열 벡터 인지 여부를 명시적으로 명확 하 게 알 수 없습니다.  따라서 $ \\s$ 및 $ \phi $가 벡터 인 경우 $ \\a\psi $의 모양이 컨텍스트에서 명확 하지 않을 수 있기 때문에 $ \\a\psi $가 정의 된 경우에도 마찬가지입니다.  벡터의 모양에 대 한 모호성 외에도 앞에서 소개한 선형 대 수 표기법을 사용 하 여 간단한 벡터를 표현 하는 것은 매우 복잡할 수 있습니다. 예를 들어 각의 비트에 $0 $ 값을 사용 하는 $-하 $n $-에 대 한 설명을 제공 하려는 경우 다음과 같이 공식적으로 상태를 표현 합니다. 

$ $ \begin{bmatrix}1 \\\\ 0 \end{bmatrix}\otimes \cdots \\\\ 0 \end{bmatrix}. $$  

이 텐서 제품을 평가 하는 과정은 벡터가 매우 많은 공간에 있기 때문에 실용적이 지 않으므로이 표기법이 이전 표기법을 사용 하 여 제공할 수 있는 상태에 대 한 최상의 설명입니다.  

[*Diac 표기법*](https://en.wikipedia.org/wiki/Bra%E2%80%93ket_notation) 은 퀀텀 메커니즘의 정확한 요구에 맞게 새로운 언어를 제공 하 여 이러한 문제를 해결 합니다.  이러한 이유로 독자는이 섹션의 예제를 퀀텀 상태를 설명 하는 방법의 고정 prescription 하는 것이 좋지만 퀀텀 아이디어를 간결 하 게 표현 하는 데 사용할 수 있는 제안 사항으로이를 확인 하는 것이 좋습니다.

단일 Ac 표기법에는 두 가지 유형의 벡터가 있습니다. *bra* vector와 *k* vector는 함께 배치 될 때 *braket* 또는 inner 곱을 형성 하기 때문에 이름이 지정 됩니다.  $ \Psi $가 열 vector 인 경우 $ \ket{\psi} $로이를 Vac 표기법으로 작성할 수 있습니다. 여기서 $ \ket{\cdot} $은 단위 열 벡터 (즉, *k* vector) 임을 나타냅니다.  마찬가지로, $ \psi ^ \psi $ 행은 $ \bra{\psi} $로 표시 됩니다. 즉, $ \psi ^ \psi $은 $ \psi $의 요소에 대 한 초급 복합 적용 하 여 가져옵니다. Bra-k notation은 $ \braket{\psi | \psi} $가 정의 $1 $를 기준으로 하는 vector $ \psi $의 내부 곱 임을 의미 합니다.  

더 일반적으로 $ \psi $ 및 $ \s$이 퀀텀 상태 벡터 인 경우 해당 내부 제품은 $ \braket{\phi | \psi} $입니다 .이는 $ \ket{\psi} $를 $ \ket{\phi} $로 측정 하는 확률이 $ | \braket{\phi | \psi} | ^ 2 $ 일 수 있음을 의미 합니다.  

다음 규칙은 0과 1의 값을 인코딩하는 퀀텀 상태를 설명 하는 데 사용 됩니다 (단일 값 비트 계산 기준 상태).

$ $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} = \ket{0}, \qquad \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} = \ket{1}.
$$

### <a name="example-representing-the-hadamard-operation-with-dirac-notation"></a>예:가 중 Ac 표기법으로 Hadamard 작업 표현

다음 표기법은 Hadamard gate를 $ \ket{0}$ 및 $ \ket{1}$에 적용 하 여 발생 하는 상태를 설명 하는 데 주로 사용 됩니다 .이는 Bloch 구에 있는 $ + x $ 및 $-x $의 단위 벡터에 해당 합니다.

$ $ \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\\\ 1 \end{bmatrix} = H\ket{0} = \ket{+}, \qquad \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\\\-1 \end{bmatrix} = H\ket{1} = \ket{-}.
$$

이러한 상태를 $ \ket{0}$ 및 $ \ket{1}$의 합으로 사용 하 여 확장할 수도 있습니다.

$ $ \ket{+} = \frac{1}{\sqrt{2}} (\ket{0} + \ket{1}), \qquad \ket{-} = \frac{1}{\sqrt{2}} (\ket{0}-\ket{1}).
$$

### <a name="computational-basis-vectors"></a>계산 기준 벡터
이러한 상태를 종종 *계산 기준*이라고 하는 이유를 보여 줍니다. 모든 퀀텀 상태는 항상 계산 기준 벡터의 합계로 표현 될 수 있으며 이러한 합계는 기타 ac 표기법을 사용 하 여 쉽게 표현 됩니다.  또한 $ \ket{+} $ 및 $ \ket{-}$ 상태는 퀀텀 상태의 기반을 형성 한다는 것에도 마찬가지입니다.  이 사실을 확인할 수 있습니다.

$ $ \ket{0} = \frac{1}{\sqrt{2}} (\ket{+} + \ket{-}), \qquad \ket{1} = \frac{1}{\sqrt{2}} (\ket{+}-\ket{-}).
$$

나머지 Ac 표기법의 예로, $0 $과 $1 $ 사이의 내부 제품인 braket $ \braket{0 | 1} $를 생각해 보세요.  다음으로 작성 될 수 있습니다. 

$ $ \braket{0 | 1} = \begin{bmatrix} 1 & 0 \end{bmatrix}\begin{bmatrix}0\\\\ 1 \ end {bmatrix} = 0. $ $

즉, $ \ket{0}$ 및 $ \ket{1}$는 직교 벡터입니다. 즉, $ \braket{0 | 1} = \braket{1 | 0} = $0입니다.  또한 정의 $ \braket{0 | 0} = \braket{1 | 1} = 1 $로 계산 됩니다. 즉, 두 계산 기준 벡터를 *orthonormal*호출할 수도 있습니다.
이러한 orthonormal 속성은 다음 예제에서 유용 합니다. 상태 $ \ket{\psi} = {\frac{3}{5}} \ket{1} + {\frac{4}{5}} \ket{0}$ then. $ \braket{1 | 0} = $0 때문에 $1 $ 측정 확률  

$ $ \big | \braket{1 | \psi}\big | ^ 2 = \big | \frac{3}{5}| 1} + \frac{4}{5}\braket{1 | 0} \big | ^ 2 = \frac{9}{25}. $ $ 

### <a name="tensor-product-notation"></a>텐서 product 표기법
또한 내부에는 암시적인 텐서 product 구조가 포함 됩니다.  이는 퀀텀 컴퓨팅에서 두 개의 상관 관계가 없는 퀀텀 레지스터에 설명 된 상태 벡터가 두 상태 벡터의 텐서 제품 이기 때문에 중요 합니다.  퀀텀 계산을 설명 하려면 텐서 제품 구조를 간결 하 게 설명 하거나 그에 대 한 이해가 중요 합니다.  텐서 제품 구조는 두 개의 퀀텀 상태 벡터 $ \as$ 및 $ \bs$ as $ \ket{\psi} \ket{\phi} $로 $ \ccooatimes $를 작성할 수 있습니다. 그러나 경우에 따라 $ \ket{\psi} \otimes \ket{\phi} $로 명시적으로 작성 된 규칙에 따라 $ \otimes $를 작성 합니다. 는 벡터 사이에서 필요 하지 않습니다.  예를 들어 0 상태로 초기화 된 두 개의 상태를 제공 하는 상태는

$ $ \begin{bmatrix} 1 \\\\ 0 \\\\ 0 \\\\ 0 \end{bmatrix} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} = \ket{0} \ otimes \ket{0}= \ket{0} \ket{0}.
$$

마찬가지로 $ \ket{p} $ for integer $p $는 정수 $p $를 이진 표현으로 인코딩하는 퀀텀 상태를 나타냅니다.  예를 들어, 부호 없는 이진 인코딩을 사용 하 여 숫자 $5 $를 표현 하려는 경우에는 동일 하 게 표현할 수 있습니다.

$ $ \ket{1}\ket{0}\ket{1} = \ket{101} = \ket{5}.
$$

이 표기법 내에서 $ \ket{0}$은 단일가 나 비트 상태를 참조할 필요는 없으며 이진 인코딩을 $0 $ *로 저장 하는 것* 이 라 합니다.  이러한 두 표기법 간의 차이점은 일반적으로 컨텍스트에서 명확 합니다.  이 규칙은 다음 중 한 가지 방법으로 작성할 수 있는 첫 번째 예제를 간소화 하는 데 유용 합니다.

$ $ \begin{bmatrix}1 \\\\ 0 \end{bmatrix}\otimes \cad\otimes\begin{bmatrix}1 \\\\ 0 \end{bmatrix} = \ket{0} \oatimes \cst\otimes \ket{0}= | 0 \ c도트 0 \ rangle = \ket{0}^ {\cdots n} = \ket{0}.
$$

### <a name="example-describing-superposition-with-dirac-notation"></a>예:가 중 Ac 표기법을 사용 하 여 superposition 설명
Diac 표기법을 사용 하 여 퀀텀 상태를 설명 하는 방법에 대 한 또 다른 예로, $n $의 가능한 모든 비트 문자열에 대해 동일한 superposition 퀀텀 상태를 작성 하는 다음과 같은 방법을 고려해 보십시오.

$ $ H ^ {\otimes n} \ket{0} = \otimes{1}{2 ^ {n/2}} \sum_{j = 0} ^ {2 ^ n-1} \ket{j} = \ket{+} ^ {\otimes n}.
$$

여기서 sum이 $n $ bits에 대해 $0 $에서 $2 ^ {n}-$1로 이동 하는 이유를 궁금할 수 있습니다.  먼저 $2 ^ {n} $ $n $ bits에서 수행할 수 있는 다른 구성이 있는지 확인 합니다.  한 비트에서 $2 $ 값을 사용할 수 있지만 두 비트가 $4 $ 값을 사용할 수 있다는 것을 확인 하 여이를 확인할 수 있습니다. 일반적으로 $2 ^ n $ 가능한 다른 비트 문자열이 있지만 그 중에서 가장 큰 값은 $1 \ cdots 1 = 2 ^ n-$1로 인코딩된 것 이므로 합계의 상한입니다.
이 예에서는 \ket{+} ^ {\otimes n} = \ket{+} $를 $ \ket{0}^ {\otimes n} = \ket{0}$과 (와) 비교 하 여 사용 하지 않았습니다 .이 표기법 밑수 규칙은 일반적으로 0으로 초기화 된 모든 비트와 함께 계산 기준 상태에 예약 되기 때문입니다.  이러한 규칙은이 경우에 유용 하지만 퀀텀 컴퓨팅 자료에서 사용 되지 않습니다.

### <a name="expressing-linearity-with-dirac-notation"></a>Diac 표기법으로 선형 표현
뛰어난 Ac 표기법의 또 다른 유용한 기능은 선형 이라는 점입니다.  네 가지 퀀텀 상태 벡터에 대해 작성 하려는 경우 

$ $ (\alpha \ket{\psi} + \beta\ket{\phi}) \otimes (\alpha \ket{\chi} + \alpha \ket{\omega}) = \alpha\gamma \ket{\psi}\ket{\chi} + \alpha\delta \ket{\psi}\ket{\omega} + \beta\gamma\ket{\phi}\ket{\chi} + \beta\delta\ket{\phi}\ket{\omega}. $ $

즉, 상태 벡터 사이에 텐서 제품을 가져오는 것이 일반적인 곱셈 처럼 종료 되도록 텐서 제품 표기법을 Diac 표기법으로 배포할 수 있습니다.

Bra 벡터는 비슷한 규칙에 따라 벡터를 k 합니다.  예를 들어 vector $ \bra{\psi}\bra{\phi} $는 상태 vector $ \psi ^ \aa\otimes \a^ \aatime \aa^ \aa> (\psi\otimes \psi) ^ \a와 동일 합니다. K vector $ \ket{\psi} $이 $ \alpha \ket{0} + \alpha \ket{1}$ 이면 vector의 bra vector 버전은 $ \bra{\psi} = \ket{\psi} ^ \alpha = (\bra{0}\alpha ^ * +{1}\alpha ^ *) $입니다.

예를 들어, $ \ket{\psi} = \frac{3}{5} \ket{1} + \frac{4}{5} \ket{0}$ 상태를 측정 하는 확률을 계산 하려고 한다고 가정 합니다.{-}$. 그런 다음 장치에서 상태가 $ \ket{-}$로 출력 될 확률은 다음과 같습니다. 

$ $ | \braket{-| \psi} | ^ 2 = \left | \frac{1}{\left{2}} (\bra{0}-\bra{1}) (\frac{3}{5} \ket{1} + \frac{4}{5} \ket{0}) \left | ^ 2 = \left |-\frac{3}{5 \ sqrt{2}} + \frac{4}{5 \ sqrt{2}} \right | ^ 2 = \frac{1}{50}. $ $

확률을 계산 하는 데 음수 기호가 표시 되는 사실은 퀀텀 간섭의 노력입니다 .이는 퀀텀 컴퓨팅이 기존 컴퓨팅 보다 이점을 얻는 메커니즘 중 하나입니다.

## <a name="ketbra-or-outer-product"></a>ketbra 또는 외부 제품
마지막 항목은 *ketbra* 또는 외부 제품입니다.  외부 제품은는 Diac 표기법 내에서 $ \ket{\psi} \bra{\phi} $로 표시 되며 bras 및 kets가 brakets와 반대 순서로 발생 하기 때문에 ketbras 라고도 합니다.  외부 제품은 행렬 곱하기를 $ \ket{\psi} \bra{\phi} = \psi \sa^ \aa$로 정의 합니다.  이 표기법의 가장 일반적인 예는 다음과 같습니다.

$ $ \ket{0} \bra{0} = \begin{bmatrix}1\\\\ 0 \end{bmatrix}\begin{bmatrix}1 & 0 \end{bmatrix} = \begin{bmatrix}1 & 0\\\\ 0 & 0 \ end {bmatrix} \qquad \ket{1} \bra{1} = \begin{bmatrix}0\\\\ 1 \end{bmatrix}\begin{bmatrix}0 & 1 \end{bmatrix} = \begin{bmatrix}0 & 0\\\\ 0 & 1 \ 끝 {bmatrix}.
$$

Ketbras는 고정 값에 퀀텀 상태를 프로젝션 하기 때문에 종종 프로젝터 라고 합니다.  이러한 작업은 단일가 아니지만 벡터의 표준을 유지 하지 않으므로 퀀텀 컴퓨터에서 프로젝터를 명확 하 게 적용할 수 없다는 것이 놀라운 것은 아닙니다.  그러나 프로젝터가 퀀텀 상태에 대해 측정 하는 작업을 설명 하는 작업을 수행 합니다.  예를 들어 $ \ket{\psi} $ 상태를 $0 $로 측정 한 후에는 상태를 측정 결과로 사용할 경우의 결과 변환은

  $ $ \ket{\psi} \rightarrow \frac{(\ket{0} \bra{0}) \ket{\psi}}{| \braket{0 | \psi} |} = \ket{0}, $ $

상태를 측정 하 고 $ \ket{0}$로 확인 하는 경우를 가정 합니다.  즉, 이러한 프로젝터는 퀀텀 컴퓨터의 상태에 따라 명확 하 게 적용할 수 없습니다.  대신, 몇 가지 고정 확률로 표시 되는 $ \ket{0}$ 결과와 함께 임의로 임의로 적용할 수 있습니다.  이러한 측정의 확률은 상태에서 퀀텀 프로젝터의 예상 값으로 작성 될 수 있습니다.

$ $ \bra{\psi} (\ket{0} \bra{0}) \ket{\psi} = | \braket{\psi | 0} | ^ 2, $ $

이는 프로젝터가 측정 프로세스를 표현 하는 새로운 방법을 제공 한다는 것을 보여 줍니다.

대신, multi-factor bit 상태의 첫 번째 비트를 $1 $로 측정 하는 것을 고려 하는 경우에는이 프로세스를 프로젝터 및 기타 Ac 표기법을 사용 하 여 편리 하 게 설명할 수도 있습니다.

$ $ P (\text{first stbit = 1}) = \bra{\psi}\left (\ket{1}\bra{1}\otimes \boldone ^ {\otimes n-1} \right) \ket{\psi}.
$$

여기에서 id 매트릭스는 다음과 같이 다른 것 처럼 편리 하 게 작성할 수 있습니다.

$ $ \boldone = \ket{0} \bra{0}+ \ket{1} \bra{1}= \begin{bmatrix}1 & 0\\\\ 0 & 1 \end{bmatrix}.
$$

다음과 같이 두 가지 비트가 있는 경우에는 프로젝터를 확장할 수 있습니다. 

$ $ \ket{1} \bra{1} \otimes \id = \ket{1}\bra{1} \otimes (\ket{0} \bra{0}+ \ket{1} \bra{1}) = \ket{10}\bra{10} + \ket{11}\bra{11}.
$$

그러면 열 벡터 표기법을 사용 하 여 다중 기능에 대 한 측정 유사도에 대 한 논의와 일치 하는 것을 알 수 있습니다.

$ $ P (\text{first stbit = 1}) = \psi ^ \text{first e\_{10}e\_{10}^ \text{first e\_{11}\_e {11}\_^ \a) \psi = | e {10}\_^ \ka\psi | ^ 2 + | e {11}^ \ 칼 표 | ^ 2, $ $

이는 여러 기능을 비교 하는 데 적합 합니다.  그러나이 결과의 일반화는 다중 기능 비트 사례에 대 한 일반화는 열 벡터 표기법 보다는 Diac 표기법을 사용 하는 것이 약간 더 간단 하며 이전 처리와 완전히 동일 합니다.

## <a name="density-operators"></a>밀도 연산자

다른 유용한 연산자는 *상태 연산자*라고도 하는 *밀도 연산자*를 사용 하 여 표현할 수 있습니다.
퀀텀 상태 벡터의 밀도 연산자는 $ \rho = \ket{\psi} \bra{\psi} $ 형식으로 사용 합니다.
벡터 대신 매트릭스로 상태를 표시 하는 이러한 개념은 확률 계산을 표현 하는 편리한 방법을 제공 하 고 통계 불확실성과 퀀텀 불확실성을 모두 설명 하는 데 사용할 수 있기 때문에 편리한 경우가 많습니다. 동일한 정해진 내에 있습니다.
벡터 대신 일반 퀀텀 상태 연산자는 일부 퀀텀 컴퓨팅 영역에서 사용할 수 있지만 필드의 기본 사항을 이해 하는 데에는 필요 하지 않습니다.
관심이 있는 독자의 경우에서 제공 하는 참조 서적 중 하나를 참조 하 여 [자세한 내용을](xref:microsoft.quantum.more-information)참조 하세요.

## <a name="q-gate-sequences-equivalent-to-quantum-states"></a>Q # 퀀텀 상태와 동일한 게이트 시퀀스
최종 지점에서 퀀텀 표기법 및 Q # 프로그래밍 언어를 발생 시킬 수 있습니다 .이 문서의 하기 시작 하면에서 퀀텀 상태는 퀀텀 컴퓨팅에서 정보의 기본적인 개체 라고 언급 했습니다.  그러면 Q #에서 퀀텀 상태에 대 한 개념이 없습니다.  대신 모든 상태는이를 준비 하는 데 사용 되는 작업에 의해서만 설명 됩니다.  위의 예제는이에 대 한 훌륭한 그림입니다.  레지스터의 모든 퀀텀 비트 문자열에 대해 균일 한 superposition을 표현 하는 대신 ^ {\otimes n} \ket{0}$ $H로 결과를 나타낼 수 있습니다.  이에 대 한 이유를 일반적으로 수 있는 이점 뿐만 아니라이에 대 한 정보를 제공 하는 것은 매우 간단 하지만, 알고리즘을 구현 하기 위해 소프트웨어 스택을 통해 전파 해야 하는 작업도 간결 하 게 정의 합니다.  이러한 이유로 Q #은 퀀텀 상태 대신 게이트 시퀀스를 내보내도록 설계 되었습니다. 그러나 이론적 수준에서 두 큐브 뷰는 동일 합니다.

