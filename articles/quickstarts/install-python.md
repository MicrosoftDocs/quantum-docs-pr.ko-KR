---
title: Q# 및 Python을 사용하여 개발
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 6513acd5b9cdce15ce61ed2c0454f46e6a6d9bd0
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274081"
---
# <a name="develop-with-q-and-python"></a><span data-ttu-id="7b6f4-102">Q# 및 Python을 사용하여 개발</span><span class="sxs-lookup"><span data-stu-id="7b6f4-102">Develop with Q# and Python</span></span>

<span data-ttu-id="7b6f4-103">QDK를 설치하여 Q# 작업을 호출하는 Python 호스트 프로그램을 개발합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-103">Install the QDK to develop Python host programs to call Q# operations.</span></span>

1. <span data-ttu-id="7b6f4-104">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="7b6f4-104">Prerequisites</span></span>

    - <span data-ttu-id="7b6f4-105">[Python](https://www.python.org/downloads/) 3.6 이상</span><span class="sxs-lookup"><span data-stu-id="7b6f4-105">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="7b6f4-106">[PIP](https://pip.pypa.io/en/stable/installing) Python 패키지 관리자</span><span class="sxs-lookup"><span data-stu-id="7b6f4-106">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="7b6f4-107">.NET Core SDK 3.1</span><span class="sxs-lookup"><span data-stu-id="7b6f4-107">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="7b6f4-108">Q#과 Python 간에 interop를 사용할 수 있도록 하는 Python 패키지인 `qsharp` 패키지를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-108">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```
    pip install qsharp
    ```

1. <span data-ttu-id="7b6f4-109">IQ#을 설치합니다. IQ#은 Jupyter 및 Python에서 주로 사용되는 커널이며, Q# 작업을 컴파일하고 실행하는 핵심 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-109">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and executing Q# operations.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="7b6f4-110">`dotnet iqsharp install` 단계 중에 오류가 발생하면 새 터미널 창을 열고 다시 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-110">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="7b6f4-111">그래도 해결되지 않으면 설치된 `dotnet-iqsharp` 도구(Windows의 경우 `dotnet-iqsharp.exe`)를 찾아서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-111">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="7b6f4-112">여기서 `/path/to/dotnet-iqsharp`은 파일 시스템에서 `dotnet-iqsharp` 도구의 절대 경로로 바꿔야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-112">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="7b6f4-113">일반적으로 사용자 프로필 폴더의 `.dotnet/tools`에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-113">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
  
1. <span data-ttu-id="7b6f4-114">모든 IDE에서 Python과 함께 Q#을 사용할 수 있지만, Q# + Python 애플리케이션용 VS Code(Visual Studio Code) IDE를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-114">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="7b6f4-115">Visual Studio Code와 QDK Visual Studio Code 확장을 사용하면 보다 다양한 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-115">By using Visual Studio Code and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

    - <span data-ttu-id="7b6f4-116">[VS Code](https://code.visualstudio.com/download)(Windows, Linux 및 Mac)를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-116">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
    - <span data-ttu-id="7b6f4-117">[VS Code용 QDK 확장](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-117">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

1. <span data-ttu-id="7b6f4-118">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-118">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="7b6f4-119">`Operation.qs`라는 파일을 만들고 다음 코드를 추가하여 최소 Q# 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-119">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
            }
        }
        ```

    - <span data-ttu-id="7b6f4-120">`hello_world.py`이라는 Python 프로그램을 만들어 Q# `SayHello()` 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-120">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="7b6f4-121">다음과 같이 프로그램을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-121">Run the program:</span></span>

        ```
        python hello_world.py
        ```

    - <span data-ttu-id="7b6f4-122">출력을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-122">Verify the output.</span></span> <span data-ttu-id="7b6f4-123">프로그램은 다음 줄을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-123">Your program should output the following lines:</span></span>

        ```
        Hello from quantum world!
        ```


> [!NOTE]
> * <span data-ttu-id="7b6f4-124">Python Jupyter Notebook을 사용하여 클래식 Python 프로그램을 작성하고 셀에서 Q# 작업을 호출할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-124">You can also use Python Jupyter notebooks to write the classical Python program and call Q# operations from the cells.</span></span> <span data-ttu-id="7b6f4-125">Python 코드는 일반적인 Python 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-125">The Python code is just a normal Python program.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7b6f4-126">다음 단계</span><span class="sxs-lookup"><span data-stu-id="7b6f4-126">Next steps</span></span>

<span data-ttu-id="7b6f4-127">지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성 및 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b6f4-127">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
