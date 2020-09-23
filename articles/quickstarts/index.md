---
title: Microsoft QDK(Quantum Development Kit) 설정
description: 다양한 환경에 Microsoft Quantum Development Kit를 설치하는 방법을 알아봅니다.
author: bradben
ms.author: v-benbra
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 74b9b3d8f694072f5b5f4d0eb520263387de8919
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834485"
---
# <a name="setting-up-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="0955d-103">Microsoft QDK(Quantum Development Kit) 설정</span><span class="sxs-lookup"><span data-stu-id="0955d-103">Setting up the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="0955d-104">퀀텀 프로그래밍을 시작할 수 있도록 사용자 환경에 맞게 Microsoft QDK(Quantum Development Kit)를 설정하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="0955d-104">Learn how to set up the Microsoft Quantum Development Kit (QDK) for your environment, so that you can get started with quantum programming.</span></span> <span data-ttu-id="0955d-105">QDK은 다음으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="0955d-105">The QDK consists of:</span></span>

- <span data-ttu-id="0955d-106">Q# 프로그래밍 언어</span><span class="sxs-lookup"><span data-stu-id="0955d-106">The Q# programming language</span></span>
- <span data-ttu-id="0955d-107">Q#의 복합 기능을 추상화하는 라이브러리 세트</span><span class="sxs-lookup"><span data-stu-id="0955d-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="0955d-108">Q#으로 작성된 퀀텀 프로그램을 실행하기 위한 Python 및 .NET 언어(C#, F# 및 VB.NET)용 API</span><span class="sxs-lookup"><span data-stu-id="0955d-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="0955d-109">개발을 용이하게 하는 도구</span><span class="sxs-lookup"><span data-stu-id="0955d-109">Tools to facilitate your development</span></span>

<span data-ttu-id="0955d-110">Q# 프로그램은 Visual Studio Code 또는 Visual Studio를 사용하거나 IQ# Jupyter 커널의 Jupyter Notebook을 통해 독립 실행형 애플리케이션으로 실행하거나 Python 또는 .NET 언어(C#, F#)로 작성된 호스트 프로그램과 쌍을 이뤄 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0955d-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, through Jupyter Notebooks with the IQ# Jupyter kernel, or paired with a host program written in Python or a .NET language (C#, F#).</span></span> <span data-ttu-id="0955d-111">[Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/) 또는 [Docker](#use-the-qdk-with-docker)를 사용하여 Q# 프로그램을 온라인으로 실행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0955d-111">You can also run Q# programs online using [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/), or [Docker](#use-the-qdk-with-docker).</span></span> 

## <a name="options-for-setting-up-the-qdk"></a><span data-ttu-id="0955d-112">QDK를 설정하는 옵션</span><span class="sxs-lookup"><span data-stu-id="0955d-112">Options for setting up the QDK</span></span>

<span data-ttu-id="0955d-113">QDK는 세 가지 방법으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0955d-113">You can use the QDK in three ways:</span></span>

- [<span data-ttu-id="0955d-114">QDK 로컬 설치</span><span class="sxs-lookup"><span data-stu-id="0955d-114">Install the QDK locally</span></span>](#install-the-qdk-locally)
- [<span data-ttu-id="0955d-115">QDK 온라인 사용</span><span class="sxs-lookup"><span data-stu-id="0955d-115">Use the QDK online</span></span>](#use-the-qdk-online)
- [<span data-ttu-id="0955d-116">QDK Docker 이미지 사용</span><span class="sxs-lookup"><span data-stu-id="0955d-116">Use a QDK Docker image</span></span>](#use-the-qdk-with-docker)

## <a name="install-the-qdk-locally"></a><span data-ttu-id="0955d-117">QDK 로컬 설치</span><span class="sxs-lookup"><span data-stu-id="0955d-117">Install the QDK locally</span></span>

<span data-ttu-id="0955d-118">대부분의 즐겨찾기 IDE에서 Q# 코드를 개발할 수 있을 뿐만 아니라 Q#를 Python 및 .NET(C#, F#)과 같은 다른 언어와 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0955d-118">You can develop Q# code in most of your favorites IDEs, as well as integrate Q# with other languages such as Python and .NET (C#, F#).</span></span>

|&nbsp; | <span data-ttu-id="0955d-119">**VS Code<br>(2019 이상)**</span><span class="sxs-lookup"><span data-stu-id="0955d-119">**VS Code<br>(2019 or later)**</span></span>| <span data-ttu-id="0955d-120">**Visual Studio<br>(2019 이상)**</span><span class="sxs-lookup"><span data-stu-id="0955d-120">**Visual Studio<br>(2019 or later)**</span></span> | <span data-ttu-id="0955d-121">**Jupyter Notebook**</span><span class="sxs-lookup"><span data-stu-id="0955d-121">**Jupyter Notebooks**</span></span> | <span data-ttu-id="0955d-122">**명령줄**</span><span class="sxs-lookup"><span data-stu-id="0955d-122">**Command line**</span></span>|
|:-----|:-----:|:-----:|:-----:|:-----:|
|<span data-ttu-id="0955d-123">**OS**</span><span class="sxs-lookup"><span data-stu-id="0955d-123">**OS**</span></span> |<span data-ttu-id="0955d-124">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="0955d-124">Windows, macOS, Linux</span></span> |<span data-ttu-id="0955d-125">Windows만</span><span class="sxs-lookup"><span data-stu-id="0955d-125">Windows only</span></span> |<span data-ttu-id="0955d-126">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="0955d-126">Windows, macOS, Linux</span></span> |<span data-ttu-id="0955d-127">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="0955d-127">Windows, macOS, Linux</span></span> |
|<br><span data-ttu-id="0955d-128">**Q# 독립 실행형**</span><span class="sxs-lookup"><span data-stu-id="0955d-128">**Q# standalone**</span></span> |<br>[<span data-ttu-id="0955d-129">설치</span><span class="sxs-lookup"><span data-stu-id="0955d-129">Install</span></span>](xref:microsoft.quantum.install.standalone) |<br> [<span data-ttu-id="0955d-130">설치</span><span class="sxs-lookup"><span data-stu-id="0955d-130">Install</span></span>](xref:microsoft.quantum.install.standalone)  |<br> [<span data-ttu-id="0955d-131">설치</span><span class="sxs-lookup"><span data-stu-id="0955d-131">Install</span></span>](xref:microsoft.quantum.install.jupyter) |<br>[<span data-ttu-id="0955d-132">설치</span><span class="sxs-lookup"><span data-stu-id="0955d-132">Install</span></span>](xref:microsoft.quantum.install.standalone)|
|<span data-ttu-id="0955d-133">**Q# 및 Python**</span><span class="sxs-lookup"><span data-stu-id="0955d-133">**Q#  and Python**</span></span> |[<span data-ttu-id="0955d-134">설치</span><span class="sxs-lookup"><span data-stu-id="0955d-134">Install</span></span>](xref:microsoft.quantum.install.python) |[<span data-ttu-id="0955d-135">설치</span><span class="sxs-lookup"><span data-stu-id="0955d-135">Install</span></span>](xref:microsoft.quantum.install.python) |[<span data-ttu-id="0955d-136">설치</span><span class="sxs-lookup"><span data-stu-id="0955d-136">Install</span></span>](xref:microsoft.quantum.install.jupyter) |[<span data-ttu-id="0955d-137">설치</span><span class="sxs-lookup"><span data-stu-id="0955d-137">Install</span></span>](xref:microsoft.quantum.install.python) |
|<span data-ttu-id="0955d-138">**Q# 및 .NET(C#, F#)**</span><span class="sxs-lookup"><span data-stu-id="0955d-138">**Q# and .NET (C#, F#)**</span></span>|[<span data-ttu-id="0955d-139">설치</span><span class="sxs-lookup"><span data-stu-id="0955d-139">Install</span></span>](xref:microsoft.quantum.install.cs) |[<span data-ttu-id="0955d-140">설치</span><span class="sxs-lookup"><span data-stu-id="0955d-140">Install</span></span>](xref:microsoft.quantum.install.cs)|<span data-ttu-id="0955d-141">&#10006;</span><span class="sxs-lookup"><span data-stu-id="0955d-141">&#10006;</span></span> |[<span data-ttu-id="0955d-142">설치</span><span class="sxs-lookup"><span data-stu-id="0955d-142">Install</span></span>](xref:microsoft.quantum.install.cs) |

## <a name="use-the-qdk-online"></a><span data-ttu-id="0955d-143">QDK 온라인 사용</span><span class="sxs-lookup"><span data-stu-id="0955d-143">Use the QDK Online</span></span>

<span data-ttu-id="0955d-144">다음과 같은 옵션으로 로컬에 아무 것도 설치하지 않고 Q# 코드를 개발할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0955d-144">You can also develop Q# code without installing anything locally with these options:</span></span>

|<span data-ttu-id="0955d-145">리소스</span><span class="sxs-lookup"><span data-stu-id="0955d-145">Resource</span></span>|<span data-ttu-id="0955d-146">장점</span><span class="sxs-lookup"><span data-stu-id="0955d-146">Advantages</span></span>|<span data-ttu-id="0955d-147">제한 사항</span><span class="sxs-lookup"><span data-stu-id="0955d-147">Limitations</span></span>|
|---|---|---|
|[<span data-ttu-id="0955d-148">**Visual Studio Codespaces**</span><span class="sxs-lookup"><span data-stu-id="0955d-148">**Visual Studio Codespaces**</span></span>](xref:microsoft.quantum.install.standalone)|<span data-ttu-id="0955d-149">풍부한 온라인 개발 환경</span><span class="sxs-lookup"><span data-stu-id="0955d-149">A rich online development environment</span></span>  |<span data-ttu-id="0955d-150">Azure 구독과 플랜 필요</span><span class="sxs-lookup"><span data-stu-id="0955d-150">Requires an Azure subscription and plan</span></span> |
|[<span data-ttu-id="0955d-151">**바인더**</span><span class="sxs-lookup"><span data-stu-id="0955d-151">**Binder**</span></span>](xref:microsoft.quantum.install.binder) | <span data-ttu-id="0955d-152">무료 온라인 Notebook 환경</span><span class="sxs-lookup"><span data-stu-id="0955d-152">Free online notebook experience</span></span> |<span data-ttu-id="0955d-153">지속성 없음</span><span class="sxs-lookup"><span data-stu-id="0955d-153">No persistence</span></span> |

## <a name="use-the-qdk-with-docker"></a><span data-ttu-id="0955d-154">Docker와 함께 QDK 사용</span><span class="sxs-lookup"><span data-stu-id="0955d-154">Use the QDK with Docker</span></span>

<span data-ttu-id="0955d-155">ACI와 같이 Docker 이미지를 지원하는 서비스를 통해 로컬 Docker 설치 또는 클라우드에서 QDK Docker 이미지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0955d-155">You can use our QDK Docker image in your local Docker installation or in the cloud via any service that supports Docker images, such as ACI.</span></span>

<span data-ttu-id="0955d-156">https://github.com/microsoft/iqsharp/#using-iq-as-a-container 에서 IQ# Docker 이미지를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0955d-156">You can download the IQ# Docker image from https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span></span> 

<span data-ttu-id="0955d-157">또한 Visual Studio Code 원격 개발 컨테이너와 함께 Docker를 사용하여 개발 환경을 빠르게 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0955d-157">You can also use Docker with a Visual Studio Code Remote Development Container to quickly define development environments.</span></span> <span data-ttu-id="0955d-158">VS Code 개발 컨테이너에 대한 자세한 내용은 https://github.com/microsoft/Quantum/tree/master/.devcontainer 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0955d-158">For more information about VS Code Development Containers, see https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0955d-159">다음 단계</span><span class="sxs-lookup"><span data-stu-id="0955d-159">Next steps</span></span>

<span data-ttu-id="0955d-160">이러한 각 설치 방법에 대한 워크플로는 [Q# 프로그램을 실행하는 방법](xref:microsoft.quantum.guide.host-programs)에서 설명하고 비교합니다.</span><span class="sxs-lookup"><span data-stu-id="0955d-160">The workflows for each of these setups are described and compared at [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>
