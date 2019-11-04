---
title: 'QDK (퀀텀 개발 키트)를 사용 하 여 Q # 프로젝트를 만드는 방법을 알아봅니다.'
description: '선택한 개발 환경에서 QDK 및 Q #을 사용 하 여 퀀텀 개발을 위한 프로젝트를 초기화 합니다.'
author: natke
ms.author: nakersha
ms.date: 10/19/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.howto.createproject
ms.openlocfilehash: b4bec5e7a174b7e2d588331dd2093c7b23a728b0
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2019
ms.locfileid: "73444177"
---
# <a name="create-a-q-project-in-your-development-environment"></a>개발 환경에서 Q # 프로젝트 만들기

QDK를 사용 하 여 Q # 프로젝트를 만드는 방법에 대해 알아봅니다.

Q # 프로젝트에는 퀀텀 코드를 포함 하는 Q # 파일 뿐만 아니라 퀀텀 프로그램을 실행 하는 호스트 프로그램도 포함 됩니다. 호스트 프로그램은 또는 Python과 C#같은 .net 언어로 작성할 수 있습니다. 또한 IQ # 커널을 사용 하 여 Jupyter 노트북에서 Q # 코드를 실행할 수 있습니다.

아래 섹션에서 개발 환경 및 언어를 선택 합니다.

* [Python](#create-a-python-project)
* [Jupyter 노트북](#create-a-jupyter-notebook-project)
* [C#Visual Studio 사용](#create-a-c-project-on-windows-using-visual-studio)
* [C#VS Code 사용](#create-a-c-project-using-vs-code)
* [C#명령줄 사용](#create-a-c-project-using-the-dotnet-command-line-tool)

## <a name="create-a-python-project"></a>Python 프로젝트 만들기

1. 필수 조건

     * [Python 용 퀀텀 개발 키트](xref:microsoft.quantum.install#develop-with-python)

1. 프로젝트에 대 한 폴더를 만들고 해당 폴더로 이동 합니다.

1. `Operation.qs`이라는 Q # 파일을 만들고 Q # 코드를 추가 합니다. 다음은 그 예입니다.

    ```qsharp
    namespace HelloWorld {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation SayHello() : Result {
            Message("Hello from quantum world!");
            return Zero;
        }
    }
    ```

1. Q # 작업을 호출 하는 `host.py` 라는 python 호스트 파일을 만듭니다. 다음은 그 예입니다.

    ```python
    import qsharp

    from HelloWorld import SayHello

    SayHello.simulate()
    ```

1. 다음과 같이 프로그램을 실행합니다.

    ```bash
    python host.py
    ```

1. 출력을 확인합니다. 프로그램은 다음 줄을 출력합니다.

    ```bash
    Hello from quantum world!
    0
    ```

이제 퀀텀 프로그램을 계속 개발할 수 있습니다.

## <a name="create-a-jupyter-notebook-project"></a>Jupyter Notebook 프로젝트 만들기

1. 필수 조건

    * [Jupyter 노트북용 퀀텀 개발 키트](xref:microsoft.quantum.install#develop-with-jupyter-notebooks)

1. 다음 명령을 실행하여 Notebook 서버를 시작합니다.

    ```bash
    jupyter notebook
    ```

1. 명령줄에 표시된 URL로 이동합니다. 예: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]

1. 브라우저에 Jupyter 페이지가 나타납니다. **파일** 탭에서 **새로** 만들기 > **q #** 를 선택 하 여 q # 커널을 사용 하 여 jupyter 노트북을 만듭니다. 첫 번째 노트북 셀에 다음 코드를 추가 합니다.

    ```qsharp
    operation SayHello() : Unit {
        Message("Hello from quantum world!");
    }
    ```

1.  > **셀** 을 선택 **하 여 노트북** 을 실행 합니다. `SayHello`은 곧 셀 출력에 표시 됩니다.

    ![Q # code를 사용 하는 jupyter 노트북 셀](~/media/install-guide-jupyter.png)

    Jupyter 노트북에서 실행 하는 경우 Q # 코드가 컴파일되고 노트북은 검색 된 작업의 이름을 출력 합니다.

1. 새 셀에서 `%simulate` magic을 사용 하 여 방금 만든 작업의 퀀텀 컴퓨터에서 실행을 시뮬레이트합니다.

    ![% 시뮬레이트 마법을 사용 하는 jupyter 노트북 셀](~/media/install-guide-jupyter-simulate.png)

    호출 된 작업 (이 경우 비어 있음)의 결과와 함께 화면에 메시지가 인쇄 됩니다.

이제 다른 Q # 작업을 추가 하 여 퀀텀 개발을 계속할 수 있습니다.

## <a name="create-a-c-project-on-windows-using-visual-studio"></a>Visual Studio C# 를 사용 하 여 Windows에서 프로젝트 만들기

1. 필수 조건

    * [Visual Studio 용 퀀텀 개발 키트](xref:microsoft.quantum.install#develop-with-c-on-windows-using-visual-studio)

1. 새 Q# 애플리케이션 만들기

    * **파일** -> **새로 만들기** -> **프로젝트**로 이동
    * 검색 상자에 `Q#` 입력
    * **Q# 애플리케이션**을 선택합니다.
    * **다음**을 선택합니다.
    * 애플리케이션의 이름 및 위치를 선택합니다.
    * **만들기**

1. 프로젝트를 검사합니다.

    C# 호스트 애플리케이션에 해당하는 `Driver.cs`와 콘솔에 메시지를 출력하는 간단한 작업을 정의하는 Q# 프로그램에 해당하는 `Operation.qs`의 두 파일이 생성된 것을 확인할 수 있습니다.

1. 애플리케이션 실행

    * **디버그** -> **디버깅하지 않고 시작**을 선택합니다.
    * 콘솔 창에 `Hello quantum world!`가 출력된 것을 볼 수 있습니다.

이제 Visual Studio를 사용 하 여 퀀텀 개발을 계속할 수 있습니다.

> [!NOTE]
> * 단일 Visual Studio 솔루션 내에 여러 프로젝트가 있는 경우 솔루션에 포함된 모든 프로젝트는 솔루션과 동일한 폴더 또는 해당 하위 폴더 중 하나에 포함되어야 합니다.  

## <a name="create-a-c-project-using-vs-code"></a>VS Code를 C# 사용 하 여 프로젝트 만들기

1. 필수 조건

    * [VS Code에 대 한 퀀텀 개발 키트](xref:microsoft.quantum.install#develop-with-c-using-visual-studio-code)

1. 새 프로젝트를 만듭니다.

    * **보기** -> **명령 팔레트**로 이동합니다.
    * **Q #: 새 프로젝트 만들기를** 선택 합니다.
    * 애플리케이션을 만들려는 파일 시스템의 위치로 이동합니다.
    * 프로젝트를 만든 후에 **새 프로젝트 열기...** 단추를 클릭합니다.

1. 애플리케이션을 실행합니다.

    * **디버그** -> **디버깅하지 않고 시작**으로 이동합니다.
    * 출력 창에 다음 텍스트가 표시되어야 합니다. `Hello quantum world!`

이제 Visual Studio Code를 사용 하 여 퀀텀 개발을 계속할 수 있습니다.

> [!NOTE]
> * 여러 루트 폴더가 있는 작업 영역은 현재 Visual Studio Code 확장에서 지원되지 않습니다. 단일 VS Code 작업 영역에 여러 프로젝트가 있는 경우 모든 프로젝트가 동일한 루트 폴더 내에 포함되어야 합니다.

## <a name="create-a-c-project-using-the-dotnet-command-line-tool"></a>`dotnet` 명령줄 C# 도구를 사용 하 여 프로젝트 만들기

1. 필수 조건

    * [명령줄에 대 한 퀀텀 개발 키트](xref:microsoft.quantum.install#develop-with-c-using-the-dotnet-command-line-tool)

1. 새 애플리케이션 만들기

    ```bash
    dotnet new console -lang Q# -o <project name>
    ```

1. 새 애플리케이션 디렉터리로 이동합니다.

    ```bash
    cd <project name>
    ```

    애플리케이션의 프로젝트 파일과 함께 Q# 파일(`Operation.qs`) 및 C# 호스트 파일(`Driver.cs`)의 두 파일이 생성된 것을 볼 수 있습니다.

1. 애플리케이션 실행

    ```bash
    dotnet run
    ```

    다음 출력이 표시됩니다. `Hello quantum world!`

이제 명령줄 도구를 사용 하 여 퀀텀 개발을 계속 합니다.

## <a name="whats-next"></a>다음은 무엇일까요?

이제 기본 설정 환경에서 프로젝트를 만들었으므로 퀀텀 개발을 계속할 수 있습니다.
