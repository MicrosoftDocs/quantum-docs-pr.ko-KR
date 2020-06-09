---
title: 'Q # 및 Python을 사용 하 여 개발'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: f18d005012dc1c52aab456f1c7b194d182cab786
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84578167"
---
# <a name="develop-with-q-and-python"></a><span data-ttu-id="ace1f-102">Q # 및 Python을 사용 하 여 개발</span><span class="sxs-lookup"><span data-stu-id="ace1f-102">Develop with Q# and Python</span></span>

<span data-ttu-id="ace1f-103">Q # 작업을 호출 하는 Python 호스트 프로그램을 개발 하려면 QDK를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ace1f-103">Install the QDK to develop Python host programs to call Q# operations.</span></span>

1. <span data-ttu-id="ace1f-104">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="ace1f-104">Pre-requisites</span></span>

    - <span data-ttu-id="ace1f-105">[Python](https://www.python.org/downloads/) 3.6 이상</span><span class="sxs-lookup"><span data-stu-id="ace1f-105">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="ace1f-106">[PIP](https://pip.pypa.io/en/stable/installing) Python 패키지 관리자</span><span class="sxs-lookup"><span data-stu-id="ace1f-106">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="ace1f-107">.NET Core SDK 3.1</span><span class="sxs-lookup"><span data-stu-id="ace1f-107">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="ace1f-108">`qsharp`Q #과 python 간에 interop를 사용할 수 있도록 하는 Python 패키지인 패키지를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ace1f-108">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```
    pip install qsharp
    ```

1. <span data-ttu-id="ace1f-109">Q # 작업을 컴파일하고 실행 하기 위한 핵심 기능을 제공 하는 Jupyter 및 Python에서 사용 하는 커널 인 IQ #을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ace1f-109">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and executing Q# operations.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```
  
1. <span data-ttu-id="ace1f-110">모든 IDE에서 Q #을 Python과 함께 사용할 수 있지만 Q # + Python 응용 프로그램에 Visual Studio Code (VS Code) IDE를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ace1f-110">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="ace1f-111">Visual Studio Code 및 QDK Visual Studio Code 확장을 사용 하 여 보다 다양 한 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ace1f-111">By using Visual Studio Code and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

    - <span data-ttu-id="ace1f-112">[VS Code](https://code.visualstudio.com/download) (Windows, Linux 및 Mac) 설치</span><span class="sxs-lookup"><span data-stu-id="ace1f-112">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
    - <span data-ttu-id="ace1f-113">[VS Code 용 Qdk 확장](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ace1f-113">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

1. <span data-ttu-id="ace1f-114">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ace1f-114">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="ace1f-115">`Operation.qs`라는 파일을 만들고 다음 코드를 추가하여 최소 Q# 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ace1f-115">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
            }
        }
        ```

    - <span data-ttu-id="ace1f-116">`hello_world.py`이라는 Python 프로그램을 만들어 Q# `SayHello()` 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="ace1f-116">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="ace1f-117">다음과 같이 프로그램을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ace1f-117">Run the program:</span></span>

        ```
        python hello_world.py
        ```

    - <span data-ttu-id="ace1f-118">출력을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ace1f-118">Verify the output.</span></span> <span data-ttu-id="ace1f-119">프로그램은 다음 줄을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="ace1f-119">Your program should output the following lines:</span></span>

        ```
        Hello from quantum world!
        ```


> [!NOTE]
> * <span data-ttu-id="ace1f-120">Python Jupyter 노트북을 사용 하 여 기존 Python 프로그램을 작성 하 고 셀에서 Q # 작업을 호출할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ace1f-120">You can also use Python Jupyter notebooks to write the classical Python program and call Q# operations from the cells.</span></span> <span data-ttu-id="ace1f-121">Python 코드는 일반적인 Python 프로그램 일 뿐입니다.</span><span class="sxs-lookup"><span data-stu-id="ace1f-121">The Python code is just a normal Python program.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ace1f-122">다음 단계</span><span class="sxs-lookup"><span data-stu-id="ace1f-122">Next steps</span></span>

<span data-ttu-id="ace1f-123">지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성 및 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ace1f-123">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
