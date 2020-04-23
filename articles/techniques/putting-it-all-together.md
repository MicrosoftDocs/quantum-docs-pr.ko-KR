---
title: 'Q # 기술 - 모든 것을 함께 넣어'
description: 양자 텔레포트를 보여 주는 기본 Q# 프로그램을 안내합니다.
uid: microsoft.quantum.techniques.puttingittogether
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4bd91699017e4c1acd9f4449b8a65e39bd07878e
ms.sourcegitcommit: b6b8459eb654040f1e19f66411b29fc9e48e95c9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/22/2020
ms.locfileid: "82030568"
---
# <a name="putting-it-all-together-teleportation"></a>모든 것을 하나로 모으기: 순간 이동 #
[양자](xref:microsoft.quantum.concepts.circuits)회로에 정의된 순간 이동 회로의 예로 돌아가보겠습니다. 지금까지 배운 개념을 설명하기 위해 이 것을 사용할 것입니다. 양자 텔레포트에 대한 설명은 이론에 익숙하지 않은 사람들을 위해 아래에 제공되며 Q#의 코드 구현에 대한 연습이 뒤따릅니다. 

## <a name="quantum-teleportation-theory"></a>양자 순간 이동: 이론
양자 텔레포트는 알 수없는 양자 상태를 보내는 기술입니다 (우리는 __'메시지'로__참조됩니다) 다른 위치에 있는 큐빗에 한 위치에서 qubit에서 (우리는 __'여기'와____'이 ',__ 각각'로 이러한 큐빗을 참조합니다). 우리는 Dirac 표기법을 사용하여 벡터로 __메시지를__ 나타낼 수 있습니다. 

$$ \ket{\psi} = \알파\케트{0} {1} + \베타\케트 $$

우리가 $\alpha$ 및 $\beta$의 값을 모르기 때문에 __메시지__ qubit의 상태는 우리에게 알려지지 않습니다.

### <a name="step-1-create-an-entangled-state"></a>1단계: 얽힌 상태 만들기
__메시지를__ 보내기 위해 우리는 __여기에__ 큐빗이 __큐빗과__얽히도록 필요한 데 필요한 . 이것은 하다마르 게이트를 적용하고 CNOT 게이트를 적용하여 달성됩니다. 이러한 게이트 작업의 배후에 있는 수학을 살펴보겠습니다.

우리는 __여기__ __저기__ qubits로 시작됩니다 모두{0}$\ket $ 상태. 이러한 qubits를 얽히게 한 후, 그들은 상태에 있습니다 :

$$ \ket{\phi^+} ={1}\frac{2}{\sqrt{00} }(\ket + \ket){11}$$

### <a name="step-2-send-the-message"></a>2단계: 메시지 보내기
__메시지를__ 보내려면 먼저 __메시지__ 큐빗이있는 CNOT 게이트를 __적용하고__ 여기에 qubit을 입력으로 적용합니다 __(메시지__ 큐빗은 컨트롤이고 __여기에__ 는 큐빗은 대상 큐빗입니다). 이 입력 상태를 작성할 수 있습니다.

$$ \ket{\psi}\ket{\phi^+} ={0} (\알파\케트{1}+ \베타\케트)(\frac{1}{2}{\sqrt }(\ket{00} + \ket)){11}$$

이 확장으로 확장됩니다.

$$ \ket{\psi}\ket{\phi^+}{2}= \frac{{\alpha}=\sqrt }\sqrt{000} }\sqrt{2}{011} } \frac{\beta}{sqrt{2}} \frac{{beta}{sqrt{100} {2}}{111}

제어 큐빗이 1일 때 CNOT 게이트가 대상 큐빗을 뒤집습니다. 예를 들어 $\ket{000}$의 입력은 첫 번째 큐빗(컨트롤)이 0이므로 변경되지 않습니다. 그러나 첫 번째 큐빗이 1인 경우(예: $\ket{100}$)의 입력을 예로 들어 보겠습니다. 이 경우 두 번째 큐빗(대상)이 CNOT 게이트에서 뒤집히면 출력은 $\ket{110}$입니다.

이제 CNOT 게이트가 위의 입력에 작용하면 출력을 고려해 보겠습니다. 결과는 다음과 같습니다.

{2}$$ \frac{\알파}{\sqrt }\ket{000} + \frac{{\alpha}{\sqrt }\sqrt{2}{011} }\sqrt }\sqrt{2}{110} }{\sqrt{2}$${101}

__메시지를__ 보내는 다음 단계는 __메시지__ 큐빗에 Hadamard 게이트를 적용하는 것입니다(각 용어의 첫 번째 큐빗임). 

다시 한 번 하다마르 문은 다음과 같은 작업을 수행합니다.

입력 | 출력
---------------------------| ---------------------------------------------------------------
$\ket{0}$  | $\frac{1}{\sqrt{2}}(\케트{0} + \케트)${1}
$\ket{1}$  | $\frac{1}{\sqrt{2}}(\케트{0} - \케트)${1}

위의 출력의 각 용어의 첫 번째 큐빗에 Hadamard 게이트를 적용하면 다음과 같은 결과를 얻을 수 있습니다.

$${2}\frac{\알파}{\sqrt }(\frac {\sqrt }(\frac{1}{\sqrt})\케트{2}{0} {1}+\ket{00} + \frac{\alpha}{\sqrt }(\frac {\sqrt{2}}(\frac{1}{sqrt{2}}\ket +{2}\ket))\ket{1}{10} {2}{1}{2}{0} {1}{01} {0} {1}{11} + \frac{\beta}{\sqrt{2}}(\frac {\sqrt }(\frac{1}{\sqrt})\케트{0} +\frac{\sqrt }(\frac {\sqrt })\켓 $$

각 용어에는 두 개의 $\frac{1}{\sqrt{2}}$ 요인이 있습니다. 우리는 다음과 같은 결과를 주는 이러한 곱할 수 있습니다.

$${2}\frac{\alpha} (\케트{0} +{1}{00} \케트 + \frac{\alpha}{2}{0} {1}(\케트 + \ket)\ket{11} + \frac{beta}{2}(\ket{0} -{2}\ket)\케트{1}{1}+{01} \ket{10} + \ket } (\ket{0} - \ket)

$\frac{1}{2}$ 요인은 각 용어에 공통적이므로 이제 대괄호 외부로 가져 갈 수 있습니다.

$$ frac{1}{2}{0} \frac \big[\ket{1}+ \ket +ket /ket{00} /ket +{11} \alpha(\ket{0} {0} + \ket + \ket{1}/{0} \ket{1}-{01}\ket - \ket -\ket)\ket{1}{10} + beta (\ket - \ket)\ket \ket \ket \ket\ket \tn@$$

그런 다음 각 용어에 대한 괄호를 곱할 수 있습니다.

$$ frac{1}{2}\frac{000} \big[\alpha\ket{100} + \alpha\ket +{111} \alpha\ket{010} + \alpha\ket{011} - \beta\ket +{101}\beta\ket{110} + \beta\ket{001} - \beta\ket \ 큰] $$

### <a name="step-3-measure-the-result"></a>3단계: 결과 측정

여기 __저기__ 얽히기 때문에 __여기에__ 있는 모든 측정은 __there__ __이__곳의 상태에 영향을 미칩니다. 우리는 첫 번째와 두 번째 qubit을 측정하는 경우 __(메시지와__ __여기에)__ 우리는 얽힘의이 속성으로 인해, 거기에 어떤 __상태를__ 배울 수 있습니다. 

* 결과 00을 측정하고 받으면 중첩이 축소되어 이 결과와 일치하는 용어만 남깁니다. 그건 $\알파\ket{000} +\베타\케트{001}$. 이것은 $\ket{00}(\알파\ket{0} +\beta\ket)$로{1}리팩터링될 수 있습니다. 따라서 첫 번째 와 두 번째 큐빗을 00으로 측정하면 세 번째 큐비트가 $(\alpha\ket __there__{0} +\beta\ket)에{1}있다는 것을 알고 있습니다.
* 결과 01을 측정하고 얻을 경우 중첩이 축소되어 이 결과와 일치하는 용어만 남깁니다. 그건 $\알파\ket{011} +\베타\케트{010}$. 이것은 $\ket{01}(\알파\ket{1} +\beta\ket)$로{0}리팩터링될 수 있습니다. 따라서 첫 번째 와 두 번째 큐빗을 01로 측정하면 세 번째 큐비트가 $(\alpha\ket __there__{1} +\beta\ket)에{0}있다는 것을 알고 있습니다.
* 결과를 측정하고 결과 10을 얻으면 중첩이 축소되어 이 결과와 일치하는 용어만 남깁니다. 그건 $\알파\ket{100} -\베타\케트{101}$. 이것은 $\ket{10}(\알파\ket{0} -\beta\ket)$로{1}리팩터링될 수 있습니다. 따라서 첫 번째 와 두 번째 큐빗을 10으로 측정하면 세 번째 큐비트가 $(\alpha\ket __there__{0} -\beta\ket)에{1}있다는 것을 알고 있습니다.
* 결과를 측정하고 얻을 경우 11, 중첩이 붕괴되고 이 결과와 일치하는 용어만 남깁니다. 그건 $\알파\ket{111} -\베타\케트{110}$. 이것은 $\ket{11}(\알파\ket{1} -\beta\ket)$로{0}리팩터링될 수 있습니다. 따라서 첫 번째 와 두 번째 큐빗을 11로 측정하면 세 번째 큐비트가 $(\alpha\ket __there__{1} -\beta\ket)에{0}있다는 것을 알고 있습니다.

### <a name="step-4-interpret-the-result"></a>4단계: 결과 해석

다시 한 번 말씀드리자면, 우리가 보내고자 했던 원래 __메시지는__ 다음과 같은 것이었습니다.

$$ \ket{\psi} = \알파\케트{0} {1} + \베타\케트 $$

수신된 상태가 의도된 상태가 되도록 __이__ 상태로 큐빗을 입력해야 합니다. 

* 우리가 측정하고 00의 결과를 얻었다면, 세 번째 qubit은 $ (\alpha\ket __there__{0} +\beta\ket)$에{1}있습니다. 이 메시지는 의도한 __메시지이기__때문에 변경할 필요가 없습니다.
* 우리가 측정하고 01의 결과를 얻었다면, 세 번째 qubit은 $ (\alpha\ket __there__{1} +\beta\ket)$에{0}있습니다. 이것은 의도 된 __메시지와__다르지만 NOT 게이트를 적용하면 원하는 상태 $(\alpha\ket{0} {1}+\beta\ket)$을 제공합니다.
* 우리가 측정하고 10의 결과를 얻었다면, 세 번째 qubit, __거기에__, 상태에{0} $(\알파\ket -\beta\ket)$입니다.{1} 이것은 의도 된 __메시지와__다르지만 Z 게이트를 적용하면 원하는 상태 $(\alpha\ket{0} {1}+\beta\ket)$을 제공합니다.
* 우리가 측정하고 11의 결과를 얻었다면, 세 번째 qubit, __거기에__, 상태에{1} $(\알파\ket -\beta\ket)$입니다.{0} 이것은 의도 된 __메시지와__다르지만 Z 게이트 다음에 NOT 게이트를 적용하면 원하는 상태{0} $(\alpha\ket{1}+\beta\ket)$을 제공합니다.

요약하면, 우리가 측정하고 첫 번째 큐빗이 1이면 Z 게이트가 적용됩니다. 측정하면 두 번째 큐빗이 1이면 NOT 게이트가 적용됩니다.

### <a name="summary"></a>요약
아래는 순간 이동을 구현하는 텍스트 북 양자 회로입니다. 왼쪽에서 오른쪽으로 이동하면 다음을 볼 수 있습니다.
- 1 단계 : 하다마드 게이트와 CNOT 게이트를 적용하여 __여기저기__ 얽히게하십시오. __there__
- 2단계: CNOT 게이트와 하다마르드 게이트를 사용하여 __메시지__ 보내기.
- 3 단계 : 첫 번째 및 두 번째 큐빗, __메시지__ 및 여기에 대한 측정을 __수행합니다.__
- 4 단계 : 3 단계에서 측정 결과에 따라 NOT 게이트 또는 Z 게이트를 적용합니다.

!['텔레포트 (msg : Qubit, 거기 : 큐빗) : 단위'](~/media/teleportation.svg)

## <a name="quantum-teleportation-code"></a>양자 순간 이동: 코드

우리는 양자 순간 이동을위한 우리의 회로를 가지고 :

!['텔레포트 (msg : Qubit, 거기 : 큐빗) : 단위'](~/media/teleportation.svg)

이제 이 양자 회로의 각 단계를 Q#으로 변환할 수 있습니다.

### <a name="step-0-definition"></a>단계 0: 정의
우리는 순간 이동을 수행 할 때, 우리는 우리가 보내고 싶은 __메시지를__ 알고 있어야합니다, 우리는 그것을 보낼 위치를 __(거기).__ 이러한 이유로 두 큐빗을 인수로 `msg` `there`지정하는 새 Teleport 작업을 정의하는 것으로 시작합니다.

```qsharp
operation Teleport(msg : Qubit, there : Qubit) : Unit {
```

우리는 또한 우리가 블록으로 `here` 달성 하는 큐빗을 `using` 할당 해야:

```qsharp
    using (here = Qubit()) {
```

### <a name="step-1-create-an-entangled-state"></a>1단계: 얽힌 상태 만들기
그런 `here` 다음 `there` @"microsoft.quantum.intrinsic.h" and @"microsoft.quantum.intrinsic.cnot" 작업을 사용하여 얽힌 쌍을 만들 수 있습니다.

```qsharp
        H(here);
        CNOT(here, there);
```

### <a name="step-2-send-the-message"></a>2단계: 메시지 보내기
그런 다음 다음 다음 $\operatorname{CNOT}$를 사용하고 $H$ 게이트를 사용하여 메시지 큐빗을 이동합니다.

```qsharp
        CNOT(msg, here);
        H(msg);
```

### <a name="step-3--4-measuring-and-interpreting-the-result"></a>3단계 & 4: 결과 측정 및 해석
마지막으로, 우리는 @"microsoft.quantum.intrinsic.m" `if` 측정을 수행하고 문으로 표시된 대로 원하는 상태를 얻기 위해 필요한 게이트 작업을 수행하는 데 사용합니다.

```qsharp
        // Measure out the entanglement
        if (M(msg) == One)  { Z(there); }
        if (M(here) == One) { X(there); }
```

### <a name="step-5-restarting-the-qubit-register"></a>5단계: 큐빗 레지스터 다시 시작

모든 Q # 작업의 끝에서 우리는 상태에서 qubits을 할 필요가{0}$\ket $. 우리는 제로 @"microsoft.quantum.intrinsic.reset" 상태로 모든 큐빗을 다시 시작하는 데 사용할 수 있으며,이 우리의 작업을 완료합니다.

```qsharp
        Reset(msg);
        Reset(here);
        Reset(there);
    }
}
```


