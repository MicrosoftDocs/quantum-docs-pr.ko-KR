---
title: 'Q # 명령줄 응용 프로그램을 사용 하 여 개발'
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 4311ebf9f72254485a20ba721ea2ce19163f4371
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630270"
---
# <a name="develop-with-q-command-line-applications"></a>Q # 명령줄 응용 프로그램을 사용 하 여 개발

Q # 프로그램은 c #, F #, Python 등의 호스트 언어로 드라이버를 사용 하지 않고 직접 실행할 수 있습니다.

## <a name="prerequisites"></a>전제 조건

- [.NET Core SDK 3.1 이상](https://www.microsoft.com/net/download)

## <a name="installation"></a>설치

모든 IDE에서 Q # 명령줄 응용 프로그램을 빌드할 수 있지만, Q # 응용 프로그램에 Visual Studio Code (VS Code) 또는 Visual Studio IDE를 사용 하는 것이 좋습니다. 이러한 도구에서 개발 하면 다양 한 기능에 액세스할 수 있습니다.

VS Code를 구성 하려면:

1. [VS Code](https://code.visualstudio.com/download) (Windows, Linux 및 Mac)를 다운로드 하 여 설치 합니다.
2. [Microsoft QDK VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)를 설치 합니다.

Visual Studio를 구성 하려면:

1. .NET Core 플랫폼 간 개발 워크 로드를 사용 하 여 [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 이상을 다운로드 하 고 설치 합니다.
2. [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)를 다운로드 하 여 설치 합니다.


## <a name="develop-with-q-using-vs-code"></a>VS Code를 사용 하 여 개발:

Q # 프로젝트 템플릿을 설치 합니다.

1. VS Code를 엽니다.
2. **보기**  ->  **명령 팔레트**를 클릭 합니다.
3. **Q #: 프로젝트 템플릿 설치**를 선택 합니다.

**프로젝트 템플릿이 성공적으로** 표시 되 면 qdk 응용 프로그램 및 라이브러리에서 사용할 준비가 된 것입니다.

새 프로젝트를 만들려면 다음을 수행 합니다.

1. **보기**  ->  **명령 팔레트** 를 클릭 하 고 **Q #: 새 프로젝트 만들기**를 선택 합니다.
2. **독립 실행형 콘솔 응용 프로그램**을 클릭 합니다.
3. 프로젝트를 저장할 위치로 이동 하 고 **프로젝트 만들기**를 클릭 합니다.
4. 프로젝트가 성공적으로 생성 되 면 오른쪽 아래에서 **새 프로젝트 열기** ...를 클릭 합니다.
        
프로젝트를 검사 합니다. `Program.qs`콘솔에 메시지를 인쇄 하는 간단한 작업을 정의 하는 Q # 프로그램인 라는 원본 파일이 표시 됩니다.

애플리케이션을 실행하려면
1. **터미널**  ->  **새 터미널**을 클릭 합니다.
2. 터미널 프롬프트에서을 입력 `dotnet run` 합니다.
3. 출력 창에 다음 텍스트가 표시되어야 합니다. `Hello quantum world!`


> [!NOTE]
> 여러 루트 폴더가 있는 작업 영역은 현재 VS Code Q # 확장에서 지원 되지 않습니다. 단일 VS Code 작업 영역에 여러 프로젝트가 있는 경우 모든 프로젝트가 동일한 루트 폴더 내에 포함되어야 합니다.

## <a name="develop-with-q-using-visual-studio"></a>Visual Studio를 사용 하 여 Q #을 사용 하 여 개발

Q # 응용 프로그램을 만들어 Visual Studio 설치를 확인 `Hello World` 합니다.

새 Q # 응용 프로그램을 만들려면 다음을 수행 합니다.
1. Visual Studio를 열고 **파일**  ->  **새로 만들기**  ->  **프로젝트**를 클릭 합니다.
2. `Q#`검색 상자에를 입력 하 고 **Q # 응용 프로그램** 을 선택한 후 **다음**을 클릭 합니다.
3. 응용 프로그램의 이름과 위치를 입력 하 고 **만들기**를 클릭 합니다.


프로젝트를 검사 합니다. `Program.qs`콘솔에 메시지를 인쇄 하는 간단한 작업을 정의 하는 Q # 프로그램인 라는 원본 파일이 표시 됩니다.

애플리케이션을 실행하려면
1. **Debug**  ->  **디버깅 하지 않고 시작**을 선택 합니다.
2. 콘솔 창에 `Hello quantum world!`가 출력된 것을 볼 수 있습니다.

> [!NOTE]
> 하나의 Visual Studio 솔루션에 여러 프로젝트가 있는 경우 솔루션에 포함 된 모든 프로젝트는 솔루션과 동일한 폴더 또는 해당 하위 폴더 중 하나에 있어야 합니다.  


## <a name="next-steps"></a>다음 단계

지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성 및 실행할 수 있습니다.
