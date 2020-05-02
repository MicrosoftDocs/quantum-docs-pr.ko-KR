---
title: Q# + C#을 사용하여 개발
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 5bcb036b0b32e64d43f90e9a068d9dcc237890ba
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/01/2020
ms.locfileid: "82680174"
---
# <a name="using-q-with-c-and-f"></a>C\# 및 F와 함께 Q # 사용\#

Q #은 c # 및 F #과 같은 .NET 언어에서 잘 작동 하도록 빌드됩니다.
이 가이드에서는 .NET 언어로 작성 된 호스트 프로그램과 함께 Q #을 사용 하는 방법을 설명 합니다.

## <a name="prerequisites"></a>사전 요구 사항

- [Q # 명령줄 프로젝트와 함께 사용 하기 위해](xref:microsoft.quantum.install.standalone)퀀텀 개발 키트를 설치 합니다.

## <a name="creating-a-q-library-and-a-net-host"></a>Q # 라이브러리 및 .NET 호스트 만들기

첫 번째 단계는 q # 라이브러리에 대 한 프로젝트와 Q # 라이브러리에 정의 된 작업 및 함수를 호출 하는 .NET 호스트에 대 한 프로젝트를 만드는 것입니다.

### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

- 새 Q # 라이브러리 만들기
  - **파일** -> **새로 만들기** -> **프로젝트** 로 이동
  - 검색 상자에 "Q #" 입력
  - **Q # 라이브러리** 를 선택 합니다.
  - **다음**을 선택합니다.
  - 라이브러리의 이름 및 위치 선택
  - "프로젝트 및 솔루션을 동일한 디렉터리에 저장"이 **선택 취소** 되어 있는지 확인 합니다.
  - **만들기** 선택
- 새 c # 또는 F # 호스트 프로그램 만들기
  - **파일** → **새로 만들기** → **프로젝트** 로 이동 합니다.
  - C # 또는 F에 대해 "콘솔 앱 (.NET Core") "을 선택 합니다. #
  - **다음**을 선택합니다.
  - *솔루션*에서 "솔루션에 추가"를 선택 합니다.
  - 호스트 프로그램의 이름 선택
  - **만들기** 선택

### <a name="visual-studio-code-or-command-line"></a>[Visual Studio Code 또는 명령줄](#tab/tabid-cmdline)

- 새 Q # 라이브러리 만들기

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- 새 c # 또는 F # 콘솔 프로젝트 만들기

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- 호스트 프로그램에서 참조로 Q # 라이브러리를 추가 합니다.

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- 필드 두 프로젝트에 대 한 솔루션을 만듭니다.

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

***

## <a name="calling-into-q-from-net"></a>.NET에서 Q #으로 호출

위의 지침에 따라 프로젝트를 설정한 후에는 .NET 콘솔 응용 프로그램에서 Q #을 호출할 수 있습니다.
Q # 컴파일러는 시뮬레이터에서 퀀텀 프로그램을 실행할 수 있도록 하는 각 Q # 작업 및 함수에 대 한 .NET 클래스를 만듭니다.

예를 들어 [.net 상호 운용성 샘플](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) 에는 다음 Q # 작업 예제가 포함 됩니다.

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

퀀텀 시뮬레이터의 .NET에서이 작업을 호출 하려면 Q # 컴파일러에 의해 `Run` 생성 된 `RunAlgorithm` .net 클래스의 메서드를 사용할 수 있습니다.

### <a name="c"></a>[C#](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[F#](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="whats-next"></a>새로운 기능

이제 Q # 명령줄 프로그램 모두에 대 한 퀀텀 개발 키트를 설정 하 고 .NET과의 상호 운용성을 위해 [첫 번째 퀀텀 프로그램](xref:microsoft.quantum.write-program)을 작성 하 고 실행할 수 있습니다.
