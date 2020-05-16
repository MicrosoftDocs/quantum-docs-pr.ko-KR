---
title: QDK (퀀텀 개발 키트) 업데이트
description: 'Q # 프로젝트와 Microsoft Quantum Development Kit를 현재 버전으로 업데이트 하는 방법을 설명 합니다.'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 53f72f1d49ae32a5a8572a1cf68a66a1d9b45e4a
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426903"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Microsoft Quantum Development Kit (QDK) 업데이트

Microsoft Quantum Development Kit (QDK)를 최신 버전으로 업데이트 하는 방법에 대해 알아봅니다.

이 문서에서는 QDK가 이미 설치 되어 있다고 가정 합니다. 를 처음 설치 하는 경우 [설치 가이드](xref:microsoft.quantum.install)를 참조 하세요.

최신 QDK 릴리스를 최신 상태로 유지 하는 것이 좋습니다. 최신 QDK 버전으로 업그레이드 하려면이 업데이트 가이드를 따르세요. 프로세스는 다음 두 부분으로 구성 됩니다.
1. 기존 Q # 파일 및 프로젝트를 업데이트 하 여 코드를 업데이트 된 구문에 맞게 정렬
2. 선택한 개발 환경에 대 한 QDK 자체 업데이트 

## <a name="updating-q-projects"></a>Q # 프로젝트 업데이트 

C # 또는 Python을 사용 하 여 Q # 작업을 호스트 하는지 여부에 관계 없이 다음 지침에 따라 Q # 프로젝트를 업데이트 합니다.

1. 먼저 [.NET Core SDK 3.1](https://dotnet.microsoft.com/download)의 최신 버전이 있는지 확인 합니다. 명령 프롬프트에서 다음 명령을 실행 합니다.

    ```dotnetcli
    dotnet --version
    ```

    출력이 이상 인지 확인 `3.1.100` 합니다. 그렇지 않은 경우 [최신 버전](https://dotnet.microsoft.com/download) 을 설치 하 고 다시 확인 합니다. 그런 다음 설치 (Visual Studio, Visual Studio Code 또는 직접 명령줄)에 따라 아래 지침을 따릅니다.

### <a name="update-q-projects-in-visual-studio"></a>Visual Studio의 업데이트 Q # 프로젝트
 
1. 최신 버전의 Visual Studio 2019로 업데이트 합니다. 지침은 [여기](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) 를 참조 하세요.
2. Visual Studio에서 솔루션을 엽니다.
3. 메뉴에서 **Build**  ->  **솔루션 정리** 빌드를 선택 합니다.
4. 각 .csproj 파일에서 대상 프레임 워크를 `netcoreapp3.1` (또는 `netstandard2.1` 라이브러리 프로젝트인 경우)로 업데이트 합니다.
    즉, 다음 폼의 줄을 편집 합니다.

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    대상 프레임 워크를 지정 하는 방법에 대 한 자세한 내용은 [여기](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)에서 찾을 수 있습니다.
5. 솔루션의 모든 파일을 저장 하 고 닫습니다.
6. **도구**  ->  **명령줄**  ->  **개발자 명령 프롬프트** 선택
7. 솔루션의 각 프로젝트에 대해 다음 명령을 실행 합니다.

    ```dotnetcli
    dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   프로젝트에서 다른 Microsoft 양자 패키지 (예: 양자)를 사용 하는 경우에도 명령을 실행 합니다.
8. 명령 프롬프트를 닫고 빌드 솔루션 **빌드**  ->  **Build Solution** 를 선택 합니다 (솔루션 다시 빌드를 선택 *하지* 않음).

이제 [Visual Studio QDK 확장 업데이트](#update-visual-studio-qdk-extension)로 건너뛸 수 있습니다.


### <a name="update-q-projects-in-visual-studio-code"></a>Visual Studio Code에서 Q # 프로젝트 업데이트

1. Visual Studio Code에서 업데이트할 프로젝트를 포함 하는 폴더를 엽니다.
2. **터미널**  ->  **새 터미널** 선택
3. 명령줄을 사용 하 여 업데이트 하는 방법에 대 한 지침을 따르세요 (바로 아래).

### <a name="update-q-projects-using-the-command-line"></a>명령줄을 사용 하 여 업데이트 Q # 프로젝트

1. 프로젝트 파일이 포함 된 폴더로 이동 합니다.
2. 다음 명령 실행:

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. 각 .csproj 파일에서 대상 프레임 워크를 `netcoreapp3.1` (또는 `netstandard2.1` 라이브러리 프로젝트인 경우)로 업데이트 합니다.
    즉, 다음 폼의 줄을 편집 합니다.

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    대상 프레임 워크를 지정 하는 방법에 대 한 자세한 내용은 [여기](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)에서 찾을 수 있습니다.
4. 다음 명령 실행:

    ```dotnetcli
    dotnet add package Microsoft.Quantum.Development.Kit
    ```

    프로젝트에서 다른 Microsoft 양자 패키지 (예: 양자)를 사용 하는 경우에도 명령을 실행 합니다.
5. 모든 파일을 저장 하 고 닫습니다.
6. 각 프로젝트 종속성에 대해 1-4을 반복한 다음 주 프로젝트가 포함 된 폴더로 다시 이동 하 고를 실행 합니다.

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

이제 Q # 프로젝트를 업데이트 하 고 아래 지침에 따라 QDK 자체를 업데이트 합니다.

## <a name="updating-the-qdk"></a>QDK 업데이트

QDK를 업데이트 하는 프로세스는 개발 언어 및 환경에 따라 달라 집니다.
아래에서 개발 환경을 선택 합니다.

* [Python: IQ # 확장 업데이트](#update-iq-for-python)
* [Jupyter 노트북: IQ # 확장 업데이트](#update-iq-for-jupyter-notebooks)
* [Visual Studio: QDK 확장 업데이트](#update-visual-studio-qdk-extension)
* [VS Code: QDK 확장 업데이트](#update-vs-code-qdk-extension)
* [명령줄 및 c #: 프로젝트 템플릿 업데이트](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a>Python 용 IQ # 업데이트

1. 커널을 업데이트 합니다. `iqsharp` 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. 버전 확인 `iqsharp`

    ```dotnetcli
    dotnet iqsharp --version
    ```

    다음과 같은 내용이 출력됩니다.

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    `iqsharp`버전이 더 높을 경우 [최신 릴리스와](xref:microsoft.quantum.relnotes)일치 해야 합니다.

3. 패키지 업데이트 `qsharp`

    ```bash
    pip install qsharp --upgrade
    ```

4. 버전 확인 `qsharp`

    ```bash
    pip show qsharp
    ```

    다음과 같은 내용이 출력됩니다.

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. 파일의 위치에서 다음 명령을 실행 합니다. `.qs`

    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. 이제 업데이트 된 QDK 버전을 사용 하 여 기존 퀀텀 프로그램을 실행할 수 있습니다.

### <a name="update-iq-for-jupyter-notebooks"></a>Jupyter 노트북용 IQ # 업데이트

1. 커널을 업데이트 합니다. `iqsharp`

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. 버전 확인 `iqsharp`

    ```dotnetcli
    dotnet iqsharp --version
    ```

    다음과 유사하게 출력될 것입니다.

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    `iqsharp`버전이 더 높을 경우 [최신 릴리스와](xref:microsoft.quantum.relnotes)일치 해야 합니다.

3. Jupyter Notebook의 셀에서 다음 명령을 실행 합니다.

    ```
    %workspace reload
    ```

4. 이제 기존 Jupyter 노트북을 열고 업데이트 된 QDK를 사용 하 여 실행할 수 있습니다.

### <a name="update-visual-studio-qdk-extension"></a>Visual Studio QDK 확장 업데이트

1. Q # Visual Studio 확장 업데이트

    - Visual Studio에서 [퀀텀 Visual studio 확장](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) 에 대 한 업데이트를 승인 하 라는 메시지를 표시 합니다.
    - 업데이트 수락

    > [!NOTE]
    > 프로젝트 템플릿이 확장으로 업데이트 됩니다. 업데이트 된 템플릿은 새로 만든 프로젝트에만 적용 됩니다. 확장이 업데이트 될 때 기존 프로젝트에 대 한 코드는 업데이트 되지 않습니다.

### <a name="update-vs-code-qdk-extension"></a>VS Code QDK 확장 업데이트

1. 퀀텀 VS Code 확장 업데이트

    - 다시 시작 VS Code
    - **확장** 탭으로 이동 합니다.
    - Visual Studio Code 확장 **에 대 한 Microsoft Quantum Development Kit** 선택
    - 확장 다시 로드

2. 퀀텀 프로젝트 템플릿을 업데이트 합니다.

   - **보기**  ->  **명령 팔레트** 로 이동
   - **Q #: 프로젝트 템플릿 설치를** 선택 합니다.
   - 몇 초 후에 "프로젝트 템플릿을 설치 했습니다."를 확인 하는 팝업이 표시 됩니다.

### <a name="c-using-the-dotnet-command-line-tool"></a>C #, `dotnet` 명령줄 도구 사용

1. .NET 용 퀀텀 프로젝트 템플릿 업데이트

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```