---
title: Q# 명령줄 애플리케이션을 사용하여 개발
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 4311ebf9f72254485a20ba721ea2ce19163f4371
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274196"
---
# <a name="develop-with-q-command-line-applications"></a>Q# 명령줄 애플리케이션을 사용하여 개발

Q# 프로그램은 C#, F# 또는 Python과 같은 호스트 언어로 된 드라이버 없이 단독 실행이 가능합니다.

## <a name="prerequisites"></a>필수 구성 요소

- [.NET Core SDK 3.1 이상](https://www.microsoft.com/net/download)

## <a name="installation"></a>설치

모든 IDE에서 Q# 명령줄 애플리케이션을 빌드할 수 있지만 Q# 애플리케이션용 VS Code(Visual Studio Code) 또는 Visual Studio IDE를 사용하는 것이 좋습니다. 이러한 도구에서 개발하면 다양한 기능에 액세스할 수 있습니다.

VS 코드를 구성하려면 다음을 수행합니다.

1. [VS Code](https://code.visualstudio.com/download)(Windows, Linux 및 Mac)를 다운로드하여 설치합니다.
2. [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)를 설치합니다.

Visual Studio를 구성하려면 다음을 수행합니다.

1. .NET Core 플랫폼 간 개발 워크로드를 사용하도록 설정한 상태에서 [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 이상을 다운로드하여 설치합니다.
2. [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)를 다운로드하여 설치합니다.


## <a name="develop-with-q-using-vs-code"></a>VS Code를 사용하여 Q#으로 개발

Q# 프로젝트 템플릿을 설치합니다.

1. VS Code를 엽니다.
2. **보기** -> **명령 팔레트**를 클릭합니다.
3. **Q#: 프로젝트 템플릿 설치**를 선택합니다.

**Project templates installed successfully**(프로젝트 템플릿이 설치되었습니다)가 표시되면 자체 애플리케이션 및 라이브러리에서 QDK를 사용할 준비가 된 것입니다.

새 프로젝트를 만들려면 다음을 수행합니다.

1. **보기** -> **명령 팔레트**를 클릭하고 **Q#: 새 프로젝트 만들기**를 선택합니다.
2. **Standalone console application**(독립 실행형 콘솔 애플리케이션)을 클릭합니다.
3. 프로젝트를 저장할 위치로 이동하여 **프로젝트 만들기**를 클릭합니다.
4. 프로젝트가 만들어지면 오른쪽 아래에서 **Open new project...** (새 프로젝트 열기)를 클릭합니다.
        
프로젝트를 검사합니다. `Program.qs`라는 소스 파일이 보입니다. 이것은 콘솔에 메시지를 인쇄하는 간단한 작업을 정의하는 Q# 프로그램입니다.

애플리케이션을 실행하려면
1. **터미널** -> **새 터미널**을 클릭합니다.
2. 터미널 프롬프트에 `dotnet run`을 입력합니다.
3. 출력 창에 다음 텍스트가 표시되어야 합니다. `Hello quantum world!`


> [!NOTE]
> 여러 루트 폴더가 있는 작업 영역은 현재 VS Code Q# 확장에서 지원되지 않습니다. 단일 VS Code 작업 영역에 여러 프로젝트가 있는 경우 모든 프로젝트가 동일한 루트 폴더 내에 포함되어야 합니다.

## <a name="develop-with-q-using-visual-studio"></a>Visual Studio를 사용하여 Q#으로 개발

Q# `Hello World` 애플리케이션을 만들어서 Visual Studio 설치를 확인합니다.

새 Q# 애플리케이션을 만들려면 다음을 수행합니다.
1. Visual Studio를 열고 **파일** -> **새로 만들기** -> **프로젝트**를 클릭합니다.
2. 검색 상자에 `Q#`을 입력하고 **Q# 애플리케이션**을 선택한 후 **다음**을 클릭합니다.
3. 애플리케이션의 이름과 위치를 입력하고 **만들기**를 클릭합니다.


프로젝트를 검사합니다. `Program.qs`라는 소스 파일이 보입니다. 이것은 콘솔에 메시지를 인쇄하는 간단한 작업을 정의하는 Q# 프로그램입니다.

애플리케이션을 실행하려면
1. **디버그** -> **디버그하지 않고 시작**을 선택합니다.
2. 콘솔 창에 `Hello quantum world!`가 출력된 것을 볼 수 있습니다.

> [!NOTE]
> 단일 Visual Studio 솔루션 내에 여러 프로젝트가 있는 경우 솔루션에 포함된 모든 프로젝트는 솔루션과 동일한 폴더 또는 해당 하위 폴더 중 하나에 포함되어야 합니다.  


## <a name="next-steps"></a>다음 단계

지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성 및 실행할 수 있습니다.
