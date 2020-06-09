---
title: Q# Jupyter Notebook을 사용하여 개발
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 9117794d6cf6f05fa34e05c21fad8977d0e76505
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84577823"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Q# Jupyter Notebook을 사용하여 개발

Q # Jupyter 노트북에서 Q # 작업을 개발 하는 데 QDK를 설치 합니다.

Jupyter 노트북은 지침, 메모 및 기타 콘텐츠와 함께 전체 코드 실행을 허용 합니다. 이 환경은 포함 된 설명 또는 퀀텀 컴퓨팅 대화형 자습서를 통해 Q # 코드를 작성 하는 데 적합 합니다. 사용자 고유의 Q# Notebook 만들기를 시작하려면 다음 작업을 수행해야 합니다.

IQ#(i-q-sharp로 발음)은 Jupyter 및 Python에서 .NET Core SDK에 주로 사용되며, Q# 작업을 컴파일하고 시뮬레이션하는 핵심 기능을 제공합니다.

> [!NOTE]
> * Q # Jupyter 노트북에서 Q # 코드만 실행할 수 있으며, 외부 호스트 프로그램 (예: Python 또는 c # 파일)에서 작업을 호출할 수 없습니다. 외부 클래식 호스트 프로그램과 퀀텀 프로그램을 결합 하는 것이 목표 인 경우에는이 환경이 적절 하지 않습니다.

1. 필수 구성 요소

    - [Python](https://www.python.org/downloads/) 3.6 이상
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [.NET Core SDK 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. `iqsharp` 패키지를 설치합니다.

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. `Hello World` 애플리케이션을 만들어 설치를 확인합니다.

    - 다음 명령을 실행하여 Notebook 서버를 시작합니다.

        ```
        jupyter notebook
        ```

    - Jupyter Notebook를 열려면 명령줄에서 제공 된 URL을 복사 하 여 브라우저에 붙여 넣습니다.

    - Q # 커널을 사용 하 여 Jupyter Notebook를 만들고 첫 번째 노트북 셀에 다음 코드를 추가 합니다.

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - 다음 Notebook 셀을 실행합니다.

        ![Q # code를 사용 하 여 셀 Jupyter Notebook](~/media/install-guide-jupyter.png)

        셀의 출력에 `SayHello`가 표시됩니다. Jupyter Notebook에서 실행 되는 경우 Q # 코드가 컴파일되고, 노트북은 검색 된 작업의 이름을 출력 합니다.


    - 새 셀에서 명령을 사용 하 여 시뮬레이터에서 방금 만든 작업을 실행 합니다 `%simulate` .

        ![% 시뮬레이트 마법을 사용 하 여 셀 Jupyter Notebook](~/media/install-guide-jupyter-simulate.png)

        호출 된 작업의 결과와 함께 화면에 메시지가 출력 되는 것을 볼 수 있습니다 ( `()` 작업에서 단순히 형식을 반환 하기 때문에 빈 튜플이 표시 됨 `Unit` ).

## <a name="next-steps"></a>다음 단계

Q # Jupyter 노트북용 QDK를 설치 했으므로 Jupyter Notebook 환경 내에서 직접 Q # 코드를 작성 하 여 [첫 번째 퀀텀 프로그램](xref:microsoft.quantum.quickstarts.qrng) 을 작성 하 고 실행할 수 있습니다.

Q # Jupyter 노트북으로 수행할 수 있는 작업에 대 한 자세한 예제는 다음을 참조 하세요.
- [Q # 및 Jupyter Notebook를 소개](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/)합니다. 이 환경에서 Q #을 사용 하는 방법을 보여 주는 Q # Jupyter Notebook를 찾을 수 있습니다.
- [Katas](xref:microsoft.quantum.overview.katas)는 자체 학습 자습서의 오픈 소스 컬렉션인 Q # Jupyter 노트북 형태의 프로그래밍 연습 집합입니다. [퀀텀 Katas tutorial 노트북](https://github.com/microsoft/QuantumKatas#tutorial-topics) 은 좋은 출발점입니다. 퀀텀 Katas는 퀀텀 컴퓨팅 및 Q # 프로그래밍의 요소를 동시에 학습 하는 것을 목표로 합니다. Q # Jupyter 노트북을 사용 하 여 만들 수 있는 콘텐츠의 종류에 대 한 좋은 예입니다.
