---
title: 'Q # +를 사용 하 여 개발C#'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 7803846279f230f5fc0ee8424bd39be735a650ca
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036290"
---
# <a name="develop-with-q--c"></a>Q # +를 사용 하 여 개발C#

Q # 작업을 호출 하 C# 는 호스트 프로그램을 개발 하려면 qdk를 설치 합니다.

Q #은 .NET 언어에서 잘 작동 하도록 빌드 되었습니다 (특히 C#). 다양 한 개발 환경 내에서이 페어링 작업을 수행할 수 있습니다.

- [Q # + C# Visual Studio 사용 (Windows)](#VS)
- [Q # + C# Visual Studio Code (Windows, Linux 및 Mac) 사용](#VSC)
- [Q # + C# `dotnet` 명령줄 도구 사용](#command)

## Visual Studio를 사용 하 C# 여 Q # +를 사용 하 여 개발 <a name="VS"></a>

Visual Studio는 Q # 프로그램을 개발 하기 위한 풍부한 환경을 제공 합니다. Q # Visual Studio 확장에는 구문 강조 표시, 코드 완성 및 IntelliSense 지원 뿐만 아니라 Q # 파일 및 프로젝트에 대 한 템플릿이 포함 되어 있습니다.


1. 필수 구성 요소

    - [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, .NET Core 플랫폼 간 개발 워크로드 설정

1. Q# Visual Studio 확장을 설치합니다.

    - [Visual Studio 확장](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) 다운로드 및 설치

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

## Visual Studio Code를 사용 하 여 C# Q # + 개발 <a name="VSC"></a>

Visual Studio Code (VS Code)는 Windows, Linux 및 Mac에서 Q # 프로그램을 개발 하기 위한 풍부한 환경을 제공 합니다.  Q # VS Code 확장에는 Q # 구문 강조 표시, 코드 완성 및 Q # 코드 조각을 위한 지원이 포함 됩니다.

1. 필수 구성 요소

   - [VS 코드](https://code.visualstudio.com/download)
   - [.NET Core SDK 3.1 이상](https://www.microsoft.com/net/download)

1. Quantum VS Code 확장을 설치합니다.

    - [VS Code 확장](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)을 설치합니다.

1. 양자 프로젝트 템플릿을 설치합니다.

   - **보기** -> **명령 팔레트**로 이동합니다.
   - **Q #: 프로젝트 템플릿 설치를** 선택 합니다.

    이제 Quantum Development Kit가 설치되었으며 사용자의 애플리케이션 및 라이브러리에서 사용할 준비가 되었습니다.

1. `Hello World` 애플리케이션을 만들어 설치를 확인합니다.

    - 새 프로젝트를 만듭니다.

        - **보기** -> **명령 팔레트**로 이동합니다.
        - **Q #: 새 프로젝트 만들기를** 선택 합니다.
        - **독립 실행형 콘솔 응용 프로그램** 선택
        - 애플리케이션을 만들려는 파일 시스템의 위치로 이동합니다.
        - 프로젝트를 만든 후에 **새 프로젝트 열기...** 단추를 클릭합니다.

    - VS Code에 대 한 C# 확장을 아직 설치 하지 않은 경우 팝업이 표시 됩니다. 확장을 설치 합니다. 

    - 애플리케이션을 실행합니다.

        - **터미널** -> **새 터미널** 로 이동 합니다.
        - `dotnet run`을 입력합니다.
        - 출력 창에 다음 텍스트가 표시되어야 합니다. `Hello quantum world!`


> [!NOTE]
> * 여러 루트 폴더가 있는 작업 영역은 현재 Visual Studio Code 확장에서 지원되지 않습니다. 단일 VS Code 작업 영역에 여러 프로젝트가 있는 경우 모든 프로젝트가 동일한 루트 폴더 내에 포함되어야 합니다.

## `dotnet` 명령줄 도구를 사용 C# 하 여 Q # +를 사용 하 여 개발<a name="command"></a>

물론 간단하게 .NET Core SDK 및 QDK 프로젝트 템플릿을 설치하여 명령줄에서 Q# 프로그램을 빌드하고 실행할 수도 있습니다. 

1. 필수 구성 요소

    - [.NET Core SDK 3.1 이상](https://www.microsoft.com/net/download)

1. .NET용 양자 프로젝트 템플릿을 설치합니다.

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    이제 Quantum Development Kit가 설치되었으며 사용자의 애플리케이션 및 라이브러리에서 사용할 준비가 되었습니다.

1. `Hello World` 애플리케이션을 만들어 설치를 확인합니다.

    - 새 애플리케이션 만들기

       ```dotnetcli
       dotnet new console -lang "Q#" -o runSayHello
       ```

    - 새 애플리케이션 디렉터리로 이동합니다.

       ```bash
       cd runSayHello
       ```

    애플리케이션의 프로젝트 파일과 함께 Q# 파일(`Operation.qs`) 및 C# 호스트 파일(`Driver.cs`)의 두 파일이 생성된 것을 볼 수 있습니다.

    - 애플리케이션 실행

        ```dotnetcli
        dotnet run
        ```

        다음 출력이 표시됩니다. `Hello quantum world!`

    
## <a name="whats-next"></a>다음 단계

지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.write-program)을 작성 및 실행할 수 있습니다.
