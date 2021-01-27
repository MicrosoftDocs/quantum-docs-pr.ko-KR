---
title: Microsoft QDK(Quantum Development Kit) 설정
description: 다양한 환경에 Microsoft Quantum Development Kit를 설치하는 방법을 알아봅니다.
author: bradben
ms.author: v-benbra
ms.date: 5/8/2020
ms.topic: quickstart
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 15067f1762f4468345beee38c98e1b943081fc1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859020"
---
# <a name="setting-up-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="c7af6-103">Microsoft QDK(Quantum Development Kit) 설정</span><span class="sxs-lookup"><span data-stu-id="c7af6-103">Setting up the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="c7af6-104">퀀텀 프로그래밍을 시작할 수 있도록 사용자 환경에 맞게 Microsoft QDK(Quantum Development Kit)를 설정하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="c7af6-104">Learn how to set up the Microsoft Quantum Development Kit (QDK) for your environment, so that you can get started with quantum programming.</span></span> <span data-ttu-id="c7af6-105">QDK은 다음으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7af6-105">The QDK consists of:</span></span>

- <span data-ttu-id="c7af6-106">Q# 프로그래밍 언어</span><span class="sxs-lookup"><span data-stu-id="c7af6-106">The Q# programming language</span></span>
- <span data-ttu-id="c7af6-107">Q#의 복합 기능을 추상화하는 라이브러리 세트</span><span class="sxs-lookup"><span data-stu-id="c7af6-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="c7af6-108">Q#으로 작성된 퀀텀 프로그램을 실행하기 위한 Python 및 .NET 언어(C#, F# 및 VB.NET)용 API</span><span class="sxs-lookup"><span data-stu-id="c7af6-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="c7af6-109">개발을 용이하게 하는 도구</span><span class="sxs-lookup"><span data-stu-id="c7af6-109">Tools to facilitate your development</span></span>

<span data-ttu-id="c7af6-110">Q# 프로그램은 Visual Studio Code 또는 Visual Studio를 사용하거나 IQ# Jupyter 커널의 Jupyter Notebook을 통해 독립 실행형 애플리케이션으로 실행하거나 Python 또는 .NET 언어(C#, F#)로 작성된 호스트 프로그램과 쌍을 이뤄 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7af6-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, through Jupyter Notebooks with the IQ# Jupyter kernel, or paired with a host program written in Python or a .NET language (C#, F#).</span></span> <span data-ttu-id="c7af6-111">[Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/) 또는 [Docker](#use-the-qdk-with-docker)를 사용하여 Q# 프로그램을 온라인으로 실행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7af6-111">You can also run Q# programs online using [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/), or [Docker](#use-the-qdk-with-docker).</span></span> 

## <a name="options-for-setting-up-the-qdk"></a><span data-ttu-id="c7af6-112">QDK를 설정하는 옵션</span><span class="sxs-lookup"><span data-stu-id="c7af6-112">Options for setting up the QDK</span></span>

<span data-ttu-id="c7af6-113">QDK는 세 가지 방법으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7af6-113">You can use the QDK in three ways:</span></span>

- [<span data-ttu-id="c7af6-114">QDK 로컬 설치</span><span class="sxs-lookup"><span data-stu-id="c7af6-114">Install the QDK locally</span></span>](#install-the-qdk-locally)
- [<span data-ttu-id="c7af6-115">QDK 온라인 사용</span><span class="sxs-lookup"><span data-stu-id="c7af6-115">Use the QDK online</span></span>](#use-the-qdk-online)
- [<span data-ttu-id="c7af6-116">QDK Docker 이미지 사용</span><span class="sxs-lookup"><span data-stu-id="c7af6-116">Use a QDK Docker image</span></span>](#use-the-qdk-with-docker)

## <a name="install-the-qdk-locally"></a><span data-ttu-id="c7af6-117">QDK 로컬 설치</span><span class="sxs-lookup"><span data-stu-id="c7af6-117">Install the QDK locally</span></span>

<span data-ttu-id="c7af6-118">대부분의 즐겨찾기 IDE에서 Q# 코드를 개발할 수 있을 뿐만 아니라 Q#를 Python 및 .NET(C#, F#)과 같은 다른 언어와 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7af6-118">You can develop Q# code in most of your favorites IDEs, as well as integrate Q# with other languages such as Python and .NET (C#, F#).</span></span>

<table>
    <tr>
        <th width=10%>&nbsp;</th>
        <th>&nbsp;</th>
        <th align="center" width=18%><img src="~/media/vs_code.png" alt="VS Code" width="50"/><br><span data-ttu-id="c7af6-119"><b>VS 코드</span><span class="sxs-lookup"><span data-stu-id="c7af6-119"><b>VS Code</span></span><br><span data-ttu-id="c7af6-120">(2019 이상)</b></span><span class="sxs-lookup"><span data-stu-id="c7af6-120">(2019 or later)</b></span></span></th>
        <th align="center" width=18%><img src="~/media/vs_studio.png" alt="Visual Studio" width="50"/><br><span data-ttu-id="c7af6-121"><b>Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c7af6-121"><b>Visual Studio</span></span><br><span data-ttu-id="c7af6-122">(2019 이상)</b></span><span class="sxs-lookup"><span data-stu-id="c7af6-122">(2019 or later)</b></span></span></th>
        <th align="center" width=18%><img src="~/media/jupyter-wht.png" alt="jupyter install" width="65"/><br><span data-ttu-id="c7af6-123"><b>Jupyter Notebook</b></span><span class="sxs-lookup"><span data-stu-id="c7af6-123"><b>Jupyter Notebooks</b></span></span></th>
        <th align="center" width=18%><img src="~/media/blank.png" alt="blank spacer" width="65"/><br><span data-ttu-id="c7af6-124"><b>명령줄</b></span><span class="sxs-lookup"><span data-stu-id="c7af6-124"><b>Command line</b></span></span></th>
    </tr>
    <tr>
        <th>&nbsp;</th>
        <td align="left"><span data-ttu-id="c7af6-125"><b>OS 지원:</b></span><span class="sxs-lookup"><span data-stu-id="c7af6-125"><b>OS support:</b></span></span></td>
        <td align="center"><span data-ttu-id="c7af6-126">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="c7af6-126">Windows, macOS, Linux</span></span></td>
        <td align="center"><span data-ttu-id="c7af6-127">Windows만</span><span class="sxs-lookup"><span data-stu-id="c7af6-127">Windows only</span></span></td>
        <td align="center"><span data-ttu-id="c7af6-128">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="c7af6-128">Windows, macOS, Linux</span></span></td>
        <td align="center"><span data-ttu-id="c7af6-129">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="c7af6-129">Windows, macOS, Linux</span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/quantum-wht.png" alt="QDK" width="60"/></td>
        <td align="left"><span data-ttu-id="c7af6-130"><b>Q# 독립 실행형</b></span><span class="sxs-lookup"><span data-stu-id="c7af6-130"><b>Q# standalone</b></span></span></td>
        <td align="center"><span data-ttu-id="c7af6-131"><a href="xref:microsoft.quantum.install.standalone">설치</a></span><span class="sxs-lookup"><span data-stu-id="c7af6-131"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="c7af6-132"><a href="xref:microsoft.quantum.install.standalone">설치</a></span><span class="sxs-lookup"><span data-stu-id="c7af6-132"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="c7af6-133"><a href="xref:microsoft.quantum.install.jupyter">설치</a></span><span class="sxs-lookup"><span data-stu-id="c7af6-133"><a href="xref:microsoft.quantum.install.jupyter">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="c7af6-134"><a href="xref:microsoft.quantum.install.standalone">설치</a></span><span class="sxs-lookup"><span data-stu-id="c7af6-134"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/python.png" alt="python install" width="50"/></td>
        <td align="left"><span data-ttu-id="c7af6-135"><b>Q# 및 Python</b></span><span class="sxs-lookup"><span data-stu-id="c7af6-135"><b>Q# and Python</b></span></span></td>
        <td align="center"><span data-ttu-id="c7af6-136"><a href="xref:microsoft.quantum.install.python">설치</a></span><span class="sxs-lookup"><span data-stu-id="c7af6-136"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="c7af6-137"><a href="xref:microsoft.quantum.install.python">설치</a></span><span class="sxs-lookup"><span data-stu-id="c7af6-137"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="c7af6-138"><a href="xref:microsoft.quantum.install.python">설치</a></span><span class="sxs-lookup"><span data-stu-id="c7af6-138"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="c7af6-139"><a href="xref:microsoft.quantum.install.python">설치</a></span><span class="sxs-lookup"><span data-stu-id="c7af6-139"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/dot_net.png" alt="dotnet install" width="50"/></td>
        <td align="left"><span data-ttu-id="c7af6-140"><b>Q# 및 .NET(C#, F#)</b></span><span class="sxs-lookup"><span data-stu-id="c7af6-140"><b>Q# and .NET (C#, F#)</b></span></span></td> 
        <td align="center"><span data-ttu-id="c7af6-141"><a href="xref:microsoft.quantum.install.cs">설치</a></span><span class="sxs-lookup"><span data-stu-id="c7af6-141"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="c7af6-142"><a href="xref:microsoft.quantum.install.cs">설치</a></span><span class="sxs-lookup"><span data-stu-id="c7af6-142"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="c7af6-143">&#10006;</span><span class="sxs-lookup"><span data-stu-id="c7af6-143">&#10006;</span></span></td>
        <td align="center"><span data-ttu-id="c7af6-144"><a href="xref:microsoft.quantum.install.cs">설치</a></span><span class="sxs-lookup"><span data-stu-id="c7af6-144"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
   </tr>
</table>

## <a name="use-the-qdk-online"></a><span data-ttu-id="c7af6-145">QDK 온라인 사용</span><span class="sxs-lookup"><span data-stu-id="c7af6-145">Use the QDK Online</span></span>

<span data-ttu-id="c7af6-146">다음과 같은 옵션으로 로컬에 아무 것도 설치하지 않고 Q# 코드를 개발할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7af6-146">You can also develop Q# code without installing anything locally with these options:</span></span>

|<span data-ttu-id="c7af6-147">리소스</span><span class="sxs-lookup"><span data-stu-id="c7af6-147">Resource</span></span>|<span data-ttu-id="c7af6-148">장점</span><span class="sxs-lookup"><span data-stu-id="c7af6-148">Advantages</span></span>|<span data-ttu-id="c7af6-149">제한 사항</span><span class="sxs-lookup"><span data-stu-id="c7af6-149">Limitations</span></span>|
|---|---|---|
|[<span data-ttu-id="c7af6-150">**Visual Studio Codespaces**</span><span class="sxs-lookup"><span data-stu-id="c7af6-150">**Visual Studio Codespaces**</span></span>](xref:microsoft.quantum.install.standalone)|<span data-ttu-id="c7af6-151">풍부한 온라인 개발 환경</span><span class="sxs-lookup"><span data-stu-id="c7af6-151">A rich online development environment</span></span>  |<span data-ttu-id="c7af6-152">Azure 구독과 플랜 필요</span><span class="sxs-lookup"><span data-stu-id="c7af6-152">Requires an Azure subscription and plan</span></span> |
|[<span data-ttu-id="c7af6-153">**바인더**</span><span class="sxs-lookup"><span data-stu-id="c7af6-153">**Binder**</span></span>](xref:microsoft.quantum.install.binder) | <span data-ttu-id="c7af6-154">무료 온라인 Notebook 환경</span><span class="sxs-lookup"><span data-stu-id="c7af6-154">Free online notebook experience</span></span> |<span data-ttu-id="c7af6-155">지속성 없음</span><span class="sxs-lookup"><span data-stu-id="c7af6-155">No persistence</span></span> |

## <a name="use-the-qdk-with-docker"></a><span data-ttu-id="c7af6-156">Docker와 함께 QDK 사용</span><span class="sxs-lookup"><span data-stu-id="c7af6-156">Use the QDK with Docker</span></span>

<span data-ttu-id="c7af6-157">ACI와 같이 Docker 이미지를 지원하는 서비스를 통해 로컬 Docker 설치 또는 클라우드에서 QDK Docker 이미지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7af6-157">You can use our QDK Docker image in your local Docker installation or in the cloud via any service that supports Docker images, such as ACI.</span></span>

<span data-ttu-id="c7af6-158"> https://github.com/microsoft/iqsharp/#using-iq-as-a-container 에서 IQ# Docker 이미지를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7af6-158">You can download the IQ# Docker image from https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span></span> 

<span data-ttu-id="c7af6-159">또한 Visual Studio Code 원격 개발 컨테이너와 함께 Docker를 사용하여 개발 환경을 빠르게 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7af6-159">You can also use Docker with a Visual Studio Code Remote Development Container to quickly define development environments.</span></span> <span data-ttu-id="c7af6-160">VS Code 개발 컨테이너에 대한 자세한 내용은 https://github.com/microsoft/Quantum/tree/master/.devcontainer 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c7af6-160">For more information about VS Code Development Containers, see https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c7af6-161">다음 단계</span><span class="sxs-lookup"><span data-stu-id="c7af6-161">Next steps</span></span>

<span data-ttu-id="c7af6-162">이러한 각 설치 방법에 대한 워크플로는 [Q# 프로그램을 실행하는 방법](xref:microsoft.quantum.guide.host-programs)에서 설명하고 비교합니다.</span><span class="sxs-lookup"><span data-stu-id="c7af6-162">The workflows for each of these setups are described and compared at [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>
