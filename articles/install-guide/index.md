---
title: Microsoft QDK(Quantum Development Kit) 설치 방법 알아보기
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 3ec53934436b47908fd4d794a98933010f6059a7
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2019
ms.locfileid: "73035302"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>Microsoft QDK(Quantum Development Kit) 설치

양자 프로그래밍을 시작할 수 있도록 Microsoft QDK(Quantum Development Kit)를 설치하는 방법을 알아봅니다. QDK은 다음으로 구성됩니다.

- Go 프로그래밍 언어
- Q#의 복합 기능을 추상화하는 라이브러리 세트
- Q#으로 작성된 양자 연산을 실행하는 호스트 애플리케이션(Python 또는 .NET 언어로 작성)
- 개발을 용이하게 하는 도구

선택한 개발 환경에 따라 여러 가지 설치 단계가 있습니다. 아래 섹션에서 환경을 선택합니다.

## <a name="develop-with-python"></a>Python으로 개발

1. 필수 조건

    - [Python](https://www.python.org/downloads/) 3.6 이상
    - [PIP](https://pip.pypa.io/en/stable/installing) Python 패키지 관리자
    - [.NET Core SDK 2.1 이상](https://www.microsoft.com/net/download)

1. `iqsharp` 패키지를 설치합니다.

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. `qsharp` 패키지를 설치합니다.

    ```bash
    pip install qsharp
    ```

1. `Hello World` 애플리케이션을 만들어 설치를 확인합니다.

    - `Operation.qs`라는 파일을 만들고 다음 코드를 추가하여 최소 Q# 작업을 만듭니다.

        ```qsharp
        namespace HelloWorld
        {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Result {
                Message("Hello from quantum world!");
                return Zero;
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

        ```bash
        python hello_world.py
        ```

    - 출력을 확인합니다. 프로그램은 다음 줄을 출력합니다.

        ```bash
        Hello from quantum world!
       0
       ```

## <a name="develop-with-jupyter-notebooks"></a>Jupyter Notebook을 사용하여 개발

1. 필수 조건

    - [Python](https://www.python.org/downloads/) 3.6 이상
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [.NET Core SDK 2.1 이상](https://www.microsoft.com/net/download)

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

    - 명령줄에 표시된 URL로 이동합니다. 예: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]

    - Q# 커널을 사용하여 Jupyter Notebook을 만들고 첫 번째 Notebook 셀에 다음 코드를 추가합니다.

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - 다음 Notebook 셀을 실행합니다.

        ![Jupyter Notebook 셀](~/media/install-guide-jupyter.png)

        셀의 출력에 `SayHello`가 표시됩니다. Jupyter Notebook에서 실행하는 경우 Q# 코드가 컴파일되고 Notebook은 검색된 작업의 이름을 출력합니다.

## <a name="develop-with-c-on-windows-using-visual-studio"></a>Windows C#에서 Visual Studio를 사용하여 C#으로 개발

1. 필수 조건

    - [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, .NET Core 플랫폼 간 개발 워크로드 설정

1. Q# Visual Studio 확장을 설치합니다.

    - [Visual Studio 확장](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)을 다운로드합니다.
    - Visual Studio에 확장을 추가합니다.

1. `Hello World` 애플리케이션을 만들어 설치를 확인합니다.

    - 새 Q# 애플리케이션 만들기

        - **파일** -> **새로 만들기** -> **프로젝트**로 이동
        - 검색 상자에 `Q#` 입력
        - **Q# 애플리케이션**을 선택합니다.
        - **다음**을 선택합니다.
        - 애플리케이션의 이름 및 위치를 선택합니다.
        - **만들기**

    - 프로젝트를 검사합니다.

        C# 호스트 애플리케이션에 해당하는 `Driver.cs`와 콘솔에 메시지를 출력하는 간단한 작업을 정의하는 Q# 프로그램에 해당하는 `Operation.qs`의 두 파일이 생성된 것을 확인할 수 있습니다.

    - 애플리케이션 실행

        - **디버그** -> **디버깅하지 않고 시작**을 선택합니다.
        - 콘솔 창에 `Hello quantum world!`가 출력된 것을 볼 수 있습니다.

> [!NOTE]
> * 단일 Visual Studio 솔루션 내에 여러 프로젝트가 있는 경우 솔루션에 포함된 모든 프로젝트는 솔루션과 동일한 폴더 또는 해당 하위 폴더 중 하나에 포함되어야 합니다.  

## <a name="develop-with-c-using-vs-code"></a>VS Code를 사용하여 C#으로 개발

1. 필수 조건

   - [VS 코드](https://code.visualstudio.com/download)
   - [.NET Core SDK 2.1 이상](https://www.microsoft.com/net/download)

1. Quantum VS Code 확장을 설치합니다.

    - [VS Code 확장](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)을 설치합니다.

1. 양자 프로젝트 템플릿을 설치합니다.

   - **보기** -> **명령 팔레트**로 이동합니다.
   - **Q#: 프로젝트 템플릿 설치**를 선택합니다.

    이제 Quantum Development Kit가 설치되었으며 사용자의 애플리케이션 및 라이브러리에서 사용할 준비가 되었습니다.

1. `Hello World` 애플리케이션을 만들어 설치를 확인합니다.

    - 새 프로젝트를 만듭니다.

        - **보기** -> **명령 팔레트**로 이동합니다.
        - **Q#: 새 프로젝트 만들기**를 선택합니다.
        - 애플리케이션을 만들려는 파일 시스템의 위치로 이동합니다.
        - 프로젝트를 만든 후에 **새 프로젝트 열기...** 단추를 클릭합니다.

    - 애플리케이션을 실행합니다.

        - **디버그** -> **디버깅하지 않고 시작**으로 이동합니다.
        - 출력 창에 다음 텍스트가 표시되어야 합니다. `Hello quantum world!`

> [!NOTE]
> * > * 여러 루트 폴더가 있는 작업 영역은 현재 Visual Studio Code 확장에서 지원되지 않습니다. 단일 VS Code 작업 영역에 여러 프로젝트가 있는 경우 모든 프로젝트가 동일한 루트 폴더 내에 포함되어야 합니다.

## <a name="develop-with-c-using-the-dotnet-command-line-tool"></a>`dotnet` 명령줄 도구를 사용하여 C#으로 개발

1. 필수 조건

    - [.NET Core SDK 2.1 이상](https://www.microsoft.com/net/download)

1. .NET용 양자 프로젝트 템플릿을 설치합니다.

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    이제 Quantum Development Kit가 설치되었으며 사용자의 애플리케이션 및 라이브러리에서 사용할 준비가 되었습니다.

1. `Hello World` 애플리케이션을 만들어 설치를 확인합니다.

    - 새 애플리케이션 만들기

       ```bash
       dotnet new console -lang Q# -o runSayHello
       ```

    - 새 애플리케이션 디렉터리로 이동합니다.

       ```bash
       cd runSayHello
       ```

    애플리케이션의 프로젝트 파일과 함께 Q# 파일(`Operation.qs`) 및 C# 호스트 파일(`Driver.cs`)의 두 파일이 생성된 것을 볼 수 있습니다.

    - 애플리케이션 실행

        ```bash
        dotnet run
        ```

        다음 출력이 표시됩니다. `Hello quantum world!`

## <a name="whats-next"></a>다음 작업

지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.write-program)을 작성 및 실행할 수 있습니다.
