---
title: '드라이버 및 호스트 언어 없이 Q # 프로그램 실행'
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: e83acaf10af952da06abf4737ad2ec91f1cf1b8e
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/01/2020
ms.locfileid: "82706804"
---
# <a name="q-command-line-applications"></a>Q # 명령줄 응용 프로그램

Q # 프로그램은 c #, F #, Python 등의 호스트 언어로 드라이버를 사용 하지 않고 직접 실행할 수 있습니다.

## <a name="pre-requisites"></a>필수 구성 요소

- [.NET Core SDK 3.1 이상](https://www.microsoft.com/net/download)

## <a name="installation"></a>설치

모든 IDE에서 Q # 명령줄 응용 프로그램을 빌드할 수 있지만, Q # 응용 프로그램에 Visual Studio Code (VS Code) 또는 Visual Studio IDE를 사용 하는 것이 좋습니다. VS Code 또는 Visual Studio와 QDK Visual Studio Code 확장을 사용 하 여 보다 다양 한 기능에 액세스할 수 있습니다.

- [VS Code](https://code.visualstudio.com/download) (Windows, Linux 및 Mac) 설치
- VS Code 또는 [용 Qdk 확장](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode) 을 설치 합니다.
- [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, .NET Core 플랫폼 간 개발 워크로드 설정
- [Visual Studio 확장](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) 다운로드 및 설치


## <a name="develop-with-q-using-vs-code"></a>VS Code를 사용 하 여 개발:

양자 프로젝트 템플릿을 설치합니다.

- **보기** -> **명령 팔레트** 로 이동
- **Q #: 프로젝트 템플릿 설치를** 선택 합니다.

이제 Quantum Development Kit가 설치되었으며 사용자의 애플리케이션 및 라이브러리에서 사용할 준비가 되었습니다.
- 새 프로젝트를 만듭니다.
  - **보기** -> **명령 팔레트** 로 이동
  - **Q #: 새 프로젝트 만들기를** 선택 합니다.
  - **독립 실행형 콘솔 응용 프로그램** 선택
  - 애플리케이션을 만들려는 파일 시스템의 위치로 이동합니다.
  - 프로젝트를 만든 후에 **새 프로젝트 열기...** 단추를 클릭합니다.
        
- 프로젝트를 검사합니다.
  - 메시지를 콘솔에 출력 하는 `Program.qs` 간단한 작업을 정의 하는 Q # 프로그램인 이라는 파일이 생성 된 것을 볼 수 있습니다.

- 애플리케이션을 실행합니다.
  - **터미널** -> **새 터미널** 로 이동
  - `dotnet run`을 입력합니다.
  - 출력 창에 다음 텍스트가 표시되어야 합니다. `Hello quantum world!`


> [!NOTE]
> * 여러 루트 폴더가 있는 작업 영역은 현재 Visual Studio Code 확장에서 지원되지 않습니다. 단일 VS Code 작업 영역에 여러 프로젝트가 있는 경우 모든 프로젝트가 동일한 루트 폴더 내에 포함되어야 합니다.

## <a name="develop-with-q-using-visual-studio"></a>Visual Studio를 사용 하 여 Q #을 사용 하 여 개발

`Hello World` 애플리케이션을 만들어 설치를 확인합니다.

- 새 Q# 애플리케이션 만들기
  - **파일** -> **새로 만들기** -> **프로젝트** 로 이동
  - 검색 상자에 `Q#` 입력
  - **Q# 애플리케이션**을 선택합니다.
  - **다음**을 선택합니다.
  - 애플리케이션의 이름 및 위치를 선택합니다.
  - **만들기** 선택

- 프로젝트를 검사합니다.
  - 라는 `Program.qs` 파일이 만들어진 것을 확인할 수 있습니다 .이는 콘솔에 메시지를 인쇄 하는 간단한 작업을 정의 하는 Q # 프로그램입니다.

- 애플리케이션 실행
  -  -> **디버깅 하지 않고 시작** **을 선택 합니다**.
  - 콘솔 창에 `Hello quantum world!`가 출력된 것을 볼 수 있습니다.

> [!NOTE]
> * 단일 Visual Studio 솔루션 내에 여러 프로젝트가 있는 경우 솔루션에 포함된 모든 프로젝트는 솔루션과 동일한 폴더 또는 해당 하위 폴더 중 하나에 포함되어야 합니다.  


## <a name="whats-next"></a>새로운 기능

지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.write-program)을 작성 및 실행할 수 있습니다.
