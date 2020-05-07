---
title: Microsoft QDK(Quantum Development Kit) 설치 방법 알아보기
description: C#용 Microsoft Quantum Development Kit, Python 및 Jupyter Notebook 환경을 설치하는 방법을 알아봅니다.
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: bca700660094b91f1c0dfa03f9bce1336073ca51
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/01/2020
ms.locfileid: "82680187"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="9a90f-103">Microsoft QDK(Quantum Development Kit) 설치</span><span class="sxs-lookup"><span data-stu-id="9a90f-103">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="9a90f-104">양자 프로그래밍을 시작할 수 있도록 Microsoft QDK(Quantum Development Kit)를 설치하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="9a90f-104">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="9a90f-105">QDK은 다음으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a90f-105">The QDK consists of:</span></span>

- <span data-ttu-id="9a90f-106">Go 프로그래밍 언어</span><span class="sxs-lookup"><span data-stu-id="9a90f-106">the Q# programming language</span></span>
- <span data-ttu-id="9a90f-107">Q#의 복합 기능을 추상화하는 라이브러리 세트</span><span class="sxs-lookup"><span data-stu-id="9a90f-107">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="9a90f-108">Q#으로 작성된 양자 프로그램을 실행하기 위한 Python 및 .NET 언어(C#, F# 및 VB.NET)용 API</span><span class="sxs-lookup"><span data-stu-id="9a90f-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="9a90f-109">개발을 용이하게 하는 도구</span><span class="sxs-lookup"><span data-stu-id="9a90f-109">tools to facilitate your development</span></span>

<span data-ttu-id="9a90f-110">Q# 프로그램은 종종 .NET 언어(일반적으로 C#) 또는 Python으로 작성된 호스트 프로그램과 쌍을 이룹니다.</span><span class="sxs-lookup"><span data-stu-id="9a90f-110">Q# programs are often paired with a host program written in a .NET language (typically C#) or Python.</span></span> <span data-ttu-id="9a90f-111">이를 통해 클래식 프로그램 내에서 양자 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a90f-111">This allows us to call quantum operations from inside a classical program.</span></span>
<span data-ttu-id="9a90f-112">또한 QDK는 IQ# Jupyter 커널을 통해 Jupyter Notebook에 Q#을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9a90f-112">In addition, the QDK provides Q# support for Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>

<span data-ttu-id="9a90f-113">QDK는 여러 개발 환경에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a90f-113">The QDK is available for multiple development environments.</span></span> <span data-ttu-id="9a90f-114">아래 섹션에서 원하는 설정을 선택하세요.</span><span class="sxs-lookup"><span data-stu-id="9a90f-114">Select your preferred setup from the sections below:</span></span>

- <span data-ttu-id="9a90f-115">[Q# 명령줄 애플리케이션:](xref:microsoft.quantum.install.standalone) 명령줄에서 Q#을 사용하려면 이 방식을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a90f-115">[Q# command line application:](xref:microsoft.quantum.install.standalone) choose this approach if you want to work with Q# from the command line.</span></span> <span data-ttu-id="9a90f-116">아래 옵션과 같이 드라이버나 호스트 프로그램이 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a90f-116">This does not require a driver or a host program like the below options.</span></span>
- <span data-ttu-id="9a90f-117">[Jupyter Notebook용 Q# 설치:](xref:microsoft.quantum.install.jupyter) 포함된 텍스트를 사용하여 셀에서 Q# 코드를 실행하거나 양자 컴퓨팅 대화형 자습서를 만들려면 이 환경을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a90f-117">[Install Q# for Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) choose this environment to execute Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> 
- <span data-ttu-id="9a90f-118">[Q# 및 Python으로 개발:](xref:microsoft.quantum.install.python) Python과 Q#을 결합하여 Q# 연산을 호출하는 Python 호스트 프로그램을 만들려면 이 방식을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a90f-118">[Develop with Q# and Python:](xref:microsoft.quantum.install.python) if you want to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>
- <span data-ttu-id="9a90f-119">[Q#과 C# 또는 F#으로 개발:](xref:microsoft.quantum.install.cs) C# 또는 F#과 Q#을 결합하여 Q# 연산을 호출하는 .NET 호스트 프로그램을 만들려면 이 방식을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a90f-119">[Develop with Q# and C# or F#:](xref:microsoft.quantum.install.cs) if you want to combine C# or F# and Q# to create a .NET host program that calls Q# operations.</span></span>
