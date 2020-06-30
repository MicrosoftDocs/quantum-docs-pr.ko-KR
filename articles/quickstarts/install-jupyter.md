---
title: Q# Jupyter Notebook을 사용하여 개발
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 5c613d29c03525d29893307684f13ccd32d4d4eb
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274092"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Q# Jupyter Notebook을 사용하여 개발

Q# Jupyter Notebook에서 Q# 작업을 개발하기 위해 QDK를 설치합니다.

Jupyter Notebook을 사용하면 지침, 메모 및 기타 콘텐츠와 함께 내부 코드를 실행할 수 있습니다. 이 환경은 설명 또는 퀀텀 컴퓨팅 대화형 자습서가 포함된 Q# 코드를 작성하는 데 적합합니다. 사용자 고유의 Q# Notebook 만들기를 시작하려면 다음 작업을 수행해야 합니다.

IQ#(i-q-sharp로 발음)은 Jupyter 및 Python에서 .NET Core SDK에 주로 사용되며, Q# 작업을 컴파일하고 시뮬레이션하는 핵심 기능을 제공합니다.

> [!NOTE]
> * Q# Jupyter Notebook에서는 Q# 코드만 실행할 수 있고 외부 호스트 프로그램(예: Python 또는 C# 파일)에서 작업을 호출할 수는 없습니다. 외부 클래식 호스트 프로그램과 퀀텀 프로그램을 결합하는 것이 목표라면 이 환경은 적합하지 않습니다.

1. 필수 구성 요소

    - [Python](https://www.python.org/downloads/) 3.6 이상
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [.NET Core SDK 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. `iqsharp` 패키지를 설치합니다.

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > `dotnet iqsharp install` 단계 중에 오류가 발생하면 새 터미널 창을 열고 다시 시도합니다.
    > 그래도 해결되지 않으면 설치된 `dotnet-iqsharp` 도구(Windows의 경우 `dotnet-iqsharp.exe`)를 찾아서 실행합니다.
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > 여기서 `/path/to/dotnet-iqsharp`은 파일 시스템에서 `dotnet-iqsharp` 도구의 절대 경로로 바꿔야 합니다.
    > 일반적으로 사용자 프로필 폴더의 `.dotnet/tools`에 있습니다.

1. `Hello World` 애플리케이션을 만들어 설치를 확인합니다.

    - 다음 명령을 실행하여 Notebook 서버를 시작합니다.

        ```
        jupyter notebook
        ```

    - Jupyter Notebook을 열려면 명령줄에 제공된 URL을 복사하여 브라우저에 붙여넣습니다.

    - Q# 커널을 사용하여 Jupyter Notebook을 만들고 첫 번째 Notebook 셀에 다음 코드를 추가합니다.

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - 다음 Notebook 셀을 실행합니다.

        ![Q# 코드가 포함된 Jupyter Notebook 셀](~/media/install-guide-jupyter.png)

        셀의 출력에 `SayHello`가 표시됩니다. Jupyter Notebook에서 실행하는 경우 Q# 코드가 컴파일되고 Notebook은 검색된 작업의 이름을 출력합니다.


    - 새 셀에서 `%simulate` 명령을 사용하여 방금 만든(시뮬레이터에서) 작업을 실행합니다.

        ![%simulate 매직이 포함된 Jupyter Notebook 셀](~/media/install-guide-jupyter-simulate.png)

        호출한 작업의 결과(여기서는 작업이 단순히 `Unit` 유형을 반환하기 때문에 빈 튜플 `()`이 표시됨)와 함께 메시지가 화면에 출력됩니다.

## <a name="next-steps"></a>다음 단계

Q# Jupyter Notebook용 QDK를 설치했으면, Jupyter Notebook 환경 내에서 직접 Q# 코드를 작성하여 [첫 번째 퀀텀 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성하고 실행할 수 있습니다.

Q# Jupyter Notebook으로 수행할 수 있는 작업에 대한 자세한 내용은 다음을 참조하세요.
- [Q# 및 Jupyter Notebook 소개](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/). 이 환경에서 Q#을 사용하는 방법을 보여주는 Q# Jupyter Notebook을 찾을 수 있습니다.
- [Quantum Katas](xref:microsoft.quantum.overview.katas)는 Q# Jupyter Notebook 형태의 자기 주도적 자습서 및 프로그래밍 연습 세트를 포함하는 오픈 소스 컬렉션입니다. [Quantum Katas 자습서 Notebook](https://github.com/microsoft/QuantumKatas#tutorial-topics)은 좋은 시작점입니다. Quantum Katas의 목표는 퀀텀 컴퓨팅과 Q# 프로그래밍 요소를 동시에 학습하는 것입니다. Q# Jupyter Notebook으로 만들 수 있는 콘텐츠의 종류를 보여주는 유용한 예입니다.
