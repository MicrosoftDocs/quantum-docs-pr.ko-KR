---
title: QDK 사용자 고유의 분류자 디자인
description: 퀀텀 회로 중심 분류자에 대 한 회로 모델 디자인의 기본 개념을 알아봅니다.
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/17/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.design
ms.openlocfilehash: 4899336f437c1b7712a7831b97fd6ec1431b59a2
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77909724"
---
# <a name="design-your-own-classifier"></a>사용자 고유의 분류자 디자인

이 가이드에서는 퀀텀 회로 중심 분류자에 대 한 회로 모델 디자인의 기본 개념을 설명 합니다.

기존 심층 학습 에서처럼 특정 아키텍처를 선택 하는 일반적인 규칙은 없습니다. 문제에 따라 일부 아키텍처는 다른 아키텍처 보다 성능이 향상 됩니다. 그러나 회로를 설계할 때 유용할 수 있는 몇 가지 개념이 있습니다.

- 많은 수의 매개 변수는 복잡 한 분류 경계를 그리는 데 적합할 수 있지만 과잉 맞춤에 더 취약할 수 있는 보다 유연한 모델을 의미 합니다.

- Entangling 게이트는 퀀텀 기능 간의 상관 관계를 캡처하기 위해 반드시 필요 합니다.

## <a name="how-to-build-a-classifier-with-q"></a>Q\#를 사용 하 여 분류자를 빌드하는 방법

분류자를 빌드하기 위해 회로 모델에서 매개 변수가 있는 제어 되는 회전을 연결 하겠습니다. 이렇게 하려면 퀀텀 Machine Learning 라이브러리에 정의 된 형식 [`ControlledRotation`](xref:microsoft.quantum.machinelearning.controlledrotation) 를 사용할 수 있습니다. 이 형식에는 대상의 인덱스, 컨트롤의 인덱스 배열, 회전 축 및 모델을 정의 하는 매개 변수 배열에 있는 연결 된 매개 변수의 인덱스를 결정 하는 네 개의 인수가 허용 됩니다.

분류자의 예를 살펴보겠습니다. [Moons 샘플](https://github.com/microsoft/Quantum/tree/master/samples/machine-learning/half-moons)에서는 파일 `Training.qs`에 정의 된 다음 분류자를 찾을 수 있습니다.

```qsharp
    function ClassifierStructure() : ControlledRotation[] {
        return [
            ControlledRotation((0, new Int[0]), PauliX, 4),
            ControlledRotation((0, new Int[0]), PauliZ, 5),
            ControlledRotation((1, new Int[0]), PauliX, 6),
            ControlledRotation((1, new Int[0]), PauliZ, 7),
            ControlledRotation((0, [1]), PauliX, 0),
            ControlledRotation((1, [0]), PauliX, 1),
            ControlledRotation((1, new Int[0]), PauliZ, 2),
            ControlledRotation((1, new Int[0]), PauliX, 3)
        ];
    }
 ```

여기에서 정의 하는 것은 매개 변수 배열과 함께 [`SequentialModel`](xref:microsoft.quantum.machinelearning.sequentialmodel)를 정의 하는 `ControlledRotation` 요소의 배열을 반환 하는 함수입니다. 이 형식은 퀀텀 Machine Learning 라이브러리에서 기본 이며 분류자를 정의 합니다. 위의 함수에서 정의 된 회로는 데이터 집합의 각 샘플에 두 가지 기능이 포함 된 분류자의 일부입니다. 따라서 두 개의 비트 비트만 필요 합니다. 회로의 그래픽 표현은 다음과 같습니다.

 ![회로 모델 예](~/media/circuit_model_1.PNG)

## <a name="use-the-library-functions-to-write-layers-of-gates"></a>라이브러리 함수를 사용 하 여 게이트 계층 작성

인스턴스당 784 기능이 포함 된 데이터 집합 (예: MNIST 데이터 집합 같은 28 × 28 픽셀 이미지)이 있다고 가정 합니다. 이 경우 회로의 너비는 충분 한 크기를 가지 므로 각 개별 gate를 편리 하 게 작성할 수 있지만 실용적이 지 않습니다. 이 때문에 퀀텀 Machine Learning 라이브러리는 매개 변수가 있는 회전 레이어를 자동으로 생성 하는 도구 집합을 제공 합니다. 예를 들어 함수 [`LocalRotationsLayer`](xref:microsoft.quantum.machinelearning.localrotationslayer) 는 지정 된 축을 따라 지정 된 축을 따라 제어 가능한 단일 각도 비트 회전의 배열을 반환 합니다. 각는 레지스터의 각가 다른 모델 매개 변수로 매개 변수가 있는 합니다. 예를 들어 `LocalRotationsLayer(4, X)`는 다음 게이트 집합을 반환 합니다.

 ![로컬 회전 계층](~/media/local_rotations_layer.PNG)

모든 도구를 검색 하 여 회로 디자인을 간소화 하는 데 사용할 수 있는 [퀀텀 Machine Learning 라이브러리의 API referenece](xref:microsoft.quantum.machinelearning) 을 살펴보는 것이 좋습니다.

## <a name="next-steps"></a>다음 단계

 샘플에서 제공 하는 예제에서 다른 구조를 시도 합니다. 모델의 성능에 대 한 변경 내용이 표시 되나요? 다음 자습서 [`Load your own datasets`](xref:microsoft.quantum.libraries.machine-learning.load)에서는 데이터 집합을 로드 하 여 분류자의 새 아키텍처를 시험해 보고 탐색 하는 방법을 배웁니다.
