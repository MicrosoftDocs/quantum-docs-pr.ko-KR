---
title: 퀀텀 난수 생성기 만들기
description: Q#퀀텀 난수 생성기를 만들어 superposition와 같은 기본적인 퀀텀 개념을 보여 주는 프로젝트를 빌드합니다.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
no-loc:
- Q#
- $$v
ms.openlocfilehash: 8db892091794cb1166e41744572d8938d975abf2
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869769"
---
# <a name="tutorial-implement-a-quantum-random-number-generator-in-q"></a>자습서: Q\#에서 퀀텀 난수 생성기 구현

에서 작성 된 퀀텀 알고리즘의 간단한 예는 Q# 퀀텀 난수 생성기입니다. 이 알고리즘은 퀀텀 메커니즘의 특성을 활용하여 난수를 생성합니다.

## <a name="prerequisites"></a>필수 구성 요소

- Microsoft [Quantum Development Kit](xref:microsoft.quantum.install)
- Q# [ Q# 명령줄에서를 사용](xref:microsoft.quantum.install.standalone)하거나 [Python 호스트 프로그램](xref:microsoft.quantum.install.python) 또는 [c # 호스트 프로그램](xref:microsoft.quantum.install.cs)을 사용 하 여에 대 한 프로젝트를 만듭니다.

## <a name="write-a-no-locq-operation"></a>작업 쓰기 Q#

### <a name="no-locq-operation-code"></a>Q#작업 코드

1. Program.qs 파일의 내용을 다음 코드로 바꿉니다.

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-15,34":::

[퀀텀 컴퓨팅 이해](xref:microsoft.quantum.overview.understanding) 문서에서 설명한 대로 큐비트는 중첩될 수 있는 퀀텀 정보의 단위입니다. 측정된 큐비트는 0 또는 1 중 하나만 될 수 있습니다. 하지만 실행 중인 동안 큐비트 상태는 측정값이 0 또는 1일 수 있는 확률을 나타냅니다. 이 확률적 상태를 중첩이라고 합니다. 이 확률을 사용하여 난수를 생성할 수 있습니다.

이 Q# 작업에서는 `Qubit` 데이터 형식을 네이티브로 도입 합니다 Q# . `Qubit`는 `using` 문으로만 할당할 수 있습니다. 할당되는 경우 큐비트는 항상 `Zero` 상태입니다. 

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

이제 Q# 임의 비트를 생성 하는 작업이 있으므로 전체 퀀텀 난수 생성기를 작성 하는 데 사용할 수 있습니다. Q#명령줄 응용 프로그램을 사용 하거나 호스트 프로그램을 사용할 수 있습니다.



### <a name="no-locq-command-line-applications-with-visual-studio-or-visual-studio-code"></a>[Q#Visual Studio 또는 Visual Studio Code를 사용 하는 명령줄 응용 프로그램](#tab/tabid-qsharp)

전체 Q# 명령줄 응용 프로그램을 만들려면 프로그램에 다음 진입점을 추가 합니다 Q# . 

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

Python에서 새 프로그램을 실행 하려면 Q# 다음 코드를로 저장 합니다 `host.py` .

:::code language="python" source="~/quantum/samples/interoperability/qrng/host.py" range="11-30":::

그러면 명령줄에서 Python 호스트 프로그램을 실행할 수 있습니다.

```bash
$ python host.py
Preparing Q# environment...
..The random number generated is 42
```

### <a name="c-with-visual-studio-code-or-visual-studio"></a>[Visual Studio Code 또는 Visual Studio를 사용한 C#](#tab/tabid-csharp)

Q#C #에서 새 프로그램을 실행 하려면 `Driver.cs` 다음 c # 코드를 포함 하도록을 수정 합니다.

:::code language="csharp" source="~/quantum/samples/interoperability/qrng/Host.cs" range="4-39":::

그러면 명령줄에서 C# 호스트 프로그램을 실행할 수 있습니다(Visual Studio에서는 F5를 눌러야 함).

```bash
$ dotnet run
The random number generated is 42
```

***
