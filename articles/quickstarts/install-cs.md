---
title: Q# 및 .NET을 사용하여 개발
description: .NET 언어를 사용하여 Q# 애플리케이션을 만드는 방법을 알아봅니다.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: quickstart
uid: microsoft.quantum.install.cs
no-loc:
- Q#
- $$v
ms.openlocfilehash: de79c361331766572f5608c341be766e071e01b5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844298"
---
# <a name="develop-with-no-locq-and-net"></a>Q# 및 .NET을 사용하여 개발

Q#은 C# 및 F#과 같은 .NET 언어와 잘 작동하도록 빌드되었습니다.
이 가이드에서는 .NET 언어로 작성된 호스트 프로그램에서 Q#을 사용하는 방법을 설명합니다.

먼저 Q# 애플리케이션과 .NET 호스트를 만든 다음, 호스트에서 Q#을 호출하는 방법을 보여줍니다.

## <a name="prerequisites"></a>필수 구성 요소

- [Q# 프로젝트에서 사용할](xref:microsoft.quantum.install.standalone) Quantum Development Kit를 설치합니다.

## <a name="creating-a-no-locq-library-and-a-net-host"></a>Q# 라이브러리 및 .NET 호스트 만들기

첫 번째 단계에서는 Q# 라이브러리용 프로젝트 및 Q# 라이브러리에 정의된 작업 및 함수를 호출할 .NET 호스트를 만듭니다.

사용하는 개발 환경에 해당하는 탭의 지침을 따릅니다.
Visual Studio 또는 VS Code 이외의 편집기를 사용하는 경우 간단하게 명령 프로그램 단계를 따르면 됩니다.

### <a name="visual-studio-code-or-command-prompt"></a>[Visual Studio Code 또는 명령 프롬프트](#tab/tabid-cmdline)

- 새 Q# 라이브러리 만들기

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- 새 C# 또는 F# 콘솔 프로젝트 만들기

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- Q# 라이브러리를 호스트 프로그램에서 참조로 추가

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- [선택 사항] 두 프로젝트 모두에 대한 솔루션 만들기

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

- 새 Q# 라이브러리 만들기
  - **파일** -> **새로 만들기** -> **프로젝트** 로 이동
  - 검색 상자에 “Q#” 입력
  - **Q# 라이브러리** 선택
  - **다음** 을 선택합니다.
  - 라이브러리의 이름 및 위치 선택
  - "솔루션 및 프로젝트를 같은 디렉터리에 배치"를 **선택하지 않아야** 합니다.
  - **만들기**
- 새 C# 또는 F# 호스트 프로그램 만들기
  - **파일** → **새로 만들기** → **프로젝트** 로 이동
  - C# 또는 F#에 대한 "콘솔 앱(.NET Core)" 선택
  - **다음** 을 선택합니다.
  - *솔루션* 에서 "솔루션에 추가" 선택
  - 호스트 프로그램의 이름 선택
  - **만들기**

**_

## <a name="calling-into-no-locq-from-net"></a>.NET에서 Q# 호출

위의 지침에 따라 프로젝트를 설정한 후에는 .NET 콘솔 애플리케이션에서 Q#을 호출할 수 있습니다.
Q# 컴파일러는 시뮬레이터에서 퀀텀 프로그램을 실행할 수 있도록 각 Q# 작업 및 함수에 대해 .NET 클래스를 생성합니다.

예를 들어 [.NET 상호 운용성 샘플](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet)에는 다음과 같은 Q# 연산 예제가 포함되어 있습니다.

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

퀀텀 시뮬레이터의 .NET에서 이 작업을 호출하려면 Q# 컴파일러에서 생성된 `RunAlgorithm` .NET 클래스의 `Run` 메서드를 사용하면 됩니다.

### <a name="c"></a>[C#](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[F#](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

_**
    
## <a name="next-steps"></a>다음 단계

Q# 애플리케이션 및 .NET과의 상호 운용성을 위한 Quantum Development Kit가 설정되었으면 [첫 번째 퀀텀 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성하고 실행할 수 있습니다.
