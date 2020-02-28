---
title: 'Q # 기술-모두 함께 배치'
description: '퀀텀 teleportation을 보여 주는 기본 Q # 프로그램을 안내 합니다.'
uid: microsoft.quantum.techniques.puttingittogether
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 6c988f77ef6e433945dbf21dfb41204c74bdda3e
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906834"
---
# <a name="putting-it-all-together-teleportation"></a>모두 함께 배치: Teleportation #
[퀀텀 회로](xref:microsoft.quantum.concepts.circuits)에 정의 된 teleportation 회로의 예제로 돌아가 보겠습니다. 지금까지 배운 개념을 설명 하는 데이 방법을 사용할 예정입니다. 퀀텀 teleportation에 대 한 설명은 아래에 설명 되어 있으며, 그 다음에는 Q #의 코드 구현 연습이 제공 됩니다. 

## <a name="quantum-teleportation-theory"></a>퀀텀 Teleportation: 이론
퀀텀 teleportation은 알 수 없는 퀀텀 상태 ('__메시지__' 라고 함)를 한 위치에 있는 특정 위치에서 다른 위치에 있는 이상으로 전송 하는 기술입니다 (각각 ' 여기 ' 및 '__여기__ __'로__표시 됨). __메시지__ 는 다음과 같이 diac 표기법을 사용 하 여 벡터로 나타낼 수 있습니다. 

$ $ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $ $

$ \Alpha $ 및 $ \alpha $ 값을 알 수 없으므로 __메시지__ 의 상태를 알 수 없습니다.

### <a name="step-1-create-an-entangled-state"></a>1 단계: entangled 상태 만들기
__메시지__ 를 보내려면 __여기__ 에는 원하는 비트를 사용 하 여이를 위한 것이 __좋습니다.__ 이는 Hadamard 게이트를 적용 하 고 CNOT 게이트를 적용 하 여 수행 됩니다. 이러한 게이트 작업 뒤의 수치를 살펴보겠습니다.

__여기서는 여기에 나와__ 있는 것과 $ \ket{0}$ 상태 모두로 시작 합니다. 이러한 entangling 후에는 상태가 됩니다.

$ $ \ket{\phi ^ +} = \frac{1}{\sqrt{2}} (\ket{00} + \ket{11}) $ $

### <a name="step-2-send-the-message"></a>2 단계: 메시지 보내기
__메시지__ 를 보내려면 먼저 __메시지__ 를 사용 하 여 cnot gate를 적용 합니다. __여기서__ 는 (컨트롤이 제어 하는 데 사용 되는 __메시지__ 이 고, __여기서__ 는이 인스턴스에서 대상의 비트입니다.) 이 입력 상태를 작성할 수 있습니다.

$ $ \ket{\psi}\ket{\phi ^ +} = (\alpha\ket{0} + \beta\ket{1}) (\frac{1}{\sqrt{2}} (\ket{00} + \ket{11})) $ $

다음과 같이 확장 됩니다.

$ $ \ket{\psi}\ket{\phi ^ +} = \frac{\alpha}{\sqrt{2}} \ket{000} + \frac{\alpha}{\sqrt{2}} \ket{011} + \frac{\beta}{\sqrt{2}} \ket{100} + \frac{\beta}{\sqrt{2}} \ket{111} $ $

이에 대 한 미리 알림으로 CNOT gate는 컨트롤의가 1 인 경우 대상의 목표를 대칭 이동 합니다. 예를 들어 $ \ket{000}$의 입력으로 인해 첫 번째 (컨트롤)가 0 이므로 변경 되지 않습니다. 그러나 첫 번째 인수를 1로 사용 하는 경우 (예: $ \ket{100}$의 입력) 이 경우 두 번째 \ket (대상)는 CNOT gate에 의해 대칭 이동 되므로 출력은 ${110}$입니다.

이제 CNOT gate가 위의 입력을 처리 한 후 출력을 살펴보겠습니다. 결과는 다음과 같습니다.

$ $ \frac{\alpha}{\sqrt{2}} \ket{000} + \frac{\alpha}{\sqrt{2}} \ket{011} + \frac{\beta}{\sqrt{2}} \ket{110} + \frac{\beta}{\sqrt{2}} \ket{101} $ $

__메시지__ 를 전송 하는 다음 단계는 Hadamard gate를 __메시지의 메시지__ 에 적용 하는 것입니다 (각 용어의 첫 번째 비트율 비트). 

Hadamard gate는 다음과 같은 작업을 수행 합니다.

입력 | 출력
---------------------------| ---------------------------------------------------------------
$ \ket{0}$  | $ \frac{1}{\sqrt{2}} (\ket{0} + \ket{1}) $
$ \ket{1}$  | $ \frac{1}{\sqrt{2}} (\ket{0}-\ket{1}) $

위의 출력의 각 용어에 대 한 첫 번째 Hadamard를 적용 하는 경우 다음과 같은 결과를 얻을 수 있습니다.

$ $ \frac{\alpha}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0} + \ket{1})) \ket{00} + \frac{\alpha}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0} + \ket{1})) \ket{11} + \frac{\beta}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0}-\ket{1})) \ket{10} + \frac{\beta}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0}-\ket{1})) \ket{01} $ $

각 용어에는 $2 \frac{1}{\sqrt{2}} $ 요인이 있습니다. 다음 결과를 제공 하는 것과 같은 결과를 얻을 수 있습니다.

$ $ \frac{\alpha}{2}(\ket{0} + \ket{1}) \ket{00} + \frac{\alpha}{2}(\ket{0} + \ket{1}) \ket{11} + \frac{\beta}{2}(\ket{0}-\ket{1}) \ket{10} + \frac{\beta}{2}(\ket{0}-\ket{1}) \ket{01} $ $

$ \Frac{1}{2}$ 요인은 각 용어에 공통적으로 적용 되므로 이제는 괄호를 벗어날 수 있습니다.

$ $ \frac{1}{2}\big [\alpha (\ket{0} + \ket{1}) \ket{00} + \alpha (\ket{0} + \ket{1}) \ket{11} + \beta (\ket{0}-\ket{1}) \ket{10} + \beta (\ket{0}-\ket{1}) \ket{01}\big] $ $

그러면 다음을 제공 하는 각 용어에 대해 괄호를 곱합니다.

$ $ \frac{1}{2}\big [\alpha\ket{000} + \alpha\ket{100} + \alpha\ket{011} + \alpha\ket{111} + \beta\ket{010}-\beta\ket{110} + \beta\ket{001}-\beta\ket{101}\big] $ $

### <a name="step-3-measure-the-result"></a>3 단계: 결과 측정

__여기__ __에는이__로 __인해,__ __여기서__ 의 모든 측정은 상태에 영향을 줍니다. 첫 번째 및 두 번째 비트 (__메시지__ 및 __여기__)를 측정 하는 경우 되거나 얽 히의이 속성으로 인해에 __있는 상태를__ 알 수 있습니다. 

* 결과 00을 측정 하 고 가져오는 경우 superposition 축소 되 고이 결과와 일치 하는 용어를 그대로 둡니다. $ \Alpha\ket{000} + \beta\ket{001}$입니다. $ \Ket{00}(\alpha\ket{0} + \beta\ket{1}) $로 리팩터링할 수 있습니다. 따라서 첫 번째 및 두 번째 비트를 00으로 측정 하는 경우 세 번째 비트는 $ (\alpha\ket{0} + \beta\ket{1}) $ 상태에 있음을 알 수 __있습니다__.
* 결과 01을 측정 하 고 가져오는 경우 superposition 축소 되 고이 결과와 일치 하는 용어를 그대로 둡니다. $ \Alpha\ket{011} + \beta\ket{010}$입니다. $ \Ket{01}(\alpha\ket{1} + \beta\ket{0}) $로 리팩터링할 수 있습니다. 따라서 첫 번째 및 두 번째 비트를 01로 측정 하는 경우 세 번째 비트는 $ (\alpha\ket{1} + \beta\ket{0}) $ 상태에 __있습니다__.
* 결과 10을 측정 하 고 얻을 경우이 결과와 일치 하는 용어를 그대로 두고 superposition 축소 됩니다. $ \Alpha\ket{100} \beta\ket{101}$입니다. $ \Ket{10}(\alpha\ket{0}-\beta\ket{1}) $로 리팩터링할 수 있습니다. 따라서 첫 번째 및 두 번째 __비트를 10__으로 측정 하는 경우 세 번째 \alpha\ket는 상태 $ ({0}-\beta\ket{1}) $입니다.
* 결과 11을 측정 하 여 얻을 경우 superposition 축소 되 고이 결과와 일치 하는 용어를 그대로 둡니다. $ \Alpha\ket{111} \beta\ket{110}$입니다. $ \Ket{11}(\alpha\ket{1}-\beta\ket{0}) $로 리팩터링할 수 있습니다. 따라서 첫 번째 및 두 번째 __비트를 11__로 측정 하는 경우 세 번째 \alpha\ket는 상태 $ ({1}-\beta\ket{0}) $입니다.

### <a name="step-4-interpret-the-result"></a>4 단계: 결과 해석

보내려는 원래 __메시지__ 는 다음과 같습니다.

$ $ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $ $

수신 된 상태가 의도 된 상태가 되도록이 상태를이 상태로 __가져와야 합니다.__ 

* 00의 결과를 측정 하 고 결과를 얻은 경우 세 번째 비트는 $ (\alpha\ket{0} + \beta\ket{1}) $ 상태에 __있습니다__. 이 메시지는 의도 된 __메시지__이므로 변경이 필요 하지 않습니다.
* 이를 측정 하 고 결과를 01로 얻은 경우 세 번째 비트는 $ (\alpha\ket{1} + \beta\ket{0}) $ 상태에 __있습니다__. 이는 의도 한 __메시지__와 다르지만, no gate를 적용 하면 원하는 상태 $ (\alpha\ket{0} + \beta\ket{1}) $가 제공 됩니다.
* 10의 결과를 측정 하 고 결과를 얻은 경우 세 번째 비트율 비트는 $ (\alpha\ket{0}-\beta\ket{1}) $ 상태에 __있습니다__. 이는 의도 한 __메시지__와 다르지만 Z 게이트를 적용 하면 원하는 상태 $ (\alpha\ket{0} + \beta\ket{1}) $가 제공 됩니다.
* 11의 결과를 측정 하 고 결과를 얻은 경우 세 번째 비트율 비트는 $ (\alpha\ket{1}-\beta\ket{0}) $ 상태에 __있습니다__. 이는 의도 한 __메시지__와는 다르지만, Z 게이트 뒤에, Z 게이트를 적용 하면 원하는 상태 $ (\alpha\ket{0} + \beta\ket{1}) $가 제공 됩니다.

요약 하면 측정 하 고 첫 번째 고 비트는 1 이면 Z 게이트가 적용 됩니다. 측정 하 고 두 번째 고 비트는 1 인 경우에는 게이트가 적용 되지 않습니다.

### <a name="summary"></a>요약
아래에는 teleportation를 구현 하는 텍스트 책 퀀텀 회로가 나와 있습니다. 왼쪽에서 오른쪽으로 이동 하 여 다음을 확인할 수 있습니다.
- 1 단계: Hadamard gate 및 CNOT gate를 적용 하 여 __여기__ __에서 Entangling__ .
- 2 단계: CNOT gate 및 Hadamard gate를 사용 하 여 __메시지__ 보내기
- 3 단계: 첫 번째 및 두 번째 비트를 측정 하 고, __메시지__ 를 __측정 합니다.__
- 4 단계: 3 단계의 측정 결과에 따라 NOT gate 또는 Z 게이트를 적용 합니다.

![' 텔레포트 (msg:?): Unit '](~/media/teleportation.svg)

## <a name="quantum-teleportation-code"></a>퀀텀 Teleportation: 코드

퀀텀 teleportation에 대 한 회로가 있습니다.

![' 텔레포트 (msg:?): Unit '](~/media/teleportation.svg)

이제이 퀀텀 회로의 각 단계를 Q #으로 변환할 수 있습니다.

### <a name="step-0-definition"></a>0 단계: 정의
Teleportation을 수행 하는 경우 보내려는 __메시지__ 와이 메시지를 보낼 위치 __()를__알아야 합니다. 이러한 이유로 두 개의 인수를 인수로 지정 하는 새 텔레포트 작업 (`msg` 및 `there`을 정의 하는 것으로 시작 합니다.

```qsharp
operation Teleport(msg : Qubit, there : Qubit) : Unit {
```

또한 `using` 블록을 사용 하 여 달성할 수 있는 `here`을 할당 해야 합니다.

```qsharp
    using (here = Qubit()) {
```

### <a name="step-1-create-an-entangled-state"></a>1 단계: entangled 상태 만들기
그런 다음 @"microsoft.quantum.intrinsic.h" 및 @"microsoft.quantum.intrinsic.cnot" 작업을 사용 하 여 `here`와 `there` 간에 entangled 쌍을 만들 수 있습니다.

```qsharp
        H(here);
        CNOT(here, there);
```

### <a name="step-2-send-the-message"></a>2 단계: 메시지 보내기
그런 다음, 다음 $ \operatorname{CNOT} $ 및 $H $ 게이트를 사용 하 여 메시지를 이동 합니다.

```qsharp
        CNOT(msg, here);
        H(msg);
```

### <a name="step-3--4-measuring-and-interpreting-the-result"></a>3 단계 & 4 단계: 결과 측정 및 해석
마지막으로 @"microsoft.quantum.intrinsic.m"를 사용 하 여 `if` 문으로 표시 된 대로 측정을 수행 하 고 필요한 게이트 작업을 수행 하 여 원하는 상태를 가져옵니다.

```qsharp
        // Measure out the entanglement
        if (M(msg) == One)  { Z(there); }
        if (M(here) == One) { X(there); }
```

이렇게 하면 teleportation 연산자의 정의가 완료 되므로 `here`할당을 취소 하 고 본문을 종료 하 고 작업을 종료할 수 있습니다.

```qsharp
    }
}
```
