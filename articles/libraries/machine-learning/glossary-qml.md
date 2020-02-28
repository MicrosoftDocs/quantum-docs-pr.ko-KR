---
title: 퀀텀 기계 학습 라이브러리
author: alexeib2
ms.author: alexei.bocharov@microsoft.com
ms.date: 2/27/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.training
ms.openlocfilehash: f9b33a607a892179795d0700ba3080f9a24ab94a
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77909775"
---
# <a name="quantum-machine-learning-glossary"></a>퀀텀 Machine Learning 용어집

회로 중심 퀀텀 분류자의 교육은 기존 분류자의 교육으로 서 평가판 및 오류에의 한 동일한 (또는 약간 더 큰)의 보정을 요구 하는 많은 이동 부분이 포함 된 프로세스입니다. 여기서는이 학습 프로세스의 주요 개념 및 원료를 정의 합니다.

## <a name="trainingtesting-schedules"></a>교육/테스트 일정

분류자의 컨텍스트에서 *일정* 은 전체 학습 또는 테스트 집합의 데이터 샘플 하위 집합을 설명 합니다. 일정은 일반적으로 샘플 인덱스의 컬렉션으로 정의 됩니다.

## <a name="parameterbias-scores"></a>매개 변수/바이어스 점수

후보 매개 변수 벡터와 분류자 바이어스가 지정 된 경우 *유효성 검사 점수* 는 선택한 유효성 검사 일정을 기준으로 측정 되며 일정의 모든 샘플에 대해 계산 된 많은 수의 오 분류로 표시 됩니다.

## <a name="hyperparameters"></a>하이퍼 매개 변수

모델 학습 프로세스는 하이퍼 *매개 변수*라고 하는 특정 미리 설정 된 값의 적용을 받습니다.

### <a name="learning-rate"></a>학습 속도

키 하이퍼 매개 변수 중 하나입니다. 이는 매개 변수 업데이트에 영향을 주는 현재 추계 그라데이션 예상 크기를 정의 합니다. 매개 변수 업데이트 델타의 크기는 학습 률에 비례 합니다. 더 작은 학습 속도 값은 더 느린 매개 변수 진화와 느린 수렴으로 이어질 수 있지만, 대부분의 경우에는 값이 너무 크면 일치를 중단할 수 있습니다. 학습 률은 학습 알고리즘에 따라 어느 정도까지 적절 하 게 조정 되지만 좋은 초기 값을 선택 하는 것이 중요 합니다. 학습 요금에 대 한 일반적인 기본 초기 값은 0.1입니다. 학습 률의 가장 적합 한 값을 선택 하는 것은 자세한 그림입니다 (예: Goodfellow et의 섹션 4.3, "심층 학습", MIT 누르기, 2017).

### <a name="minibatch-size"></a>미니 배치 크기

추계 그라디언트의 단일 예측에 사용 되는 데이터 샘플 수를 정의 합니다. 미니 배치 크기의 값이 클수록 일반적으로 더 강력 하 고 단조가 증가 하지만, minimatch 크기에 비례 하는 한 가지 그라데이션 추정의 비용이 발생 하기 때문에 학습 프로세스의 속도를 저하 시킬 수 있습니다. 미니 배치 크기의 일반적인 기본값은 10입니다.

### <a name="training-epochs-tolerance-gridlocks"></a>교육 epoch, 허용 오차, gridlocks

"Epoch"는 예약 된 학습 데이터를 통과 하는 하나의 완전 한 과정을 의미 합니다.
학습 스레드 (아래 참조) 당 최대 epoch 수는 작아야 합니다. 최대 개수의 epoch가 실행 될 때 학습 스레드는 종료 되도록 정의 됩니다 (가장 알려진 후보 매개 변수 포함). 그러나 유효성 검사 일정에 대 한 잘못 된 분류 비율이 선택한 허용 오차 미만으로 떨어지면 이러한 교육은 이전에 종료 됩니다. 예를 들어 잘못 된 분류 허용 오차는 0.01 (1%)입니다. 2000의 유효성 검사 집합에서 20 개 미만의 분류를 표시 하는 경우 허용 오차 수준이 달성 됩니다. 또한 후보 모델의 유효성 검사 점수가 여러 연속 epoch (gridlock)에 대해 향상 된 것으로 표시 되지 않은 경우 학습 스레드는 중간에 종료 됩니다. Gridlock 종료에 대 한 논리는 현재 하드 코드 되어 있습니다.

### <a name="measurements-count"></a>측정값 수

퀀텀 장치에서 추계 그라데이션의 구성 요소 및 학습/유효성 검사 점수를 예측 하 여 적절 한 관찰 가능 개체의 여러 측정이 필요한 퀀텀 상태 겹침을 예측 합니다. 측정 수는 $O (1/\ 엡실론 ^ 2)로 확장 해야 합니다. 여기서 $ \epsilon $은 원하는 추정 오류입니다.
이에 대 한 규칙에 따라 초기 측정 수는 약 $1/\ mbox {tolerance} ^ 2 $ 일 수 있습니다 (이전 단락의 허용 오차 정의 참조). 그라데이션 디센더가 너무 불안정 하 여 너무 많이 수렴 하 여 달성할 수 없는 것 처럼 보이는 경우에는 측정값 수를 위쪽으로 수정 해야 합니다.

### <a name="training-threads"></a>스레드 학습

분류자의 학습 유틸리티인 가능성 함수는 거의 발생 하지 않습니다. 즉, 일반적으로 품질에 따라 크게 다를 수 있는 매개 변수 공간에는 다 수의 로컬 optima 있습니다. SGD 프로세스는 하나의 특정 최적에만 수렴 될 수 있으므로 여러 개의 시작 매개 변수 벡터를 탐색 하는 것이 중요 합니다. 기계 학습에서 일반적인 방법은 이러한 시작 벡터를 임의로 초기화 하는 것입니다. Q # 학습 API는 이러한 시작 벡터의 임의 배열을 허용 하지만 기본 코드는 순차적으로 탐색 합니다. 다중 코어 컴퓨터의 경우 또는 병렬 컴퓨팅 아키텍처의 경우 호출에서 여러 매개 변수 초기화를 사용 하 여 여러 개의 Q # 학습 API 호출을 동시에 수행 하는 것이 좋습니다.

#### <a name="how-to-modify-the-hyperparameters"></a>하이퍼 매개 변수를 수정 하는 방법

QML 라이브러리에서 하이퍼 매개 변수를 수정 하는 가장 좋은 방법은 UDT [`TrainingOptions`](xref:microsoft.quantum.machinelearning.trainingoptions)의 기본값을 재정의 하는 것입니다. 이렇게 하려면 [`DefaultTrainingOptions`](xref:microsoft.quantum.machinelearning.defaulttrainingoptions) 함수를 사용 하 여이를 호출 하 고 연산자 `w/`를 적용 하 여 기본값을 재정의 합니다. 예를 들어 10만 측정치와 0.01의 학습 률을 사용 하려면 다음을 수행 합니다.
 ```qsharp
let options = DefaultTrainingOptions()
w/ LearningRate <- 0.01
w/ NMeasurements <- 100000;
 ```
