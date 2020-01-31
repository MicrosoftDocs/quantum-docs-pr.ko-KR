---
title: 'Q # + Python을 사용 하 여 개발'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 1e40c2dddeaf4fad41693c976493f10fffffa139
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76831004"
---
# <a name="develop-with-q--python"></a><span data-ttu-id="ea84c-102">Q # + Python을 사용 하 여 개발</span><span class="sxs-lookup"><span data-stu-id="ea84c-102">Develop with Q# + Python</span></span>

<span data-ttu-id="ea84c-103">Q # 작업을 호출 하는 Python 호스트 프로그램을 개발 하려면 QDK를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea84c-103">Install the QDK to develop Python host programs to call Q# operations.</span></span>

1. <span data-ttu-id="ea84c-104">필수 조건</span><span class="sxs-lookup"><span data-stu-id="ea84c-104">Pre-requisites</span></span>

    - <span data-ttu-id="ea84c-105">[Python](https://www.python.org/downloads/) 3.6 이상</span><span class="sxs-lookup"><span data-stu-id="ea84c-105">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="ea84c-106">[PIP](https://pip.pypa.io/en/stable/installing) Python 패키지 관리자</span><span class="sxs-lookup"><span data-stu-id="ea84c-106">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="ea84c-107">.NET Core SDK 3.1 이상</span><span class="sxs-lookup"><span data-stu-id="ea84c-107">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)


1. <span data-ttu-id="ea84c-108">Q #과 Python 간에 interop를 사용할 수 있도록 하는 Python 패키지인 `qsharp` 패키지를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea84c-108">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```bash
    pip install qsharp
    ```

1. <span data-ttu-id="ea84c-109">Q # 작업을 컴파일하고 실행 하기 위한 핵심 기능을 제공 하는 Jupyter 및 Python에서 사용 하는 커널로 `iqsharp`를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea84c-109">Install `iqsharp`, a kernel used by Jupyter and Python that provides the core functionality for compiling and executing Q# operations.</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```
  
1. <span data-ttu-id="ea84c-110">모든 IDE에서 Q #을 Python과 함께 사용할 수 있지만 Q # + Python 응용 프로그램에 Visual Studio Code (VS Code) IDE를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ea84c-110">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="ea84c-111">Visual Studio Code 및 QDK Visual Studio Code 확장을 사용 하 여 보다 다양 한 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea84c-111">By using Visual Studio Code and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

    - <span data-ttu-id="ea84c-112">[VS Code](https://code.visualstudio.com/download) (Windows, Linux 및 Mac) 설치</span><span class="sxs-lookup"><span data-stu-id="ea84c-112">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
    - <span data-ttu-id="ea84c-113">[VS Code 용 Qdk 확장](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea84c-113">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

1. <span data-ttu-id="ea84c-114">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ea84c-114">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="ea84c-115">`Operation.qs`라는 파일을 만들고 다음 코드를 추가하여 최소 Q# 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea84c-115">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
            }
        }
        ```

    - <span data-ttu-id="ea84c-116">`hello_world.py`이라는 Python 프로그램을 만들어 Q# `SayHello()` 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="ea84c-116">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="ea84c-117">다음과 같이 프로그램을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ea84c-117">Run the program:</span></span>

        ```bash
        python hello_world.py
        ```

    - <span data-ttu-id="ea84c-118">출력을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ea84c-118">Verify the output.</span></span> <span data-ttu-id="ea84c-119">프로그램은 다음 줄을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="ea84c-119">Your program should output the following lines:</span></span>

        ```bash
        Hello from quantum world!
       ```


> [!NOTE]
> * <span data-ttu-id="ea84c-120">Python Jupyter 노트북을 사용 하 여 기존 Python 프로그램을 작성 하 고 셀에서 Q # 작업을 호출할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea84c-120">You can also use Python Jupyter notebooks to write the classical Python program and call Q# operations from the cells.</span></span> <span data-ttu-id="ea84c-121">Python 코드는 일반적인 Python 프로그램 일 뿐입니다.</span><span class="sxs-lookup"><span data-stu-id="ea84c-121">The Python code is just a normal Python program.</span></span>

## <a name="whats-next"></a><span data-ttu-id="ea84c-122">다음은 무엇일까요?</span><span class="sxs-lookup"><span data-stu-id="ea84c-122">What's next?</span></span>

<span data-ttu-id="ea84c-123">지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.write-program)을 작성 및 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea84c-123">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
