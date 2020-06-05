---
title: 퀀텀 Machine Learning 라이브러리를 사용 하는 기본 분류
description: 'Microsoft QDK 퀀텀 Machine Learning 라이브러리를 사용 하 여 Q #으로 작성 된 퀀텀 순차 분류자를 실행 하는 방법에 대해 알아봅니다.'
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.basics
ms.openlocfilehash: 1d2538fd164c4c61c2712978d3b5c57b0eb766e6
ms.sourcegitcommit: 8d9d392bf5e114ae223e6f689ba80d25866ff586
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/04/2020
ms.locfileid: "84422175"
---
# <a name="basic-classification-classify-data-with-the-qdk"></a>기본 분류: QDK 데이터 분류

이 빠른 시작에서는 QDK의 퀀텀 Machine Learning 라이브러리를 사용 하 여 Q #으로 작성 된 퀀텀 순차 분류자를 실행 하는 방법에 대해 설명 합니다. 

이 가이드에서는 Q #에 정의 된 분류자 구조를 사용 하 여 초승달 데이터 집합을 사용 합니다.

## <a name="prerequisites"></a>사전 요구 사항

- Microsoft [Quantum Development Kit](xref:microsoft.quantum.install)
- [Python 호스트 프로그램](xref:microsoft.quantum.install.python) 또는 [c # 호스트 프로그램](xref:microsoft.quantum.install.cs)에 대해 Q # 프로젝트를 만듭니다.

## <a name="host-program"></a>호스트 프로그램

호스트 프로그램은 다음 세 부분으로 구성 됩니다.

- 데이터 집합을 로드 하 고 모델의 시작 매개 변수 집합을 선택 합니다.
- 학습을 실행 하 여 모델의 매개 변수 및 바이어스를 확인 합니다.
- 모델의 유효성을 검사 하 여 정확성 확인

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Visual Studio 코드 또는 명령줄을 사용하는 Python](#tab/tabid-python)

    Python의 Q # 분류자를 실행 하려면 다음 코드를로 저장 합니다 `host.py` . `Training.qs`이 자습서의 뒷부분에서 설명 하는 Q # 파일도 필요 합니다.

    :::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="3-42":::

    그러면 명령줄에서 Python 호스트 프로그램을 실행할 수 있습니다.

    ```bash
    $ python host.py
    Preparing Q# environment...
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[Visual Studio 코드 또는 명령줄을 사용하는 C#](#tab/tabid-csharp)

    C #의 Q # 분류자를 실행 하려면 다음 코드를로 저장 합니다 `Host.cs` . `Training.qs`이 자습서의 뒷부분에서 설명 하는 Q # 파일도 필요 합니다.

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    그러면 명령줄에서 C# 호스트 프로그램을 실행할 수 있습니다.

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-2019"></a>[Visual Studio 2019를 사용하는 C#](#tab/tabid-vs2019)

    Visual Studio의 c #에서 새 Q # 프로그램을 실행 하려면 `Host.cs` 다음 c # 코드를 포함 하도록을 수정 합니다. `Training.qs`이 자습서의 뒷부분에서 설명 하는 Q # 파일도 필요 합니다.

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    그런 다음, F5 키를 누르면 프로그램이 실행되고 새 창에 다음 결과가 표시됩니다. 

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```
    ***

## <a name="q-classifier-code"></a>Q \# 분류자 코드

이제 호스트 프로그램에서 호출 하는 작업이 Q #에서 정의 되는 방식을 살펴보겠습니다.
이라는 파일에 다음 코드를 저장 `Training.qs` 합니다.

:::code language="qsharp" source="~/quantum/samples/machine-learning/half-moons/Training.qs" range="4-116":::

위의 코드에 정의 된 가장 중요 한 함수와 연산은 다음과 같습니다.

- `ClassifierStructure() : ControlledRotation[]`:이 함수에서 고려 하는 제어 되는 게이트의 계층을 추가 하 여 회로 모델 구조를 설정 합니다. 이 단계는 순차적 심층 학습 모델에서 뉴런의 계층 선언과 유사 합니다.
- `TrainHalfMoonModel() : (Double[], Double)`:이 작업은 코드의 핵심 부분이 며 학습을 정의 합니다. 여기에서 라이브러리에 포함 된 데이터 집합의 샘플을 로드 하 고, 학습에 대 한 하이퍼 매개 변수 및 초기 매개 변수를 설정 하 고, 라이브러리에 포함 된 작업을 호출 하 여 학습을 시작 합니다 `TrainSequentialClassifier` . 분류자를 결정 하는 매개 변수 및 바이어스를 출력 합니다.
- `ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int`:이 작업은 모델을 평가 하는 유효성 검사 프로세스를 정의 합니다. 여기서는 유효성 검사에 대 한 샘플, 샘플 당 측정 수 및 허용 오차를 로드 합니다. 유효성 검사를 위해 선택한 샘플 일괄 처리의 오 분류 수를 출력 합니다.

## <a name="next-steps"></a>다음 단계

첫째, 코드를 사용 하 여 재생 하 고 몇 가지 매개 변수를 변경 하 여 학습에 미치는 영향을 확인할 수 있습니다. 그런 다음, 다음 자습서의 [고유한 분류자 디자인](xref:microsoft.quantum.libraries.machine-learning.design)에서 분류자의 구조를 정의 하는 방법을 배웁니다.
