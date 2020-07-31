---
title: Q# 및 Python을 사용하여 개발
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 4d148435f01d975e690828dd02335758fc71dfe4
ms.sourcegitcommit: 2f4c637e194dc2b5d18539469ed37444e2800199
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/30/2020
ms.locfileid: "87436550"
---
# <a name="develop-with-q-and-python"></a>Q# 및 Python을 사용하여 개발

QDK를 설치하여 Q# 작업을 호출하는 Python 호스트 프로그램을 개발합니다.

## <a name="install-the-qsharp-python-package"></a>`qsharp` Python 패키지 설치

### <a name="install-using-conda-recommended"></a>[conda를 사용하여 설치(권장)](#tab/tabid-conda)

1. [Miniconda](https://docs.conda.io/en/latest/miniconda.html) 또는 [Anaconda](https://www.anaconda.com/products/individual#Downloads)를 설치합니다. **참고:** 64비트를 설치해야 합니다.

1. Anaconda 프롬프트를 엽니다.

   - 또는 PowerShell이나 pwsh를 사용하려면 셸을 열고 `conda init powershell`을 실행한 다음, 셸을 닫았다가 다시 엽니다.

1. 다음 명령을 실행하여 필요한 패키지(Jupyter Notebook 및 IQ# 포함)가 포함된 `qsharp-env`라는 새 conda 환경을 만들고 활성화합니다.

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. 동일한 터미널에서 `python -c "import qsharp"`을 실행하여 설치를 확인하고, 로컬 패키지 캐시를 필요한 QDK 구성 요소로 채웁니다.

### <a name="install-using-net-cli-and-pip-advanced"></a>[.NET CLI 및 pip를 사용하여 설치(고급)](#tab/tabid-dotnetcli)

1. 필수 조건:

    - [Python](https://www.python.org/downloads/) 3.6 이상
    - [PIP](https://pip.pypa.io/en/stable/installing) Python 패키지 관리자
    - [.NET Core SDK 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. Q#과 Python 간에 interop를 사용할 수 있도록 하는 Python 패키지인 `qsharp` 패키지를 설치합니다.

    ```
    pip install qsharp
    ```

1. IQ#을 설치합니다. IQ#은 Jupyter 및 Python에서 주로 사용되는 커널이며, Q# 작업을 컴파일하고 실행하는 핵심 기능을 제공합니다.

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > `dotnet iqsharp install` 단계 중에 오류가 발생하면 새 터미널 창을 열고 다시 시도합니다.
    > 그래도 해결되지 않으면 설치된 `dotnet-iqsharp` 도구(Windows의 경우 `dotnet-iqsharp.exe`)를 찾아서 실행합니다.
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > 여기서 `/path/to/dotnet-iqsharp`은 파일 시스템에서 `dotnet-iqsharp` 도구의 절대 경로로 바꿔야 합니다.
    > 일반적으로 사용자 프로필 폴더의 `.dotnet/tools`에 있습니다.
    
***

이것으로 끝입니다. 이제 Python에서 Q# 작업을 컴파일 및 실행하기 위한 핵심 기능을 제공하고 Q# Jupyter Notebook을 사용할 수 있게 해주는 `qsharp` Python 패키지와 Jupyter용 IQ# 커널이 모두 있습니다.

## <a name="choose-your-ide"></a>IDE 선택

모든 IDE에서 Python과 함께 Q#을 사용할 수 있지만, Q# + Python 애플리케이션용 VS Code(Visual Studio Code) IDE를 사용하는 것이 좋습니다. QDK Visual Studio Code 확장을 사용하여 경고, 구문 강조 표시, 프로젝트 템플릿 등과 같은 다양한 기능에 액세스할 수 있습니다.

VS Code를 사용하려면 다음을 수행합니다.

- [VS Code](https://code.visualstudio.com/download)(Windows, Linux 및 Mac)를 설치합니다.
- [VS Code용 QDK 확장](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)을 설치합니다.

그 외의 편집기는 위의 지침을 수행하면서 이미 설정이 완료되었습니다.

## <a name="write-your-first-q-program"></a>첫 번째 Q# 프로그램 작성

이제 간단한 Q# 프로그램을 작성하고 실행하여 `qsharp` Python 패키지 설치를 확인할 준비가 되었습니다.

1. `Operation.qs`라는 파일을 만들고 다음 코드를 추가하여 최소 Q# 작업을 만듭니다.

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="3-14":::

1. 다음과 같이 `Operation.qs`와 동일한 폴더에 `host.py`라는 Python 프로그램을 만들어 Q# `SampleQuantumRandomNumberGenerator()` 작업을 시뮬레이션합니다.

    ```python
    import qsharp
    from Qrng import SampleQuantumRandomNumberGenerator

    print(SampleQuantumRandomNumberGenerator.simulate())
    ```

1. 설치하는 동안 만든 환경(즉, `qsharp`을 설치한 conda 또는 Python 환경)에서 다음과 같이 프로그램을 실행합니다.

    ```
    python host.py
    ```

1. 호출한 작업의 결과가 표시됩니다. 이 예에서는 작업에서 임의의 결과를 생성하기 때문에 화면에 `0` 또는 `1`이 출력됩니다. 프로그램을 반복해서 실행하면 각 결과가 약 절반의 시간 동안 표시됩니다.

> [!NOTE]
> * Python 코드는 일반적인 Python 프로그램입니다. Python 기반 Jupyter Notebook을 비롯한 Python 환경을 사용하여 Python 프로그램을 작성하고 Q# 작업을 호출할 수 있습니다. Python 프로그램은 Python 코드 자체와 동일한 폴더에 있는 모든 .qs 파일에서 Q# 작업을 가져올 수 있습니다.

## <a name="next-steps"></a>다음 단계

기본 설정 환경에 Quantum Development Kit를 설치했으므로, 이제 이 자습서를 따라 [첫 번째 퀀텀 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성하여 실행할 수 있습니다.
