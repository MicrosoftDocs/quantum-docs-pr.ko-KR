---
title: 양자 난수 생성기 만들기
description: 양자 난수 생성기를 만들어서 중첩 같은 기본적인 양자 개념을 보여주는 Q# 프로젝트를 빌드합니다.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: 5a433606f08f4c6a4ab7b5df67a7f0c30d2b3f0d
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/01/2020
ms.locfileid: "82683000"
---
# <a name="quickstart-implement-a-quantum-random-number-generator-in-q"></a>빠른 시작: Q\#에서 양자 난수 생성기 구현

Q#으로 양자 난수 생성기를 작성하는 간단한 양자 알고리즘 예제입니다. 이 알고리즘은 양자 메커니즘의 특성을 활용하여 난수를 생성합니다.

## <a name="prerequisites"></a>사전 요구 사항

- Microsoft [Quantum Development Kit](xref:microsoft.quantum.install)
- [Q# 프로젝트 만들기](xref:microsoft.quantum.howto.createproject)

## <a name="write-a-q-operation"></a>Q# 연산 작성

### <a name="q-operation-code"></a>Q# 연산 코드

1. Program.qs 파일의 내용을 다음 코드로 바꿉니다.

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-15,34":::

[양자 컴퓨팅이란?](xref:microsoft.quantum.overview.what) 문서에서 언급했듯이, 큐비트는 중첩에 있을 수 있는 양자 정보의 단위입니다. 측정된 큐비트는 0 또는 1 중 하나만 될 수 있습니다. 하지만 실행 중인 동안 큐비트 상태는 측정값이 0 또는 1일 수 있는 확률을 나타냅니다. 이 확률적 상태를 중첩이라고 합니다. 이 확률을 사용하여 난수를 생성할 수 있습니다.

Q# 연산에서는 Q#의 기본 형식인 `Qubit` 데이터 형식을 도입합니다. `Qubit`는 `using` 문으로만 할당할 수 있습니다. 할당되는 경우 큐비트는 항상 `Zero` 상태입니다. 

`H` 연산을 사용하여 `Qubit`를 중첩 상태로 전환할 수 있습니다. 큐비트를 측정하고 값을 읽으려면 `M` 내장 연산을 사용합니다.

`Qubit`를 중첩 상태로 전환하고 측정하면 코드가 호출될 때마다 다른 값이 반환됩니다.

`Qubit`를 할당 취소하면 큐비트가 명시적으로 다시 `Zero` 상태로 설정되어야 합니다. 그렇지 않으면 시뮬레이터가 런타임 오류를 보고합니다. 이렇게 하는 쉬운 방법은 `Reset`을 호출하는 것입니다.

### <a name="visualizing-the-code-with-the-bloch-sphere"></a>블로흐 구를 사용하여 코드 시각화

Bloch 구의 북극은 클래식 **0** 값을 나타내고, 남극은 클래식 **1** 값을 나타냅니다. 모든 중첩은 구의 점으로 표현할 수 있습니다(화살표로 표시). 화살표의 끝부분이 극에 가까울수록 측정 시 큐비트가 해당 극에 할당된 클래식 값으로 축소될 확률이 높아집니다. 예를 들어 아래쪽 빨간색 화살표로 표현되는 큐비트 상태는 측정될 경우 **0** 값을 제공할 확률이 높습니다.

<img src="~/media/qrng-Bloch.png" width="175" alt="A qubit state with a high probability of measuring zero">

이 표현을 사용하여 코드가 하는 일을 시각화할 수 있습니다.

* 먼저 **0** 상태에서 시작된 큐비트로 시작하고, `H`를 적용하여 **0**과 **1**의 확률이 동일한 중첩을 만듭니다.

<img src="~/media/qrng-H.png" width="450" alt="Preparing a qubit in superposition">

* 그런 다음, 큐비트를 측정하고 출력을 저장합니다.

<img src="~/media/qrng-meas.png" width="450" alt="Measuring a qubit and saving the output">

측정 결과는 완전히 임의적이므로 임의의 비트를 얻었습니다. 이 연산을 여러 번 호출하여 정수를 만들 수 있습니다. 예를 들어 이 연산을 세 번 호출하여 세 개의 임의 비트를 얻으면 임의의 3비트 숫자(즉, 0~7 사이의 임의 숫자)를 빌드할 수 있습니다.


## <a name="creating-a-complete-random-number-generator"></a>완전한 난수 생성기 만들기

이제 임의 비트를 생성하는 Q# 연산 기능이 있으므로 이를 사용하여 완전한 양자 난수 생성기를 빌드할 수 있습니다. Q# 명령줄 애플리케이션을 사용하거나 호스트 프로그램을 사용할 수 있습니다.



### <a name="q-command-line-applications-with-visual-studio-or-visual-studio-code"></a>[Visual Studio 또는 Visual Studio Code를 사용한 Q# 명령줄 애플리케이션](#tab/tabid-qsharp)

전체 Q# 명령줄 애플리케이션을 만들려면 다음 진입점을 Q# 프로그램에 추가합니다. 

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="17-33":::

실행 파일은 프로젝트 구성 및 명령줄 옵션에 따라 시뮬레이터 또는 리소스 예측 도구에서 `@EntryPoint()` 특성으로 표시된 작업 또는 함수를 실행합니다.

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-34":::

Visual Studio에서 Ctrl + F5 키를 눌러 스크립트를 실행하기만 하면 됩니다.

VS Code에서 터미널에 아래를 입력하여 Program.qs를 처음으로 빌드합니다.

```dotnetcli
dotnet build
```

후속 실행 시, 다시 빌드할 필요가 없습니다. 실행하려면 다음 명령을 입력하고 Enter 키를 누릅니다.

```dotnetcli
dotnet run --no-build
```

### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Visual Studio 코드 또는 명령줄을 사용하는 Python](#tab/tabid-python)

Python에서 새 Q# 프로그램을 실행하려면 다음 코드를 `host.py`로 저장합니다.

:::code language="python" source="~/quantum/samples/interoperability/qrng/host.py" range="11-30":::

그러면 명령줄에서 Python 호스트 프로그램을 실행할 수 있습니다.

```bash
$ python host.py
Preparing Q# environment...
..The random number generated is 42
```

### <a name="c-with-visual-studio-code-or-visual-studio"></a>[Visual Studio Code 또는 Visual Studio를 사용한 C#](#tab/tabid-csharp)

C#에서 새 Q# 프로그램을 실행하려면 다음 C# 코드를 포함하도록 `Driver.cs`를 수정합니다.

:::code language="csharp" source="~/quantum/samples/interoperability/qrng/Host.cs" range="4-39":::

그러면 명령줄에서 C# 호스트 프로그램을 실행할 수 있습니다(Visual Studio에서는 F5를 눌러야 함).

```bash
$ dotnet run
The random number generated is 42
```

***
