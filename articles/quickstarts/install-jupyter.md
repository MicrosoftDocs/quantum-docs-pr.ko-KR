---
title: Q# Jupyter Notebook을 사용하여 개발
description: Jupyter Notebook을 사용하여 Q# 애플리케이션을 만드는 방법을 알아봅니다.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
no-loc:
- Q#
- $$v
ms.openlocfilehash: b34d89ab33a4644c1dd4342949685f9bf84babd8
ms.sourcegitcommit: d98190988ff03146d9ca2b0d325870cd717d729a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/06/2020
ms.locfileid: "91771403"
---
# <a name="develop-with-no-locq-jupyter-notebooks"></a>Q# Jupyter Notebook을 사용하여 개발

Q# Jupyter Notebook에서 Q# 작업을 개발하기 위해 QDK를 설치합니다.

Jupyter Notebook을 사용하면 지침, 메모 및 기타 콘텐츠와 함께 내부 코드를 실행할 수 있습니다. 이 환경은 설명 또는 퀀텀 컴퓨팅 대화형 자습서가 포함된 Q# 코드를 작성하는 데 적합합니다. 사용자 고유의 Q# Notebook 만들기를 시작하려면 다음 작업을 수행해야 합니다.

## <a name="install-the-ino-locq-jupyter-kernel"></a>IQ# Jupyter 커널 설치

IQ#(i-q-sharp로 발음)는 Jupyter 및 Python에서 .NET Core SDK에 주로 사용되며, Q# 작업을 컴파일하고 시뮬레이션하는 핵심 기능을 제공합니다.

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

### <a name="install-using-net-cli-advanced"></a>[.NET CLI를 사용하여 설치(고급)](#tab/tabid-dotnetcli)

1. 필수 조건:

    - [Python](https://www.python.org/downloads/) 3.6 이상
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [.NET Core SDK 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. `Microsoft.Quantum.IQSharp` 패키지를 설치합니다.

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

이것으로 끝입니다. 이제 Q# Jupyter Notebook에서 Q# 작업을 컴파일 및 실행하기 위한 핵심 기능을 제공하는 Jupyter용 IQ# 커널이 있습니다.

## <a name="create-your-first-no-locq-notebook"></a>첫 번째 Q# Notebook 만들기

이제 간단한 Q# 작업을 작성하고 실행하여 Q# Jupyter Notebook 설치를 확인할 준비가 되었습니다.

1. 설치하는 동안 만든 환경(즉, 직접 만든 conda 환경 또는 Jupyter를 설치한 Python 환경)에서 다음 명령을 실행하여 Jupyter Notebook 서버를 시작합니다.

    ```
    jupyter notebook
    ```

    - 사용하는 브라우저에서 Jupyter Notebook이 자동으로 열리지 않으면 명령줄에 제공된 URL을 복사하여 브라우저에 붙여넣습니다.

1. **새로 만들기 → Q#** 을 선택하여 Q# 커널로 Jupyter Notebook을 만들고, 첫 번째 Notebook 셀에 다음 코드를 추가합니다.

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="6-13":::

1. 다음 Notebook 셀을 실행합니다.

    ![Q# 코드가 포함된 Jupyter Notebook 셀](~/media/install-guide-jupyter.png)

    셀의 출력에 `SampleQuantumRandomNumberGenerator`가 표시됩니다. Jupyter Notebook에서 실행하는 경우 Q# 코드가 컴파일되고, 셀은 검색한 모든 작업의 이름을 출력합니다.

1. 새 셀에서 `%simulate` 명령을 사용하여 방금 만든(시뮬레이터에서) 작업을 실행합니다.

    ![%simulate 매직이 포함된 Jupyter Notebook 셀](~/media/install-guide-jupyter-simulate.png)

    호출한 작업의 결과가 표시됩니다. 이 예에서는 작업에서 임의의 결과를 생성하기 때문에 화면에 `Zero` 또는 `One`이 출력됩니다. 셀을 반복해서 실행하면 각 결과가 약 절반의 시간 동안 표시됩니다.

## <a name="next-steps"></a>다음 단계

Q# Jupyter Notebook용 QDK를 설치했으므로, Jupyter Notebook 환경 내에서 직접 Q# 코드를 작성하여 [첫 번째 퀀텀 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성하고 실행할 수 있습니다.

Q# Jupyter Notebook으로 수행할 수 있는 작업에 대한 자세한 내용은 다음을 참조하세요.

- [Q# 및 Jupyter Notebook 소개](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/). Jupyter 환경에서 Q#을 사용하는 방법을 자세히 설명하는 Q# Jupyter Notebook을 찾을 수 있습니다.
- [Quantum Katas](xref:microsoft.quantum.overview.katas)는 Q# Jupyter Notebook 형태의 자기 주도적 자습서 및 프로그래밍 연습 세트를 포함하는 오픈 소스 컬렉션입니다. [Quantum Katas 자습서 Notebook](https://github.com/microsoft/QuantumKatas#tutorial-topics)은 좋은 시작점입니다. Quantum Katas의 목표는 퀀텀 컴퓨팅과 Q# 프로그래밍 요소를 동시에 학습하는 것입니다. Q# Jupyter Notebook으로 만들 수 있는 콘텐츠의 종류를 보여주는 유용한 예입니다.
