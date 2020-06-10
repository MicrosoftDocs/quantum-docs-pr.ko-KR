---
title: 'Q # 및 Python을 사용 하 여 개발'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 1ae208e7047cb040fb44945a59c3cc6508a09723
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630279"
---
# <a name="develop-with-q-and-python"></a>Q # 및 Python을 사용 하 여 개발

Q # 작업을 호출 하는 Python 호스트 프로그램을 개발 하려면 QDK를 설치 합니다.

1. 전제 조건

    - [Python](https://www.python.org/downloads/) 3.6 이상
    - [PIP](https://pip.pypa.io/en/stable/installing) Python 패키지 관리자
    - [.NET Core SDK 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. `qsharp`Q #과 python 간에 interop를 사용할 수 있도록 하는 Python 패키지인 패키지를 설치 합니다.

    ```
    pip install qsharp
    ```

1. Q # 작업을 컴파일하고 실행 하기 위한 핵심 기능을 제공 하는 Jupyter 및 Python에서 사용 하는 커널 인 IQ #을 설치 합니다.

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > 단계 중에 오류가 발생 하면 `dotnet iqsharp install` 새 터미널 창을 열고 다시 시도 합니다.
    > 그래도 작동 하지 않으면 설치 된 `dotnet-iqsharp` 도구 (Windows)를 찾아 `dotnet-iqsharp.exe` 실행 합니다.
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > 는 `/path/to/dotnet-iqsharp` 파일 시스템의 도구에 대 한 절대 경로로 바꾸어야 합니다 `dotnet-iqsharp` .
    > 일반적으로이는 `.dotnet/tools` 사용자 프로필 폴더에 있습니다.
  
1. 모든 IDE에서 Q #을 Python과 함께 사용할 수 있지만 Q # + Python 응용 프로그램에 Visual Studio Code (VS Code) IDE를 사용 하는 것이 좋습니다. Visual Studio Code 및 QDK Visual Studio Code 확장을 사용 하 여 보다 다양 한 기능에 액세스할 수 있습니다.

    - [VS Code](https://code.visualstudio.com/download) (Windows, Linux 및 Mac) 설치
    - [VS Code 용 Qdk 확장](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)을 설치 합니다.

1. `Hello World` 애플리케이션을 만들어 설치를 확인합니다.

    - `Operation.qs`라는 파일을 만들고 다음 코드를 추가하여 최소 Q# 작업을 만듭니다.

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
            }
        }
        ```

    - `hello_world.py`이라는 Python 프로그램을 만들어 Q# `SayHello()` 작업을 호출합니다.

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - 다음과 같이 프로그램을 실행합니다.

        ```
        python hello_world.py
        ```

    - 출력을 확인합니다. 프로그램은 다음 줄을 출력합니다.

        ```
        Hello from quantum world!
        ```


> [!NOTE]
> * Python Jupyter 노트북을 사용 하 여 기존 Python 프로그램을 작성 하 고 셀에서 Q # 작업을 호출할 수도 있습니다. Python 코드는 일반적인 Python 프로그램 일 뿐입니다.

## <a name="next-steps"></a>다음 단계

지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성 및 실행할 수 있습니다.
