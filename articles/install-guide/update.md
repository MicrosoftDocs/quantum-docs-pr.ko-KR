---
title: Microsoft Quantum Development Kit (QDK)를 업데이트 하는 방법 알아보기
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: fc430a77f88878437e662c5b54507f70f3c6e020
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2019
ms.locfileid: "73185854"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Microsoft Quantum Development Kit (QDK) 업데이트

Microsoft Quantum Development Kit (QDK)를 최신 버전으로 업데이트 하는 방법에 대해 알아봅니다.

이 문서에서는 QDK가 이미 설치 되어 있다고 가정 합니다. 를 처음 설치 하는 경우 [설치 가이드](xref:microsoft.quantum.install)를 참조 하세요.

업데이트 단계는 개발 환경에 따라 달라 집니다. 다음 섹션에서 환경을 선택 합니다.

## <a name="python"></a>파이썬

1. `iqsharp` 커널을 업데이트 합니다.

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. `iqsharp` 버전 확인

    ```bash
    dotnet iqsharp --version
    ```

    다음 출력이 표시됩니다.

    ```bash
    iqsharp: 0.9.1909.3002
    Jupyter Core: 1.1.18837.0
    ```

1. `qsharp` 패키지 업데이트

    ```bash
    pip install qsharp --upgrade
    ```

1. `qsharp` 버전 확인

    ```bash
    pip show qsharp
    ```

    다음 출력이 표시됩니다.

    ```bash
    Name: qsharp
    Version: 0.9.1909.3002
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

1. 이제 업데이트 된 QDK 버전을 사용 하 여 기존 퀀텀 프로그램을 실행할 수 있습니다.

## <a name="jupyter-notebooks"></a>Jupyter Notebook

1. `iqsharp` 커널을 업데이트 합니다.

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. `iqsharp` 버전 확인

    ```bash
    dotnet iqsharp --version
    ```

    다음 출력이 표시됩니다.

    ```bash
    iqsharp: 0.9.1909.3002
    Jupyter Core: 1.1.18837.0
    ```

1. 이제 기존 Jupyter 노트북을 열고 업데이트 된 QDK를 사용 하 여 실행할 수 있습니다.

## <a name="c-on-windows-using-visual-studio"></a>C#Windows에서 Visual Studio 사용

1. Q # Visual Studio 확장 업데이트

    - Visual Studio에서 [퀀텀 Visual studio 확장](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) 에 대 한 업데이트를 승인 하 라는 메시지를 표시 합니다.
    - 업데이트 수락

    > [!NOTE]
    > 프로젝트 템플릿이 확장으로 업데이트 됩니다. 업데이트 된 템플릿은 새로 만든 프로젝트에만 적용 됩니다. 확장이 업데이트 될 때 기존 프로젝트에 대 한 코드는 업데이트 되지 않습니다.

1. QDK 패키지 업데이트

    - 기존 응용 프로그램 열기
    - 솔루션 탐색기에서 **종속성** 을 선택 합니다.
    - **NuGet 패키지 관리** 를 선택 합니다.
    - **Microsoft 양자** 패키지를 최신 버전으로 업데이트 합니다.

1. 이제 최신 QDK를 사용 하 여 응용 프로그램을 실행할 수 있습니다.

## <a name="c-using-vs-code"></a>C#, VS Code 사용

1. 퀀텀 VS Code 확장 업데이트

    - 다시 시작 VS Code
    - **확장** 탭으로 이동 합니다.
    - Visual Studio Code 확장 **에 대 한 Microsoft Quantum Development Kit** 선택
    - 확장 다시 로드

1. 퀀텀 프로젝트 템플릿을 업데이트 합니다.

   - **보기** -> **명령 팔레트** 로 이동
   - **Q #: 프로젝트 템플릿 설치를** 선택 합니다.

1. VS Code에서 기존 응용 프로그램을 엽니다.

   - .Csproj 파일을 편집 하 여 새 패키지 버전을 추가 합니다.

    ```xml
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Standard" Version="0.9.1909.3002" />
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.9.1909.3002" />
    </ItemGroup>
    ```

    다른 `Microsoft.Quantum` 패키지를 사용 하는 경우에도 업데이트 합니다.

1. 이제 업데이트 된 QDK를 사용 하 여 응용 프로그램을 실행할 수 있습니다.

## <a name="c-using-the-dotnet-command-line-tool"></a>C#`dotnet` 명령줄 도구 사용

1. .NET 용 퀀텀 프로젝트 템플릿 업데이트

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. 기존 응용 프로그램 업데이트 및 실행

    - 응용 프로그램에서 QDK 패키지 버전 업데이트

        ```bash
        dotnet add package Microsoft.Quantum.Development.Kit
        dotnet add package Microsoft.Quantum.Standard
        ```

        응용 프로그램에서 다른 `Microsoft.Quantum` 패키지를 사용 하는 경우에도 업데이트 합니다.

    - 애플리케이션 실행

        ```bash
        dotnet run
        ```

    - 새 패키지 버전으로 응용 프로그램이 실행 됩니다.

## <a name="whats-next"></a>다음은 무엇일까요?

선호 하는 환경에서 퀀텀 개발 키트를 업데이트 했으므로 계속 해 서 퀀텀 프로그램을 개발 하 고 실행할 수 있습니다. 프로그램을 아직 작성 하지 않은 경우 [첫 번째 퀀텀 프로그램](xref:microsoft.quantum.write-program)을 시작할 수 있습니다.
