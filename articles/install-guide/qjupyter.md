---
title: 'Q # Jupyter 노트북을 사용 하 여 개발'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: b7276f9b273f601f30e4938018398353b6a9102d
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76831072"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Q # Jupyter 노트북을 사용 하 여 개발

Q # Jupyter 노트북에서 Q # 작업을 개발 하는 데 QDK를 설치 합니다.

Jupyter 노트북은 지침, 메모 및 기타 콘텐츠와 함께 전체 코드 실행을 허용 합니다. 이 환경은 포함 된 설명 또는 퀀텀 컴퓨팅 대화형 자습서를 통해 Q # 코드를 작성 하는 데 적합 합니다. 사용자 고유의 Q# Notebook 만들기를 시작하려면 다음 작업을 수행해야 합니다.

IQ#(i-q-sharp로 발음)은 Jupyter 및 Python에서 .NET Core SDK에 주로 사용되며, Q# 작업을 컴파일하고 시뮬레이션하는 핵심 기능을 제공합니다.

> [!NOTE]
> * Q # Jupyter 노트북에서 Q # 코드만 실행할 수 있으며 작업은 외부 호스트 프로그램 (예: Python 또는 C# 파일)에서 호출할 수 없습니다. 외부 클래식 호스트 프로그램과 퀀텀 프로그램을 결합 하는 것이 목표 인 경우에는이 환경이 적절 하지 않습니다.

1. 필수 조건

    - [Python](https://www.python.org/downloads/) 3.6 이상
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [.NET Core SDK 3.1 이상](https://www.microsoft.com/net/download)

1. `iqsharp` 패키지를 설치합니다.

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. `Hello World` 애플리케이션을 만들어 설치를 확인합니다.

    - 다음 명령을 실행하여 Notebook 서버를 시작합니다.

        ```bash
        jupyter notebook
        ```

    - Jupyter 노트 복사를 열려면 명령줄에서 제공 된 URL을 브라우저에 붙여 넣습니다.

    - Q# 커널을 사용하여 Jupyter Notebook을 만들고 첫 번째 Notebook 셀에 다음 코드를 추가합니다.

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - 다음 Notebook 셀을 실행합니다.

        ![Q# 코드를 사용하는 Jupyter Notebook 셀](~/media/install-guide-jupyter.png)

        셀의 출력에 `SayHello`가 표시됩니다. Jupyter Notebook에서 실행하는 경우 Q# 코드가 컴파일되고 Notebook은 검색된 작업의 이름을 출력합니다.


    - 새 셀에서 `%simulate` 명령을 사용 하 여 시뮬레이터에서 방금 만든 작업을 실행 합니다.

        ![%simulate 매직을 사용하는 Jupyter Notebook 셀](~/media/install-guide-jupyter-simulate.png)

        호출 된 작업의 결과와 함께 화면에 메시지가 출력 되는 것을 볼 수 있습니다 (작업에서 단순히 `Unit` 형식을 반환 하기 때문에 빈 튜플 `()` 표시 됨).

## <a name="whats-next"></a>다음은 무엇일까요?

지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.write-program)을 작성 및 실행할 수 있습니다.
