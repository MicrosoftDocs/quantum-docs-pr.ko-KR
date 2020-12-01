---
title: QDK(Quantum Development Kit) 업데이트
description: Q# 프로젝트와 Microsoft Quantum Development Kit를 현재 버전으로 업데이트하는 방법을 설명합니다.
author: bradben
ms.author: v-benbra
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
no-loc:
- Q#
- $$v
ms.openlocfilehash: d9678a61f5fe4ca466b6a84e9e4b68321c5baee3
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834926"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Microsoft QDK(Quantum Development Kit) 업데이트

Microsoft QDK(Quantum Development Kit)를 최신 버전으로 업데이트하는 방법에 대해 알아봅니다.

이 문서에서는 QDK가 이미 설치되어 있다고 가정합니다. 처음 설치하는 경우에는 [설치 가이드](xref:microsoft.quantum.install)를 참조하세요.

최신 QDK 릴리스를 사용하여 최신 상태로 유지하는 것이 좋습니다. 업데이트 가이드에 따라 최신 QDK 버전으로 업그레이드하세요. 프로세스는 다음 두 부분으로 구성됩니다.
1. 기존 Q# 파일 및 프로젝트를 업데이트하여 업데이트된 구문에 맞게 코드를 조정합니다.
2. 선택한 개발 환경에 맞게 QDK를 업데이트합니다.

## <a name="updating-no-locq-projects"></a>Q# 프로젝트 업데이트 

Q# 작업을 호스트하는 데 C#과 Python 중 무엇을 사용하든, 다음 지침에 따라 Q# 프로젝트를 업데이트합니다.

1. 먼저 [.NET Core SDK 3.1](https://dotnet.microsoft.com/download) 최신 버전이 있는지 확인합니다. 명령 프롬프트에서 다음 명령을 실행합니다.

    ```dotnetcli
    dotnet --version
    ```

    출력이 `3.1.100` 이상인지 확인합니다. 그렇지 않으면, [최신 버전](https://dotnet.microsoft.com/download)을 설치하고 다시 확인합니다. 그런 다음, 설정(Visual Studio, Visual Studio Code 또는 명령 프롬프트에서 직접)에 따라 아래 지침을 따릅니다.

### <a name="update-no-locq-projects-in-visual-studio"></a>Visual Studio에서 Q# 프로젝트 업데이트
 
1. 최신 버전의 Visual Studio 2019로 업데이트합니다. (자세한 내용은 [여기](https://docs.microsoft.com/visualstudio/install/update-visual-studio)를 참조하세요.)
2. Visual Studio에서 솔루션을 엽니다.
3. 메뉴에서 **빌드** -> **솔루션 정리** 를 선택합니다.
4. 각 .csproj 파일에서 대상 프레임워크를 `netcoreapp3.1`(라이브러리 프로젝트인 경우 `netstandard2.1`)로 업데이트합니다.
    즉, 다음 형태의 줄을 편집합니다.

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    대상 프레임워크를 지정하는 방법에 대한 자세한 내용은 [여기](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)를 참조하세요.

5. 아래 줄을 참조하여, 각 .csproj 파일에서 SDK를 `Microsoft.Quantum.Sdk`로 설정합니다. 버전 번호는 사용 가능한 최신 버전이어야 하며 [릴리스 정보](https://docs.microsoft.com/quantum/relnotes/)를 검토하여 확인할 수 있습니다.

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    ```

6. 솔루션의 모든 파일을 저장하고 닫습니다.

7. **도구** -> **명령줄** -> **개발자 명령 프롬프트** 를 선택합니다. 또는 Visual Studio에서 패키지 관리 콘솔을 사용할 수 있습니다.

8. 솔루션의 각 프로젝트에 대해 다음 명령을 실행하여 패키지를 **제거** 합니다.

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   프로젝트에서 다른 Microsoft.Quantum 또는 Microsoft.Azure.Quantum 패키지(예: Microsoft.Quantum.Numerics)를 사용하는 경우 **add** 명령을 실행하여 사용된 버전을 업데이트합니다.

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. 명령 프롬프트를 닫고 **빌드** -> **솔루션 빌드** 를 선택합니다. (솔루션 다시 빌드는 선택하지 *마십시오*.)

이제 [Visual Studio QDK 확장 업데이트](#update-visual-studio-qdk-extension)로 건너뛸 수 있습니다.


### <a name="update-no-locq-projects-in-visual-studio-code"></a>Visual Studio Code에서 Q# 프로젝트 업데이트

1. Visual Studio Code에서 업데이트할 프로젝트가 포함된 폴더를 엽니다.
2. **터미널** -> **새 터미널** 을 선택합니다.
3. 명령 프롬프트를 사용하여 업데이트하는 지침을 따릅니다(바로 아래).

### <a name="update-no-locq-projects-using-the-command-prompt"></a>명령 프롬프트를 사용하여 Q# 프로젝트 업데이트

1. 주 프로젝트 파일이 포함된 폴더로 이동합니다.

2. 다음 명령을 실행합니다.

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. QDK의 현재 버전을 확인합니다. 알아보려면 [릴리스 정보](https://docs.microsoft.com/quantum/relnotes/)를 검토하세요. 버전은 `0.12.20072031`과 비슷한 형식입니다.

4. 각 `.csproj` 파일에서 다음 단계를 진행합니다.

    - 대상 프레임워크를 `netcoreapp3.1`(라이브러리 프로젝트인 경우 `netstandard2.1`)로 업데이트합니다. 즉, 다음 형태의 줄을 편집합니다.

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        대상 프레임워크를 지정하는 방법에 대한 자세한 내용은 [여기](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)를 참조하세요.

    - 프로젝트 정의에서 SDK에 대한 참조를 바꿉니다. 버전 번호가 **3단계** 에서 확인한 값과 일치하는지 확인합니다.

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
        ```

    - `Microsoft.Quantum.Development.Kit` 패키지에 대한 참조가 있으면(다음 항목에 지정됨) 제거합니다.

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - 모든 Microsoft Quantum 패키지 버전을 가장 최근에 릴리스된 QDK 버전(**3단계** 에서 확인함)으로 업데이트합니다. 해당 패키지는 다음과 같은 패턴으로 이름이 지정됩니다.

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        패키지에 대한 참조는 다음과 같은 형식입니다.

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.12.20072031" />
        ```

    - 업데이트된 파일을 저장합니다.

    - 다음을 수행하여 프로젝트의 종속성을 복원합니다.

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. 주 프로젝트가 포함된 폴더로 다시 이동하여 다음을 실행합니다.

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

Q# 프로젝트가 업데이트되었으면 아래 지침에 따라 QDK 자체를 업데이트합니다.

## <a name="updating-the-qdk"></a>QDK 업데이트

QDK를 업데이트하는 프로세스는 개발 언어와 환경에 따라 달라집니다.
아래에서 개발 환경을 선택하세요.

* [Python: `qsharp` 패키지 업데이트](#update-the-qsharp-python-package)
* [Jupyter Notebook: IQ# 커널 업데이트](#update-the-iq-jupyter-kernel)
* [Visual Studio: QDK 확장 업데이트](#update-visual-studio-qdk-extension)
* [VS Code: QDK 확장 업데이트](#update-vs-code-qdk-extension)
* [명령줄 및 C#: 프로젝트 템플릿 업데이트](#c-using-the-dotnet-command-line-tool)


### <a name="update-the-qsharp-python-package"></a>`qsharp` Python 패키지 업데이트

업데이트 절차는 처음에 conda를 사용하여 설치했는지 아니면 .NET CLI와 pip를 사용하여 설치했는지에 따라 달라집니다.

#### <a name="update-using-conda-recommended"></a>[conda를 사용하여 업데이트(권장)](#tab/tabid-conda)

1. `qsharp` 패키지를 설치한 conda 환경을 활성화하고, 다음 명령을 실행하여 환경을 업데이트합니다.

    ```
    conda update -c quantum-engineering qsharp
    ```

1. `.qs` 파일이 있는 위치에서 다음 명령을 실행합니다.

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

#### <a name="update-using-net-cli-and-pip-advanced"></a>[.NET CLI 및 pip를 사용하여 업데이트(고급)](#tab/tabid-dotnetcli)

1. `iqsharp` 커널을 업데이트합니다. 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. `iqsharp` 버전을 확인합니다.

    ```dotnetcli
    dotnet iqsharp --version
    ```

    다음 출력이 표시됩니다.

    ```
    iqsharp: 0.12.20072031
    Jupyter Core: 1.4.0.0
    ```

    `iqsharp` 버전이 더 높은 경우에는 걱정할 필요가 없습니다. [최신 릴리스](xref:microsoft.quantum.relnotes)와 일치해야 합니다.

1. 다음과 같이 `qsharp` 패키지를 업데이트합니다.

    ```
    pip install qsharp --upgrade
    ```

1. 다음과 같이 `qsharp` 버전을 확인합니다.

    ```
    pip show qsharp
    ```

    다음 출력이 표시됩니다.

    ```
    Name: qsharp
    Version: 0.12.2007.2031
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

1. `.qs` 파일이 있는 위치에서 다음 명령을 실행합니다.

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

***

이제 업데이트된 `qsharp` Python 패키지를 사용하여 기존 퀀텀 프로그램을 실행할 수 있습니다.

### <a name="update-the-ino-locq-jupyter-kernel"></a>IQ# Jupyter 커널 업데이트

업데이트 절차는 처음에 conda를 사용하여 설치했는지 아니면 .NET CLI와 pip를 사용하여 설치했는지에 따라 달라집니다.

#### <a name="update-using-conda-recommended"></a>[conda를 사용하여 업데이트(권장)](#tab/tabid-conda)

1. `qsharp` 패키지를 설치한 conda 환경을 활성화하고, 다음 명령을 실행하여 환경을 업데이트합니다.

    ```
    conda update -c quantum-engineering qsharp
    ```

1. 기존 Q# Jupyter Notebook의 각 셀에서 다음 명령을 실행합니다.

    ```
    %workspace reload
    ```

#### <a name="update-using-net-cli-and-pip-advanced"></a>[.NET CLI 및 pip를 사용하여 업데이트(고급)](#tab/tabid-dotnetcli)

1. 다음과 같이 `Microsoft.Quantum.IQSharp` 패키지를 업데이트합니다.

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. 다음과 같이 `iqsharp` 버전을 확인합니다.

    ```dotnetcli
    dotnet iqsharp --version
    ```

    다음과 유사하게 출력될 것입니다.

    ```
    iqsharp: 0.12.20072031
    Jupyter Core: 1.4.0.0
    ```

    `iqsharp` 버전이 더 높은 경우에는 걱정할 필요가 없습니다. [최신 릴리스](xref:microsoft.quantum.relnotes)와 일치해야 합니다.

1. 기존 Q# Jupyter Notebook의 각 셀에서 다음 명령을 실행합니다.

    ```
    %workspace reload
    ```

***

이제 업데이트된 IQ# 커널을 사용하여 기존 Q# Jupyter Notebook을 실행할 수 있습니다.

### <a name="update-visual-studio-qdk-extension"></a>Visual Studio QDK 확장 업데이트

1. Q# Visual Studio 확장 업데이트

    - [Quantum Visual Studio 확장](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)에 대한 업데이트를 수락하라는 메시지가 Visual Studio에 표시됩니다.
    - 업데이트를 수락합니다.

    > [!NOTE]
    > 프로젝트 템플릿이 확장으로 업데이트됩니다. 업데이트된 템플릿은 새로 만든 프로젝트에만 적용됩니다. 확장이 업데이트될 때 기존 프로젝트에 대한 코드는 업데이트되지 않습니다.

### <a name="update-vs-code-qdk-extension"></a>VS Code QDK 확장 업데이트

1. Quantum VS Code 확장 업데이트

    - VS Code를 다시 시작합니다.
    - **확장** 탭으로 이동합니다.
    - **Microsoft Quantum Development Kit for Visual Studio Code** 확장을 선택합니다.
    - 확장을 다시 로드합니다.

### <a name="c-using-the-dotnet-command-line-tool"></a>C#, `dotnet` 명령줄 도구 사용

1. .NET용 Quantum 프로젝트 템플릿을 업데이트합니다.

    명령 프롬프트에서:

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

   또는 명령줄 템플릿을 사용하고 VS Code QDK 확장이 이미 설치되어 있는 경우 확장 자체에서 프로젝트 템플릿을 업데이트할 수 있습니다.

   - [QDK 확장 업데이트](#update-vs-code-qdk-extension)
   - VS Code에서 **보기** -> **명령 팔레트** 로 이동합니다.
   - **Q#을 선택합니다. 명령줄 프로젝트 템플릿 설치** 를 선택합니다.
   - 몇 초 후에 "project templates installed successfully"(프로젝트 템플릿이 설치되었습니다)라는 팝업이 나타납니다.
