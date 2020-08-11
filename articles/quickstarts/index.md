---
title: Microsoft QDK(Quantum Development Kit) 설치
description: 다양한 환경에 Microsoft Quantum Development Kit를 설치하는 방법입니다.
author: bradben
ms.author: bradben
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 378970dc911ea5a794590f8336ffc6d3f9673285
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867576"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="f3cdf-103">Microsoft QDK(Quantum Development Kit) 설치</span><span class="sxs-lookup"><span data-stu-id="f3cdf-103">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="f3cdf-104">양자 프로그래밍을 시작할 수 있도록 Microsoft QDK(Quantum Development Kit)를 설치하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="f3cdf-104">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="f3cdf-105">QDK은 다음으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3cdf-105">The QDK consists of:</span></span>

- <span data-ttu-id="f3cdf-106">Q# 프로그래밍 언어</span><span class="sxs-lookup"><span data-stu-id="f3cdf-106">The Q# programming language</span></span>
- <span data-ttu-id="f3cdf-107">Q#의 복합 기능을 추상화하는 라이브러리 세트</span><span class="sxs-lookup"><span data-stu-id="f3cdf-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="f3cdf-108">Q#으로 작성된 퀀텀 프로그램을 실행하기 위한 Python 및 .NET 언어(C#, F# 및 VB.NET)용 API</span><span class="sxs-lookup"><span data-stu-id="f3cdf-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="f3cdf-109">개발을 용이하게 하는 도구</span><span class="sxs-lookup"><span data-stu-id="f3cdf-109">Tools to facilitate your development</span></span>

<span data-ttu-id="f3cdf-110">Q# 프로그램은 Visual Studio Code 또는 Visual Studio를 사용하거나 IQ# Jupyter 커널의 Jupyter Notebook을 통해 독립 실행형 애플리케이션으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3cdf-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, or through Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>
<span data-ttu-id="f3cdf-111">또한 .NET 언어(대개 C#) 또는 Python으로 작성된 호스트 프로그램과 쌍을 이룰 수 있으므로 기존 프로그램 내부에서 양자 연산을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3cdf-111">They can also be paired with a host program written in a .NET language (typically C#) or Python, enabling you to call quantum operations from inside a classical program.</span></span>

<span data-ttu-id="f3cdf-112">이러한 각 설치 방법에 대한 워크플로는 [Q# 프로그램을 실행하는 방법](xref:microsoft.quantum.guide.host-programs)에서 설명하고 비교합니다.</span><span class="sxs-lookup"><span data-stu-id="f3cdf-112">The workflows for each of these setups are described and compared at [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

<span data-ttu-id="f3cdf-113">QDK 설치를 진행하고 Q# 프로젝트를 만들려면 원하는 설치 방법을 선택하세요.</span><span class="sxs-lookup"><span data-stu-id="f3cdf-113">To proceed with installing the QDK and creating Q# projects, select your preferred setup:</span></span>

<span data-ttu-id="f3cdf-114">[Q# 명령줄 애플리케이션으로 개발](xref:microsoft.quantum.install.standalone) - 명령줄에서 Q#으로 작업하려면 이 방법을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f3cdf-114">[Develop with Q# command line applications](xref:microsoft.quantum.install.standalone) - Choose this approach to work with Q# from the command line.</span></span> <span data-ttu-id="f3cdf-115">아래 옵션과 같이 드라이버나 호스트 프로그램이 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3cdf-115">This does not require a driver or a host program like the below options.</span></span>

<span data-ttu-id="f3cdf-116">[Q# Jupyter Notebook으로 개발](xref:microsoft.quantum.install.jupyter) - 포함된 텍스트를 사용하여 셀에서 Q# 코드를 실행하거나 양자 컴퓨팅 대화형 자습서를 만들려면 이 환경을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f3cdf-116">[Develop with Q# Jupyter Notebooks](xref:microsoft.quantum.install.jupyter) - Select this environment to run Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> 

<span data-ttu-id="f3cdf-117">[Q# 및 Python으로 개발](xref:microsoft.quantum.install.python) - Python과 Q#을 결합하여 Q# 연산을 호출하는 Python 호스트 프로그램을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3cdf-117">[Develop with Q# and Python](xref:microsoft.quantum.install.python) - Enables you to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>

<span data-ttu-id="f3cdf-118">[Q# 및 .NET으로 개발](xref:microsoft.quantum.install.cs) - C#, F# 또는 VB.NET을 Q#과 결합하여 Q# 연산을 호출하는 .NET 호스트 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f3cdf-118">[Develop with Q# and .NET](xref:microsoft.quantum.install.cs) - Combine C#, F#, or VB.NET with Q# to create a .NET host program that calls Q# operations.</span></span>
