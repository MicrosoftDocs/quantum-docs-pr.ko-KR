---
title: 'Q # Jupyter 노트북을 사용 하 여 개발'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: b7276f9b273f601f30e4938018398353b6a9102d
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76831072"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="3a88d-102">Q # Jupyter 노트북을 사용 하 여 개발</span><span class="sxs-lookup"><span data-stu-id="3a88d-102">Develop with Q# Jupyter notebooks</span></span>

<span data-ttu-id="3a88d-103">Q # Jupyter 노트북에서 Q # 작업을 개발 하는 데 QDK를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="3a88d-104">Jupyter 노트북은 지침, 메모 및 기타 콘텐츠와 함께 전체 코드 실행을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="3a88d-105">이 환경은 포함 된 설명 또는 퀀텀 컴퓨팅 대화형 자습서를 통해 Q # 코드를 작성 하는 데 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="3a88d-106">사용자 고유의 Q# Notebook 만들기를 시작하려면 다음 작업을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="3a88d-107">IQ#(i-q-sharp로 발음)은 Jupyter 및 Python에서 .NET Core SDK에 주로 사용되며, Q# 작업을 컴파일하고 시뮬레이션하는 핵심 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="3a88d-108">Q # Jupyter 노트북에서 Q # 코드만 실행할 수 있으며 작업은 외부 호스트 프로그램 (예: Python 또는 C# 파일)에서 호출할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="3a88d-109">외부 클래식 호스트 프로그램과 퀀텀 프로그램을 결합 하는 것이 목표 인 경우에는이 환경이 적절 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="3a88d-110">필수 조건</span><span class="sxs-lookup"><span data-stu-id="3a88d-110">Pre-requisites</span></span>

    - <span data-ttu-id="3a88d-111">[Python](https://www.python.org/downloads/) 3.6 이상</span><span class="sxs-lookup"><span data-stu-id="3a88d-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="3a88d-112">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="3a88d-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="3a88d-113">.NET Core SDK 3.1 이상</span><span class="sxs-lookup"><span data-stu-id="3a88d-113">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="3a88d-114">`iqsharp` 패키지를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-114">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="3a88d-115">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-115">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="3a88d-116">다음 명령을 실행하여 Notebook 서버를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-116">Run the following command to start the notebook server:</span></span>

        ```bash
        jupyter notebook
        ```

    - <span data-ttu-id="3a88d-117">Jupyter 노트 복사를 열려면 명령줄에서 제공 된 URL을 브라우저에 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-117">To open the Jupyter notebook copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="3a88d-118">Q# 커널을 사용하여 Jupyter Notebook을 만들고 첫 번째 Notebook 셀에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-118">Create a Jupyter notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="3a88d-119">다음 Notebook 셀을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-119">Run this cell of the notebook:</span></span>

        ![Q# 코드를 사용하는 Jupyter Notebook 셀](~/media/install-guide-jupyter.png)

        <span data-ttu-id="3a88d-121">셀의 출력에 `SayHello`가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-121">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="3a88d-122">Jupyter Notebook에서 실행하는 경우 Q# 코드가 컴파일되고 Notebook은 검색된 작업의 이름을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-122">When running in jupyter notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="3a88d-123">새 셀에서 `%simulate` 명령을 사용 하 여 시뮬레이터에서 방금 만든 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-123">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![%simulate 매직을 사용하는 Jupyter Notebook 셀](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="3a88d-125">호출 된 작업의 결과와 함께 화면에 메시지가 출력 되는 것을 볼 수 있습니다 (작업에서 단순히 `Unit` 형식을 반환 하기 때문에 빈 튜플 `()` 표시 됨).</span><span class="sxs-lookup"><span data-stu-id="3a88d-125">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="whats-next"></a><span data-ttu-id="3a88d-126">다음은 무엇일까요?</span><span class="sxs-lookup"><span data-stu-id="3a88d-126">What's next?</span></span>

<span data-ttu-id="3a88d-127">지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.write-program)을 작성 및 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a88d-127">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
