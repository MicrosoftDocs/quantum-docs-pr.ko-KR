---
title: Quantum Development Kit 릴리스 정보
description: Microsoft Quantum Development Kit 미리보기의 최신 업데이트에 대해 알아보세요.
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
uid: microsoft.quantum.relnotes
ms.openlocfilehash: 0fcdec1a304730b593224283421539ea3ca9c913
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415458"
---
# <a name="microsoft-quantum-development-kit-release-notes"></a><span data-ttu-id="e8eef-103">Microsoft Quantum Development Kit 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="e8eef-103">Microsoft Quantum Development Kit Release Notes</span></span>

<span data-ttu-id="e8eef-104">이 문서에는 각 Quantum Development Kit 릴리스에 대한 정보가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-104">This article contains information on each Quantum Development Kit release.</span></span>

<span data-ttu-id="e8eef-105">설치 지침은[설치 가이드](xref:microsoft.quantum.install)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-105">For installation instructions, please refer to the [install guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="e8eef-106">업데이트 지침은 [업데이트 가이드](xref:microsoft.quantum.update)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-106">For update instructions, please refer to the [update guide](xref:microsoft.quantum.update).</span></span>

## <a name="version-0112006403"></a><span data-ttu-id="e8eef-107">버전 0.11.2006.403</span><span class="sxs-lookup"><span data-stu-id="e8eef-107">Version 0.11.2006.403</span></span>

<span data-ttu-id="e8eef-108">*릴리스 날짜: 2020년 6월 4일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-108">*Release date: June 4th, 2020*</span></span>

<span data-ttu-id="e8eef-109">이 릴리스는 Q# 프로젝트의 컴파일에 영향을 주는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-109">This release fixes a bug affecting compilation of Q# projects.</span></span>

## <a name="version-0112006207"></a><span data-ttu-id="e8eef-110">버전 0.11.2006.207</span><span class="sxs-lookup"><span data-stu-id="e8eef-110">Version 0.11.2006.207</span></span>

<span data-ttu-id="e8eef-111">*릴리스 날짜: 2020년 6월 3일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-111">*Release date: June 3rd, 2020*</span></span>

<span data-ttu-id="e8eef-112">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-112">This release contains the following:</span></span>

- <span data-ttu-id="e8eef-113">Q# 진입점이 있으면 Q# Notebook 및 Python 호스트 프로그램이 더 이상 실패하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-113">Q# notebooks and Python host programs will no longer fail when a Q# entry point is present</span></span>
- <span data-ttu-id="e8eef-114">액세스 한정자를 사용하도록 [표준 라이브러리](xref:microsoft.quantum.libraries.standard.intro)로 업데이트</span><span class="sxs-lookup"><span data-stu-id="e8eef-114">Updates to [Standard library](xref:microsoft.quantum.libraries.standard.intro) to use access modifiers</span></span>
- <span data-ttu-id="e8eef-115">컴파일러는 기본 제공 재작성 단계 사이에 재작성 단계의 플러그 인을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-115">Compiler now allows plug-in of rewrite steps between built-in rewrite steps</span></span>
- <span data-ttu-id="e8eef-116">[API 원칙](xref:microsoft.quantum.contributing.api-design)에 설명된 일정에 따라 몇 가지 사용되지 않는 함수 및 작업이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-116">Several deprecated functions and operations have been removed following the schedule described in our [API principles](xref:microsoft.quantum.contributing.api-design).</span></span> <span data-ttu-id="e8eef-117">버전 0.11.2004.2825에서 경고 없이 빌드된 Q# 프로그램 및 라이브러리는 계속 수정되지 않은 상태로 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-117">Q# programs and libraries that build without warnings in version 0.11.2004.2825 will continue to work unmodified.</span></span>

<span data-ttu-id="e8eef-118">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [컴파일러](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [런타임](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed), [IQ#](https://github.com/microsoft/iqsharp/pulls?q=is%3Apr+is%3Aclosed) 및 [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed)에 대한 비공개 PR의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-118">See the full list of closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed), [IQ#](https://github.com/microsoft/iqsharp/pulls?q=is%3Apr+is%3Aclosed) and [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

> [!NOTE]
> <span data-ttu-id="e8eef-119">이 버전에는 Q# 프로젝트 컴파일에 영향을 주는 버그가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-119">This version contains a bug affecting compilation of Q# projects.</span></span> <span data-ttu-id="e8eef-120">최신 릴리스로 업그레이드하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-120">We recommend upgrading to a newer release.</span></span>

## <a name="version-01120042825"></a><span data-ttu-id="e8eef-121">버전 0.11.2004.2825</span><span class="sxs-lookup"><span data-stu-id="e8eef-121">Version 0.11.2004.2825</span></span>

<span data-ttu-id="e8eef-122">*릴리스 날짜: 2020년 4월 30일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-122">*Release date: April 30th, 2020*</span></span>

<span data-ttu-id="e8eef-123">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-123">This release contains the following:</span></span>

- <span data-ttu-id="e8eef-124">C# 또는 Python 호스트 파일이 더 이상 필요하지 않은 Q# 명령줄 애플리케이션에 대한 지원이 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-124">New support for Q# command line applications, which no longer require a C# or Python host file.</span></span> <span data-ttu-id="e8eef-125">Q# 명령줄 애플리케이션을 시작하는 방법에 대한 자세한 내용은 [여기](xref:microsoft.quantum.install.standalone)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-125">For more information on getting started with Q# command line applications, see [here](xref:microsoft.quantum.install.standalone).</span></span>
- <span data-ttu-id="e8eef-126">C# 또는 Python 호스트 파일이 더 이상 필요하지 않은 퀀텀 난수 생성기 빠른 시작이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-126">Updated quantum random number generator quickstart to no longer require a C# or Python host file.</span></span> <span data-ttu-id="e8eef-127">업데이트된 [빠른 시작](xref:microsoft.quantum.quickstarts.qrng)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-127">See the updated  [Quickstart](xref:microsoft.quantum.quickstarts.qrng)</span></span>
- <span data-ttu-id="e8eef-128">IQ # Docker 이미지 성능 향상</span><span class="sxs-lookup"><span data-stu-id="e8eef-128">Performance improvements to IQ# Docker images</span></span>

> [!NOTE]
> <span data-ttu-id="e8eef-129">새로운 [`@EntryPoint()`](xref:microsoft.quantum.core.entrypoint) 특성을 사용하는 Q# 명령줄 애플리케이션은 현재 Python 또는 .NET 호스트 프로그램에서 호출할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-129">Q# command-line applications using the new [`@EntryPoint()`](xref:microsoft.quantum.core.entrypoint) attribute currently cannot be called from Python or .NET host programs.</span></span>
> <span data-ttu-id="e8eef-130">자세한 내용은 [Python](xref:microsoft.quantum.install.python) 및 [.NET 상호 운용성](xref:microsoft.quantum.install.cs) 가이드를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-130">See the [Python](xref:microsoft.quantum.install.python) and [.NET interoperability](xref:microsoft.quantum.install.cs) guides for more information.</span></span>

## <a name="version-01120033107"></a><span data-ttu-id="e8eef-131">버전 0.11.2003.3107</span><span class="sxs-lookup"><span data-stu-id="e8eef-131">Version 0.11.2003.3107</span></span>

<span data-ttu-id="e8eef-132">*릴리스 날짜: 2020년 3월 31일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-132">*Release date: March 31, 2020*</span></span>

<span data-ttu-id="e8eef-133">이 릴리스에는 버전 0.11.2003.2506에 대한 사소한 버그 수정이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-133">This release contains minor bugfixes for version 0.11.2003.2506.</span></span>

## <a name="version-01120032506"></a><span data-ttu-id="e8eef-134">버전 0.11.2003.2506</span><span class="sxs-lookup"><span data-stu-id="e8eef-134">Version 0.11.2003.2506</span></span>

<span data-ttu-id="e8eef-135">*릴리스 날짜: 2020년 3월 26일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-135">*Release date: March 26th, 2020*</span></span>

<span data-ttu-id="e8eef-136">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-136">This release contains the following:</span></span>

- <span data-ttu-id="e8eef-137">Q#의 액세스 한정자용 새로운 지원에 대한 자세한 내용은 [파일 구조](xref:microsoft.quantum.guide.filestructure)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-137">New support for access modifiers in Q#, for more information see [File Structures](xref:microsoft.quantum.guide.filestructure)</span></span>
- <span data-ttu-id="e8eef-138">.NET Core SDK 3.1로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e8eef-138">Updated to .NET Core SDK 3.1</span></span>

<span data-ttu-id="e8eef-139">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [컴파일러](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [런타임](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) 및 [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed)에 대한 비공개 PR의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-139">See the full list of closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) and [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

## <a name="version-01020022610"></a><span data-ttu-id="e8eef-140">버전 0.10.2002.2610</span><span class="sxs-lookup"><span data-stu-id="e8eef-140">Version 0.10.2002.2610</span></span>

<span data-ttu-id="e8eef-141">*릴리스 날짜: 2020년 2월 27일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-141">*Release date: February 27th, 2020*</span></span>

<span data-ttu-id="e8eef-142">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-142">This release contains the following:</span></span>

- <span data-ttu-id="e8eef-143">새로운 양자 기계 학습 라이브러리. 자세한 내용은 [QML 문서 페이지](https://docs.microsoft.com/quantum/libraries/machine-learning/?view=qsharp-preview)에서 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-143">New Quantum Machine Learning library, for more information go to our [QML docs page](https://docs.microsoft.com/quantum/libraries/machine-learning/?view=qsharp-preview)</span></span>
- <span data-ttu-id="e8eef-144">IQ# 버그 수정. NuGet 패키지를 로드할 때 성능이 최대 10-20배 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-144">IQ# bug fixes, resulting in up to a 10-20x performance increase when loading NuGet packages</span></span>

<span data-ttu-id="e8eef-145">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [컴파일러](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [런타임](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) 및 [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed)에 대한 비공개 PR의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-145">See the full list of closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) and [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

## <a name="version-01020012831"></a><span data-ttu-id="e8eef-146">버전 0.10.2001.2831</span><span class="sxs-lookup"><span data-stu-id="e8eef-146">Version 0.10.2001.2831</span></span>

<span data-ttu-id="e8eef-147">*릴리스 날짜: 2020년 1월 29일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-147">*Release date: January 29th, 2020*</span></span>

<span data-ttu-id="e8eef-148">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-148">This release contains the following:</span></span>

- <span data-ttu-id="e8eef-149">새 프로젝트를 만들 때 Microsoft.Quantum.Development.Kit NuGet 패키지를 대체할 새로운 Microsoft.Quantum.SDK NuGet</span><span class="sxs-lookup"><span data-stu-id="e8eef-149">New Microsoft.Quantum.SDK NuGet package which will replace Microsoft.Quantum.Development.Kit NuGet package when creating new projects.</span></span> <span data-ttu-id="e8eef-150">Microsoft.Quantum.Development.Kit NuGet 패키지는 기존 프로젝트를 계속 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-150">Microsoft.Quantum.Development.Kit NuGet package will continue to be supported for existing projects.</span></span> 
- <span data-ttu-id="e8eef-151">새로운 Microsoft.Quantum.SDK NuGet 패키지에서 사용하도록 설정된 Q# 컴파일러 확장 지원. 자세한 내용은 [Github의 설명서](https://github.com/microsoft/qsharp-compiler/tree/master/src/QuantumSdk#extending-the-q-compiler), [컴파일러 확장 샘플](https://github.com/microsoft/qsharp-compiler/tree/master/examples/CompilerExtensions) 및 [Q# 개발 블로그](https://devblogs.microsoft.com/qsharp/extending-the-q-compiler/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-151">Support for Q# compiler extensions, enabled by the new Microsoft.Quantum.SDK NuGet packge, for more information see the [documentation on Github](https://github.com/microsoft/qsharp-compiler/tree/master/src/QuantumSdk#extending-the-q-compiler), the [compiler extensions sample](https://github.com/microsoft/qsharp-compiler/tree/master/examples/CompilerExtensions) and the [Q# Dev Blog](https://devblogs.microsoft.com/qsharp/extending-the-q-compiler/)</span></span>
- <span data-ttu-id="e8eef-152">.NET Core 3.1에 대한 지원 추가. 이전 .NET Core SDK 버전으로 빌드하면 문제가 발생할 수 있으므로 버전 3.1.100을 설치하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-152">Added support for .NET Core 3.1, it is highly recommended to have version 3.1.100 installed since building with older .NET Core SDK versions may cause issues</span></span>
- <span data-ttu-id="e8eef-153">Microsoft.Quantum.QsCompiler.Experimental에서 사용할 수 있는 새 컴파일러 변환</span><span class="sxs-lookup"><span data-stu-id="e8eef-153">New compiler transformations available under Microsoft.Quantum.QsCompiler.Experimental</span></span>
- <span data-ttu-id="e8eef-154">IQ#에서 출력 상태 벡터를 HTML로 노출하는 새 기능</span><span class="sxs-lookup"><span data-stu-id="e8eef-154">New functionality to expose output state vectors as HTML in IQ#</span></span>
- <span data-ttu-id="e8eef-155">Hadamard 및 SWAP 테스트를 위한 Microsoft.Quantum.Characterization에 EstimateFrequencyA 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e8eef-155">Added support for EstimateFrequencyA to Microsoft.Quantum.Characterization for Hadamard and SWAP tests</span></span>
- <span data-ttu-id="e8eef-156">이제 AmplitudeAmplification 네임스페이스에서 Q# 스타일 가이드 사용</span><span class="sxs-lookup"><span data-stu-id="e8eef-156">AmplitudeAmplification namespace now uses Q# style guide</span></span>

<span data-ttu-id="e8eef-157">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [컴파일러](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [런타임](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) 및 [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed)에 대한 비공개 PR의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-157">See the full list of closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) and [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

## <a name="version-01019120501"></a><span data-ttu-id="e8eef-158">버전 0.10.1912.0501</span><span class="sxs-lookup"><span data-stu-id="e8eef-158">Version 0.10.1912.0501</span></span>

<span data-ttu-id="e8eef-159">*릴리스 날짜: 2019년 12월 5일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-159">*Release date: December 5th, 2019*</span></span>

<span data-ttu-id="e8eef-160">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-160">This release contains the following:</span></span>

- <span data-ttu-id="e8eef-161">Q# 단위 테스트를 위한 새 테스트 속성은 [여기에서](https://docs.microsoft.com/qsharp/api/qsharp/microsoft.quantum.diagnostics.test) 업데이트된 API 설명서 및 [여기에서](xref:microsoft.quantum.guide.testingdebugging) 업데이트된 테스트 & 디버깅 가이드를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-161">New Test attribute for Q# unit testing, see updated API documentation [here](https://docs.microsoft.com/qsharp/api/qsharp/microsoft.quantum.diagnostics.test) and updated testing & debugging guide [here](xref:microsoft.quantum.guide.testingdebugging)</span></span>
- <span data-ttu-id="e8eef-162">Q# 프로그램 실행 오류 발생 시 스택 추적 추가</span><span class="sxs-lookup"><span data-stu-id="e8eef-162">Added stack trace in the case of a Q# program execution error</span></span>
- <span data-ttu-id="e8eef-163">[OmniSharp C# Visual Studio Code 확장](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)의 업데이트로 인한 Visual Studio Code 중단점 지원</span><span class="sxs-lookup"><span data-stu-id="e8eef-163">Support for breakpoints in Visual Studio Code due to an update in the [OmniSharp C# Visual Studio Code extension](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)</span></span>

<span data-ttu-id="e8eef-164">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [컴파일러](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [런타임](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) 및 [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed)에 대한 비공개 PR의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-164">See the full list of closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) and [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

## <a name="version-01019111607"></a><span data-ttu-id="e8eef-165">버전 0.10.1911.1607</span><span class="sxs-lookup"><span data-stu-id="e8eef-165">Version 0.10.1911.1607</span></span>

<span data-ttu-id="e8eef-166">*릴리스 날짜: 2019년 11월 17일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-166">*Release date: November 17th, 2019*</span></span>

<span data-ttu-id="e8eef-167">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-167">This release contains the following:</span></span>

- <span data-ttu-id="e8eef-168">[Quantum Katas](https://github.com/Microsoft/QuantumKatas) 및 Jupyter Notebooks에 대한 성능 수정</span><span class="sxs-lookup"><span data-stu-id="e8eef-168">Performance fix for [Quantum Katas](https://github.com/Microsoft/QuantumKatas) and Jupyter notebooks</span></span>

<span data-ttu-id="e8eef-169">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [컴파일러](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [런타임](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) 및 [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed)에 대한 비공개 PR의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-169">See the full list of closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) and [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).</span></span>  


## <a name="version-0101911307"></a><span data-ttu-id="e8eef-170">버전 0.10.1911.307</span><span class="sxs-lookup"><span data-stu-id="e8eef-170">Version 0.10.1911.307</span></span>

<span data-ttu-id="e8eef-171">*릴리스 날짜: 2019년 11월 1일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-171">*Release date: November 1st, 2019*</span></span>

<span data-ttu-id="e8eef-172">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-172">This release contains the following:</span></span>

- <span data-ttu-id="e8eef-173">.NET Core SDK 버전에 종속되지 않도록 언어 서버를 자체 포함 실행 파일로 배포하는 Visual Studio Code 및 Visual Studio 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="e8eef-173">Updates to Visual Studio Code & Visual Studio extensions to deploy language server as a self-contained executable, eliminating the .NET Core SDK version dependency</span></span>  
- <span data-ttu-id="e8eef-174">.NET Core 3.0으로 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="e8eef-174">Migration to .NET Core 3.0</span></span>
- <span data-ttu-id="e8eef-175">새 `Fail` 메서드가 도입된 Microsoft.Quantum.Simulation.Core.IOperationFactory의 주요 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-175">Breaking change to Microsoft.Quantum.Simulation.Core.IOperationFactory with introduction of new `Fail` method.</span></span> <span data-ttu-id="e8eef-176">SimulatorBase를 확장하지 않는 사용자 지정 시뮬레이터에만 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-176">It affects only custom simulators that do not extend SimulatorBase.</span></span> <span data-ttu-id="e8eef-177">자세한 내용은 [GitHub에서 끌어오기 요청 보기를 참조하세요](https://github.com/microsoft/qsharp-runtime/pull/59).</span><span class="sxs-lookup"><span data-stu-id="e8eef-177">For more details, [view the pull request on GitHub](https://github.com/microsoft/qsharp-runtime/pull/59).</span></span>
- <span data-ttu-id="e8eef-178">사용되지 않는 특성에 대한 새로운 지원</span><span class="sxs-lookup"><span data-stu-id="e8eef-178">New support for Deprecated attributes</span></span>

<span data-ttu-id="e8eef-179">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [컴파일러](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [런타임](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) 및 [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed)에 대한 비공개 PR의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-179">See the full list of closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) and [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

## <a name="version-0919093002"></a><span data-ttu-id="e8eef-180">버전 0.9.1909.3002</span><span class="sxs-lookup"><span data-stu-id="e8eef-180">Version 0.9.1909.3002</span></span>

<span data-ttu-id="e8eef-181">*릴리스 날짜: 2019년 9월 30일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-181">*Release date: September 30th, 2019*</span></span>

<span data-ttu-id="e8eef-182">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-182">This release contains the following:</span></span>

- <span data-ttu-id="e8eef-183">Visual Studio 2019(버전 16.3 이상) 및 Visual Studio Code에서 Q# 코드 완성에 대한 새로운 지원</span><span class="sxs-lookup"><span data-stu-id="e8eef-183">New support for Q# code completion in Visual Studio 2019 (versions 16.3 & later) & Visual Studio Code</span></span>
- <span data-ttu-id="e8eef-184">양자 가산기에 대한 새 [Quantum Kata](https://github.com/Microsoft/QuantumKatas)</span><span class="sxs-lookup"><span data-stu-id="e8eef-184">New [Quantum Kata](https://github.com/Microsoft/QuantumKatas) for quantum adders</span></span>

<span data-ttu-id="e8eef-185">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [컴파일러](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [런타임](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) 및 [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed)에 대한 비공개 PR의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-185">See the full list of closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) and [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

## <a name="version-09-packagereference-0919082902"></a><span data-ttu-id="e8eef-186">버전 0.9(*PackageReference 0.9.1908.2902*)</span><span class="sxs-lookup"><span data-stu-id="e8eef-186">Version 0.9 (*PackageReference 0.9.1908.2902*)</span></span>

<span data-ttu-id="e8eef-187">*릴리스 날짜: 2019년 8월 29일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-187">*Release date: August 29th, 2019*</span></span>

<span data-ttu-id="e8eef-188">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-188">This release contains the following:</span></span>

- <span data-ttu-id="e8eef-189">Q#의 [접합 문](xref:microsoft.quantum.guide.operationsfunctions#conjugations)에 대한 새로운 지원</span><span class="sxs-lookup"><span data-stu-id="e8eef-189">New support for [conjugation statements](xref:microsoft.quantum.guide.operationsfunctions#conjugations) in Q#</span></span>
- <span data-ttu-id="e8eef-190">컴파일러의 새 코드 작업(예: "바꿀 내용", "설명서 추가" 및 단순 배열 항목 업데이트)</span><span class="sxs-lookup"><span data-stu-id="e8eef-190">New code actions in the compiler, such as: "replace with", "add documentation", and simple array item update</span></span>
- <span data-ttu-id="e8eef-191">설치 템플릿 및 새 프로젝트 명령이 Visual Studio Code 확장에 추가됨</span><span class="sxs-lookup"><span data-stu-id="e8eef-191">Added install template and new project commands to Visual Studio Code extension</span></span>
- <span data-ttu-id="e8eef-192">ApplyIf 조합기의 새 변형(예: [Microsoft.Quantum.Canon.ApplyIfOne](xref:microsoft.quantum.canon.applyifone))이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e8eef-192">Added new variants of ApplyIf combinator such as [Microsoft.Quantum.Canon.ApplyIfOne](xref:microsoft.quantum.canon.applyifone)</span></span>
- <span data-ttu-id="e8eef-193">추가 [Quantum Katas](https://github.com/Microsoft/QuantumKatas)가 Jupyter Notebook으로 변환됨</span><span class="sxs-lookup"><span data-stu-id="e8eef-193">Additional [Quantum Katas](https://github.com/Microsoft/QuantumKatas) converted to Jupyter Notebooks</span></span>
- <span data-ttu-id="e8eef-194">Visual Studio 확장에는 이제 Visual Studio 2019가 필요함</span><span class="sxs-lookup"><span data-stu-id="e8eef-194">Visual Studio Extension now requires Visual Studio 2019</span></span>

<span data-ttu-id="e8eef-195">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [컴파일러](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [런타임](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) 및 [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed)에 대한 비공개 PR의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-195">See the full list of closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) and [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

<span data-ttu-id="e8eef-196">여기에는 변경 내용이 요약되어 있으며, 기존 프로그램을 업그레이드하는 방법에 대한 지침도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-196">The changes are summarized here as well as instructions for upgrading your existing programs.</span></span>  <span data-ttu-id="e8eef-197">이러한 변경 내용은 [Q# 개발 블로그](https://devblogs.microsoft.com/qsharp)에서 자세히 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-197">Read more about these changes on the [Q# dev blog](https://devblogs.microsoft.com/qsharp).</span></span>

## <a name="version-08-packagereference-0819071701"></a><span data-ttu-id="e8eef-198">버전 0.8(*PackageReference 0.8.1907.1701*)</span><span class="sxs-lookup"><span data-stu-id="e8eef-198">Version 0.8 (*PackageReference 0.8.1907.1701*)</span></span>

<span data-ttu-id="e8eef-199">*릴리스 날짜: 2019년 7월 12일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-199">*Release date: July 12, 2019*</span></span>

<span data-ttu-id="e8eef-200">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-200">This release contains the following:</span></span>

- <span data-ttu-id="e8eef-201">배열 조각화에 대한 새 인덱싱 위치 - 자세한 내용은 [언어 참조](xref:microsoft.quantum.guide.expressions#array-slices)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-201">New indexing locations for slicing arrays, [see the language reference](xref:microsoft.quantum.guide.expressions#array-slices) for more information.</span></span>
- <span data-ttu-id="e8eef-202">[Microsoft Container Registry](https://github.com/microsoft/ContainerRegistry)에서 호스팅되는 Docker 파일이 추가됨 - 자세한 내용은 [IQ# 리포지토리](https://github.com/microsoft/iqsharp/blob/master/README.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-202">Added Dockerfile hosted on the [Microsoft Container Registry](https://github.com/microsoft/ContainerRegistry), see the [IQ# repository for more information](https://github.com/microsoft/iqsharp/blob/master/README.md)</span></span>
- <span data-ttu-id="e8eef-203">[추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)에 대한 호환성이 손상되는 변경, 구성 설정 업데이트, 이름 변경 - [업데이트된 이름에 대한 .NET API 브라우저](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulatorconfiguration)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-203">Breaking change for [the trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), update to configuration settings, name changes; see the [.NET API Browser for the updated names](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulatorconfiguration).</span></span>

<span data-ttu-id="e8eef-204">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) 및 [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed)에 대한 비공개 PR의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-204">See the full list of closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) and [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

## <a name="version-07-packagereference-0719053109"></a><span data-ttu-id="e8eef-205">버전 0.7(*PackageReference 0.7.1905.3109*)</span><span class="sxs-lookup"><span data-stu-id="e8eef-205">Version 0.7 (*PackageReference 0.7.1905.3109*)</span></span>

<span data-ttu-id="e8eef-206">*릴리스 날짜: 2019년 5월 31일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-206">*Release date: May 31, 2019*</span></span>

<span data-ttu-id="e8eef-207">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-207">This release contains the following:</span></span>
- <span data-ttu-id="e8eef-208">Q# 언어에 추가된 항목</span><span class="sxs-lookup"><span data-stu-id="e8eef-208">additions to the Q# language,</span></span> 
- <span data-ttu-id="e8eef-209">화학 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="e8eef-209">updates to the chemistry library,</span></span> 
- <span data-ttu-id="e8eef-210">새 숫자 라이브러리</span><span class="sxs-lookup"><span data-stu-id="e8eef-210">a new numerics library.</span></span>

<span data-ttu-id="e8eef-211">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) 및 [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed)에 대한 비공개 PR의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-211">See the full list of closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) and [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

<span data-ttu-id="e8eef-212">여기에는 변경 내용이 요약되어 있으며, 기존 프로그램을 업그레이드하는 방법에 대한 지침도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-212">The changes are summarized here as well as instructions for upgrading your existing programs.</span></span>  <span data-ttu-id="e8eef-213">이러한 변경 내용은 [Q# 개발 블로그](https://devblogs.microsoft.com/qsharp)에서 자세히 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-213">Read more about these changes on the [Q# dev blog](https://devblogs.microsoft.com/qsharp).</span></span>

### <a name="q-language-syntax"></a><span data-ttu-id="e8eef-214">Q # 언어 구문</span><span class="sxs-lookup"><span data-stu-id="e8eef-214">Q# language syntax</span></span>
<span data-ttu-id="e8eef-215">이 릴리스에 추가된 새 Q# 언어 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-215">This release adds new Q# language syntax:</span></span>
* <span data-ttu-id="e8eef-216">[사용자 정의 형식](xref:microsoft.quantum.guide.types#user-defined-types)에 대해 명명된 항목이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-216">Add named items for [user-defined types](xref:microsoft.quantum.guide.types#user-defined-types).</span></span>  
* <span data-ttu-id="e8eef-217">이제 사용자 정의 형식 생성자를 함수로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-217">User-defined type constructors can now be used as functions.</span></span>
* <span data-ttu-id="e8eef-218">[복사 및 업데이트](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions)(copy-and-update) 및 [적용 및 재할당](xref:microsoft.quantum.guide.variables#rebinding-of-mutable-symbols)(apply-and-reassign) 지원이 사용자 정의 형식에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-218">Add support for [copy-and-update](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) and [apply-and-reassign](xref:microsoft.quantum.guide.variables#rebinding-of-mutable-symbols) in user-defined types.</span></span>
* <span data-ttu-id="e8eef-219">[성공할 때까지 반복](xref:microsoft.quantum.guide.controlflow#repeat-until-success-loop)(repeat-until-success) 루프에 대한 픽스업 블록은 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-219">Fixup-block for [repeat-until-success](xref:microsoft.quantum.guide.controlflow#repeat-until-success-loop) loops is now optional.</span></span>
* <span data-ttu-id="e8eef-220">이제 작동 중이 아닌 함수에서 while 루프를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-220">We now support while loops in functions (not in operations).</span></span>

### <a name="library"></a><span data-ttu-id="e8eef-221">라이브러리</span><span class="sxs-lookup"><span data-stu-id="e8eef-221">Library</span></span> 

<span data-ttu-id="e8eef-222">이 릴리스에는 숫자 라이브러리가 추가되었습니다. [새 숫자 라이브러리를 사용](xref:microsoft.quantum.numerics.usage)하는 방법에 대한 자세한 정보를 알아보고, [새 샘플](https://github.com/microsoft/quantum/tree/master/Numerics)을 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-222">This release adds a numerics library: Learn more about how to [use the new numerics library](xref:microsoft.quantum.numerics.usage) and try out the [new samples](https://github.com/microsoft/quantum/tree/master/Numerics).</span></span>  <span data-ttu-id="e8eef-223">[PR #102](https://github.com/Microsoft/QuantumLibraries/pull/102)</span><span class="sxs-lookup"><span data-stu-id="e8eef-223">[PR #102](https://github.com/Microsoft/QuantumLibraries/pull/102).</span></span>  

<span data-ttu-id="e8eef-224">이 릴리스에서는 화학 라이브러리가 확장 및 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-224">This release reorganizes extends and updates the chemistry library:</span></span>
* <span data-ttu-id="e8eef-225">구성 요소, 확장성, 일반 코드 정리의 모듈화가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-225">Improves modularity of components, extensibility, general code cleanup.</span></span>  <span data-ttu-id="e8eef-226">[PR #58](https://github.com/microsoft/QuantumLibraries/pull/58).</span><span class="sxs-lookup"><span data-stu-id="e8eef-226">[PR #58](https://github.com/microsoft/QuantumLibraries/pull/58).</span></span>
* <span data-ttu-id="e8eef-227">[다중 참조 wavefunction(파동 함수)](xref:microsoft.quantum.chemistry.concepts.multireference)에 대한 지원(스파스 다중 참조 파동 함수 및 단일 결합 클러스터 모두)이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-227">Add support for [multi-reference wavefunctions](xref:microsoft.quantum.chemistry.concepts.multireference), both sparse multi-reference wavefunctions and unitary coupled cluster.</span></span>  <span data-ttu-id="e8eef-228">[PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110)</span><span class="sxs-lookup"><span data-stu-id="e8eef-228">[PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110).</span></span>
* <span data-ttu-id="e8eef-229">(감사합니다!) [1QBit](https://1qbit.com) 기여자([@valentinS4t1qbit](https://github.com/ValentinS4t1qbit)): 변이 가설 풀이(variational ansatz)를 사용한 에너지 평가입니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-229">(Thank you!) [1QBit](https://1qbit.com) contributor ([@valentinS4t1qbit](https://github.com/ValentinS4t1qbit)): Energy evaluation using variational ansatz.</span></span> <span data-ttu-id="e8eef-230">[PR #120](https://github.com/Microsoft/QuantumLibraries/pull/120)</span><span class="sxs-lookup"><span data-stu-id="e8eef-230">[PR #120](https://github.com/Microsoft/QuantumLibraries/pull/120).</span></span>
* <span data-ttu-id="e8eef-231">[Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) 스키마가 새 [0.2 버전](xref:microsoft.quantum.libraries.chemistry.schema.spec_v_0_2)으로 업데이트되고, 단일 결합 클러스터 사양이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-231">Updating [Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) schema to new [version 0.2](xref:microsoft.quantum.libraries.chemistry.schema.spec_v_0_2), adding unitary coupled cluster specification.</span></span> <span data-ttu-id="e8eef-232">[Issue #65](https://github.com/microsoft/QuantumLibraries/issues/65)</span><span class="sxs-lookup"><span data-stu-id="e8eef-232">[Issue #65](https://github.com/microsoft/QuantumLibraries/issues/65).</span></span>
* <span data-ttu-id="e8eef-233">Python 상호 운용성이 화학 라이브러리 기능에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-233">Adding Python interoperability to chemistry library functions.</span></span> <span data-ttu-id="e8eef-234">이 [샘플](https://github.com/microsoft/Quantum/tree/master/Chemistry/PythonIntegration)을 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-234">Try out this [sample](https://github.com/microsoft/Quantum/tree/master/Chemistry/PythonIntegration).</span></span> <span data-ttu-id="e8eef-235">[이슈 #53](https://github.com/microsoft/QuantumLibraries/issues/53) [PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110).</span><span class="sxs-lookup"><span data-stu-id="e8eef-235">[Issue #53](https://github.com/microsoft/QuantumLibraries/issues/53) [PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110).</span></span>

## <a name="version-061905"></a><span data-ttu-id="e8eef-236">버전 0.6.1905</span><span class="sxs-lookup"><span data-stu-id="e8eef-236">Version 0.6.1905</span></span>

<span data-ttu-id="e8eef-237">*릴리스 날짜: 2019년 5월 3일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-237">*Release date: May 3, 2019*</span></span>

<span data-ttu-id="e8eef-238">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-238">This release contains the following:</span></span>
- <span data-ttu-id="e8eef-239">Q# 언어 변경</span><span class="sxs-lookup"><span data-stu-id="e8eef-239">makes changes to the Q# language,</span></span> 
- <span data-ttu-id="e8eef-240">Quantum Development Kit 라이브러리 재구성</span><span class="sxs-lookup"><span data-stu-id="e8eef-240">restructures the Quantum Development Kit libraries,</span></span> 
- <span data-ttu-id="e8eef-241">새 샘플 추가</span><span class="sxs-lookup"><span data-stu-id="e8eef-241">adds new samples, and</span></span> 
- <span data-ttu-id="e8eef-242">버그 수정</span><span class="sxs-lookup"><span data-stu-id="e8eef-242">fixes bugs.</span></span>  <span data-ttu-id="e8eef-243">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) 및 [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed)에 대한 몇 가지 비공개 PR</span><span class="sxs-lookup"><span data-stu-id="e8eef-243">Several closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) and [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

<span data-ttu-id="e8eef-244">여기에는 변경 내용이 요약되어 있으며, 기존 프로그램을 업그레이드하는 방법에 대한 지침도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-244">The changes are summarized here as well as instructions for upgrading your existing programs.</span></span>  <span data-ttu-id="e8eef-245">이러한 변경 내용은 devblogs.microsoft.com/qsharp에서 자세히 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-245">You can read more about these changes on devblogs.microsoft.com/qsharp.</span></span>

### <a name="q-language-syntax"></a><span data-ttu-id="e8eef-246">Q # 언어 구문</span><span class="sxs-lookup"><span data-stu-id="e8eef-246">Q# language syntax</span></span>
<span data-ttu-id="e8eef-247">이 릴리스에 추가된 새 Q# 언어 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-247">This release adds new Q# language syntax:</span></span>
* <span data-ttu-id="e8eef-248">`+` 연산자를 사용하여 [양자 연산 특수화(제어 및 수반(adjoint))를 표현하는 간단한 방법](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations)이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-248">Add a [shorthand way to express specializations of quantum operations](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations) (control and adjoints) with `+` operators.</span></span>  <span data-ttu-id="e8eef-249">이전 구문은 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-249">The old syntax is deprecated.</span></span>  <span data-ttu-id="e8eef-250">이전 구문(예: `: adjoint`)을 사용하는 프로그램은 계속 작동하지만 컴파일 시간 경고가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-250">Programs that use the old syntax (e.g., `: adjoint`) will continue to work, but a compile time warning will be generated.</span></span>  
* <span data-ttu-id="e8eef-251">새로운 [복사 및 업데이트](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) 연산자인 `w/`가 추가되었습니다. 이는 배열 만들기를 기존 배열의 수정으로 표현하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-251">Add a new operator for [copy-and-update](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions), `w/`, can be used to express array creation as a modification of an existing array.</span></span>
* <span data-ttu-id="e8eef-252">일반적인 [적용 및 업데이트(apply-and-update) 문](xref:microsoft.quantum.guide.variables#rebinding-of-mutable-symbols)(예: `+=`, `w/=`)이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-252">Add the common [apply-and-update statement](xref:microsoft.quantum.guide.variables#rebinding-of-mutable-symbols), e.g., `+=`, `w/=`.</span></span>
* <span data-ttu-id="e8eef-253">짧은 네임스페이스 이름을 지정하는 방법이 [open 지시문](xref:microsoft.quantum.guide.filestructure#open-directives)에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-253">Add a way to specify a short name for namespaces in [open directives](xref:microsoft.quantum.guide.filestructure#open-directives).</span></span>

<span data-ttu-id="e8eef-254">이 릴리즈에서는 더 이상 배열 요소를 set 문의 왼쪽에 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-254">With this release, we no longer allow an array element to be specified on the left side of a set statement.</span></span>  <span data-ttu-id="e8eef-255">이는 실제로 연산 결과에서 항상 수정을 통해 새 배열을 만드는 경우 구문에서 이 배열을 변경할 수 있음을 의미하기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-255">This is because that syntax implies that arrays are mutable when in fact, the result of the operation has always been the creation of a new array with the modification.</span></span>  <span data-ttu-id="e8eef-256">대신, 동일한 결과를 얻기 위해 새 복사 및 업데이트 연산자인 `w/`를 사용하라는 제안과 함께 컴파일러 오류가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-256">Instead, a compiler error will be generated with a suggestion to use the new copy-and-update operator, `w/`, to accomplish the same result.</span></span>  

### <a name="library-restructuring"></a><span data-ttu-id="e8eef-257">라이브러리 재구성</span><span class="sxs-lookup"><span data-stu-id="e8eef-257">Library restructuring</span></span>
<span data-ttu-id="e8eef-258">이 릴리스에서는 라이브러리를 다음과 같이 일관된 방식으로 확장할 수 있도록 재구성합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-258">This release reorganizes the libraries to enable their growth in a consistent way:</span></span>
* <span data-ttu-id="e8eef-259">Microsoft.Quantum.Primitive 네임스페이스의 이름을 Microsoft.Quantum.Intrinsic으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-259">Renames the Microsoft.Quantum.Primitive namespace  to Microsoft.Quantum.Intrinsic.</span></span>  <span data-ttu-id="e8eef-260">이러한 연산은 대상 머신에서 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-260">These operations are implemented by the target machine.</span></span>  <span data-ttu-id="e8eef-261">Microsoft.Quantum.Primitive 네임스페이스는 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-261">The Microsoft.Quantum.Primitive namespace is deprecated.</span></span>  <span data-ttu-id="e8eef-262">프로그램에서 더 이상 사용되지 않는 이름을 사용하여 연산과 함수를 호출하는 경우 런타임 경고에서 이를 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-262">A runtime warning will advise when programs call operations and functions using deprecated names.</span></span>

* <span data-ttu-id="e8eef-263">Microsoft.Quantum.Canon 패키지의 이름을 Microsoft.Quantum.Standard로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-263">Renames the Microsoft.Quantum.Canon package to Microsoft.Quantum.Standard.</span></span>  <span data-ttu-id="e8eef-264">이 패키지에는 대부분의 Q# 프로그램에 공통된 네임스페이스가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-264">This package contains namespaces that are common to most Q# programs.</span></span>  <span data-ttu-id="e8eef-265">다음 내용이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-265">This includes:</span></span>  
    - <span data-ttu-id="e8eef-266">일반 연산에 대한 Microsoft.Quantum.Canon</span><span class="sxs-lookup"><span data-stu-id="e8eef-266">Microsoft.Quantum.Canon for common operations</span></span>
    - <span data-ttu-id="e8eef-267">범용 산술 연산용 Microsoft.Quantum.Arithmetic</span><span class="sxs-lookup"><span data-stu-id="e8eef-267">Microsoft.Quantum.Arithmetic for general purpose arithmetic operations</span></span>
    - <span data-ttu-id="e8eef-268">큐비트 상태를 준비하는 데 사용되는 연산에 대한 Microsoft.Quantum.Preparation</span><span class="sxs-lookup"><span data-stu-id="e8eef-268">Microsoft.Quantum.Preparation for operations used to prepare qubit state</span></span>
    - <span data-ttu-id="e8eef-269">시뮬레이션 기능에 대한 Microsoft.Quantum.Simulation</span><span class="sxs-lookup"><span data-stu-id="e8eef-269">Microsoft.Quantum.Simulation for simulation functionality</span></span>

<span data-ttu-id="e8eef-270">이 변경으로 인해 Microsoft.Quatum.Canon 네임스페이스에 대한 단일 "open" 문이 포함된 프로그램에서 다른 세 개의 새 네임스페이스로 이동된 연산을 참조하는 경우 빌드 오류가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-270">With this change, programs that include a single "open" statement for the namespace Microsoft.Quatum.Canon may encounter build errors if the program references operations that were moved to the other three new namespaces.</span></span>  <span data-ttu-id="e8eef-271">세 개의 새 네임스페이스에 대한 추가 open 문을 추가하면 이 문제를 간단히 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-271">Adding the additional open statements for the three new namespaces is a straightforward way to resolve this issue.</span></span>  

* <span data-ttu-id="e8eef-272">내부 연산이 다른 네임스페이스로 재구성되었으므로 여러 네임스페이스가 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-272">Several namespaces have been deprecated as the operations within have been reorganized to other namespaces.</span></span> <span data-ttu-id="e8eef-273">이러한 네임스페이스를 사용하는 프로그램은 계속 작동하며, 컴파일 시간 경고는 연산이 정의된 네임스페이스를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-273">Programs that use these namespaces will continue to work, and a compile time warning will denote the namespace where the operation is defined.</span></span>  

* <span data-ttu-id="e8eef-274">Microsoft.Quantum.Arithmetic 네임스페이스는 <xref:microsoft.quantum.arithmetic.littleendian> 사용자 정의 형식을 사용하도록 일반화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-274">The Microsoft.Quantum.Arithmetic namespace has been normalized to use the <xref:microsoft.quantum.arithmetic.littleendian> user-defined type.</span></span> <span data-ttu-id="e8eef-275">little endian으로 변환해야 하는 경우, 함수 [BigEndianAsLittleEndian](xref:microsoft.quantum.arithmetic.bigendianaslittleendian)을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-275">Use the function [BigEndianAsLittleEndian](xref:microsoft.quantum.arithmetic.bigendianaslittleendian) when needed to convert to little endian.</span></span>  

* <span data-ttu-id="e8eef-276">몇몇 호출 가능 항목(함수 및 작업)의 이름이 [Q# 스타일 가이드](xref:microsoft.quantum.contributing.style)에 맞춰 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-276">The names of several callables (functions and operations) have been changed to conform to the [Q# Style Guide](xref:microsoft.quantum.contributing.style).</span></span>  <span data-ttu-id="e8eef-277">이전 호출 가능 이름은 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-277">The old callable names are deprecated.</span></span>  <span data-ttu-id="e8eef-278">이전 호출 가능 항목을 사용하는 프로그램은 계속 작동하지만 컴파일 시간 경고가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-278">Programs that use the old callables will continue to work with a compile time warning.</span></span> 

### <a name="new-samples"></a><span data-ttu-id="e8eef-279">새 샘플</span><span class="sxs-lookup"><span data-stu-id="e8eef-279">New Samples</span></span>

<span data-ttu-id="e8eef-280">[F# 드라이버에 Q#를 사용하는 샘플](https://github.com/Microsoft/Quantum/pull/164)을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-280">We added a [sample of using Q# with F# driver](https://github.com/Microsoft/Quantum/pull/164).</span></span>  

<span data-ttu-id="e8eef-281">**감사합니다.**</span><span class="sxs-lookup"><span data-stu-id="e8eef-281">**Thank you!**</span></span> <span data-ttu-id="e8eef-282">[http://github.com/Microsoft/Quantum](http://github.com/Microsoft/Quantum ) 에서 열려 있는 코드베이스에 기여해 주신 분들께 감사의 말씀을 전합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-282">to the following contributor to our open code base at http://github.com/Microsoft/Quantum.</span></span> <span data-ttu-id="e8eef-283">이러한 기여는 Q# 코드의 다양한 샘플을 모으는 데 큰 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-283">These contributions add significantly to the rich samples of Q# code:</span></span>

* <span data-ttu-id="e8eef-284">Mathias Soeken([@msoeken](https://github.com/msoeken)): Oracle 함수 합성.</span><span class="sxs-lookup"><span data-stu-id="e8eef-284">Mathias Soeken ([@msoeken](https://github.com/msoeken)): Oracle function synthesis.</span></span> <span data-ttu-id="e8eef-285">[PR #135](https://github.com/Microsoft/Quantum/pull/135).</span><span class="sxs-lookup"><span data-stu-id="e8eef-285">[PR #135](https://github.com/Microsoft/Quantum/pull/135).</span></span>

### <a name="migrating-existing-projects-to-061905"></a><span data-ttu-id="e8eef-286">기존 프로젝트를 0.6.1905로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-286">Migrating existing projects to 0.6.1905.</span></span>

<span data-ttu-id="e8eef-287">QDK를 업데이트하려면 [설치 가이드](xref:microsoft.quantum.install)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-287">See the [install guide](xref:microsoft.quantum.install) to update the QDK.</span></span>
  
<span data-ttu-id="e8eef-288">Quantum Development Kit 버전 0.5의 기존 Q# 프로젝트가 있는 경우, 해당 프로젝트를 최신 버전으로 마이그레이션하는 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-288">If you have existing Q# projects from version 0.5 of the Quantum Development Kit, the following are the steps to migrate those projects to the newest version.</span></span>

    1. <span data-ttu-id="e8eef-289">프로젝트는 순서대로 업그레이드해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-289">Projects need to be upgraded in order.</span></span>  <span data-ttu-id="e8eef-290">솔루션의 프로젝트가 여러 개인 경우, 각 프로젝트를 참조 순서대로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-290">If you have a solution with multiple projects, update each project in the order they are referenced.</span></span>
    2. <span data-ttu-id="e8eef-291">명령줄에서 `dotnet clean`을 실행하여 기존의 모든 이진 파일과 중간 파일을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-291">From a command line, Run `dotnet clean` to remove all existing binaries and intermediate files.</span></span>
    3. <span data-ttu-id="e8eef-292">텍스트 편집기에서 .csproj 파일을 편집하여 모든 "Microsoft.Quantum" `PackageReference`의 버전을 0.6.1904 버전으로 변경하고 "Microsoft.Quantum.Canon" 패키지 이름을 "Microsoft.Quantum.Standard"로 변경합니다. 예:</span><span class="sxs-lookup"><span data-stu-id="e8eef-292">In a text editor, edit the .csproj file to change the version of all the "Microsoft.Quantum" `PackageReference` to version 0.6.1904, and change the "Microsoft.Quantum.Canon" package name to "Microsoft.Quantum.Standard", for example:</span></span>

         ```xml
        <PackageReference Include="Microsoft.Quantum.Standard" Version="0.6.1905.301" />
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.6.1905.301" />
        ```
    4. <span data-ttu-id="e8eef-293">명령줄에서 다음 명령을 실행합니다. `dotnet msbuild`</span><span class="sxs-lookup"><span data-stu-id="e8eef-293">From the command line, run this command: `dotnet msbuild`</span></span>  
    5. <span data-ttu-id="e8eef-294">이를 실행한 후에도 여전히 위에 나열한 변경 내용으로 인해 수동으로 오류를 해결해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-294">After running this, you might still need to manually address errors due to changes listed above.</span></span>  <span data-ttu-id="e8eef-295">대부분의 경우 Visual Studio 또는 Visual Studio Code의 IntelliSense가 이러한 오류를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-295">In many cases, these errors will also be reported by IntelliSense in Visual Studio or Visual Studio Code.</span></span>
        - <span data-ttu-id="e8eef-296">Visual Studio 2019 또는 Visual Studio Code에서 프로젝트의 루트 폴더 또는 포함 솔루션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-296">Open the root folder of the project or the containing solution in Visual Studio 2019 or Visual Studio Code.</span></span>
        - <span data-ttu-id="e8eef-297">편집기에서 .qs 파일을 열면 출력 창에 Q# 언어 확장의 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-297">After opening a .qs file in the editor, you should see the output of the Q# language extension in the output window.</span></span>
        - <span data-ttu-id="e8eef-298">프로젝트를 로드한 후(출력 창에 표시됨), 각 파일을 열어 남은 모든 문제를 수동으로 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-298">After the project has loaded successfully (indicated in the output window) open each file and manually to address all remaining issues.</span></span>

> [!NOTE]
> * <span data-ttu-id="e8eef-299">0\.6 릴리스의 경우, Quantum Development Kit에 포함된 언어 서버는 여러 작업 영역을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-299">For the 0.6 release, the language server included with the Quantum Development Kit does not support multiple workspaces.</span></span>
> * <span data-ttu-id="e8eef-300">Visual Studio Code에서 프로젝트 작업을 하려면 해당 프로젝트 자체와 참조된 모든 프로젝트가 포함된 루트 폴더를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-300">In order to work with a project in Visual Studio Code, open the root folder containing the project itself and all referenced projects.</span></span>   
> * <span data-ttu-id="e8eef-301">Visual Studio에서 솔루션을 사용하려면 솔루션에 포함된 모든 프로젝트가 솔루션이 있는 폴더나 그 하위 폴더 중 하나에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-301">In order to work with a solution in Visual Studio, all projects contained in the solution need to be in the same folder as the solution or in one of its subfolders.</span></span>  
> * <span data-ttu-id="e8eef-302">0\.6 이상에 마이그레이션된 프로젝트와 이전 패키지 버전을 사용하는 프로젝트 간의 참조는 지원되지 **않습니다**.</span><span class="sxs-lookup"><span data-stu-id="e8eef-302">References between projects migrated to 0.6 and higher and projects using older package versions are **not** supported.</span></span>

## <a name="version-051904"></a><span data-ttu-id="e8eef-303">버전 0.5.1904</span><span class="sxs-lookup"><span data-stu-id="e8eef-303">Version 0.5.1904</span></span>

<span data-ttu-id="e8eef-304">*릴리스 날짜: 2019년 4월 15일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-304">*Release date: April 15, 2019*</span></span>

<span data-ttu-id="e8eef-305">이 릴리스에는 버그 수정이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-305">This release contains bug fixes.</span></span>


## <a name="version-051903"></a><span data-ttu-id="e8eef-306">버전 0.5.1903</span><span class="sxs-lookup"><span data-stu-id="e8eef-306">Version 0.5.1903</span></span>

<span data-ttu-id="e8eef-307">*릴리스 날짜: 2019년 3월 27일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-307">*Release date: March 27, 2019*</span></span>

<span data-ttu-id="e8eef-308">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-308">This release contains the following:</span></span>

- <span data-ttu-id="e8eef-309">Q#를 학습할 수 있는 좋은 방법을 제공하는 Jupyter Notebook에 대한 지원이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-309">Adds support for Jupyter Notebook, which offers a great way to learn about Q#.</span></span>  <span data-ttu-id="e8eef-310">[새 Jupyter Notebook 샘플을 확인하고 사용자 고유의 노트북을 작성하는 방법을 알아보세요](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="e8eef-310">[Check out new Jupyter Notebook samples and learn how to write your own Notebooks](xref:microsoft.quantum.install).</span></span> 

- <span data-ttu-id="e8eef-311">정수 adder 산술을 Quantum Canon 라이브러리에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-311">Adds integer adder arithmetic to the Quantum Canon library.</span></span>  <span data-ttu-id="e8eef-312">[새 정수 adder를 사용하는 방법](https://github.com/microsoft/Quantum/blob/master/samples/arithmetic/AdderExample.ipynb)을 설명하는 Jupyter Notebook도 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-312">See also a Jupyter Notebook that [describes how to use the new integer adders](https://github.com/microsoft/Quantum/blob/master/samples/arithmetic/AdderExample.ipynb).</span></span>

- <span data-ttu-id="e8eef-313">커뮤니티가 보고한 DumpRegister 문제의 버그를 수정했습니다([#148](https://github.com/Microsoft/Quantum/issues/148)).</span><span class="sxs-lookup"><span data-stu-id="e8eef-313">Bug fix for DumpRegister issue reported by the community ([#148](https://github.com/Microsoft/Quantum/issues/148)).</span></span>

- <span data-ttu-id="e8eef-314">[문 사용](xref:microsoft.quantum.guide.qubits#allocating-qubits) 내에서 반환하는 기능을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-314">Added ability to return from within a [using statement](xref:microsoft.quantum.guide.qubits#allocating-qubits).</span></span>

- <span data-ttu-id="e8eef-315">[시작 가이드](xref:microsoft.quantum.install)를 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-315">Revamped [getting started guide](xref:microsoft.quantum.install).</span></span>


## <a name="version-051902"></a><span data-ttu-id="e8eef-316">버전 0.5.1902</span><span class="sxs-lookup"><span data-stu-id="e8eef-316">Version 0.5.1902</span></span>

<span data-ttu-id="e8eef-317">*릴리스 날짜: 2019년 2월 27일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-317">*Release date: February 27, 2019*</span></span>

<span data-ttu-id="e8eef-318">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-318">This release contains the following:</span></span>

- <span data-ttu-id="e8eef-319">플랫폼 간 Python 호스트에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-319">Adds support for a cross-platform Python host.</span></span>  <span data-ttu-id="e8eef-320">Python의 `qsharp` 패키지를 사용하면 Python 내에서 Q# 작업 및 함수를 쉽게 시뮬레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-320">The `qsharp` package for Python makes it easy to simulate Q# operations and functions from within Python.</span></span> <span data-ttu-id="e8eef-321">[Python 상호 운용성](xref:microsoft.quantum.install)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-321">Learn more about [Python interoperability](xref:microsoft.quantum.install).</span></span> 

- <span data-ttu-id="e8eef-322">Visual Studio 및 Visual Studio Code 확장은 이제 기호 이름 바꾸기(예: 함수 및 작업)를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-322">The Visual Studio and Visual Studio Code extensions now support renaming of symbols (e.g., functions and operations).</span></span>

- <span data-ttu-id="e8eef-323">이제 Visual Studio 2019에 Visual Studio 확장을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-323">The Visual Studio extension can now be installed on Visual Studio 2019.</span></span>

## <a name="version-041901"></a><span data-ttu-id="e8eef-324">버전 0.4.1901</span><span class="sxs-lookup"><span data-stu-id="e8eef-324">Version 0.4.1901</span></span>

<span data-ttu-id="e8eef-325">*릴리스 날짜: 2019년 1월 30일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-325">*Release date: January 30, 2019*</span></span>

<span data-ttu-id="e8eef-326">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-326">This release contains the following:</span></span>

- <span data-ttu-id="e8eef-327">임의적 크기의 부호 있는 정수를 나타내는 새 기본 형식인 BigInt에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-327">adds support for a new primitive type, BigInt, which represents a signed integer of arbitrary size.</span></span>  <span data-ttu-id="e8eef-328">[BigInt 형식](xref:microsoft.quantum.guide.types)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-328">Learn more about [BigInt type](xref:microsoft.quantum.guide.types).</span></span>
- <span data-ttu-id="e8eef-329">매우 많은 수의 큐비트로 X, CNOT, 다중 제어 X 퀀텀 작업을 시뮬레이션할 수 있는 특별한 용도의 고속 시뮬레이터인 새 Toffoli 시뮬레이터를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-329">adds new Toffoli simulator, a special purpose fast simulator that can simulate X, CNOT and multi-controlled X quantum operations with very large numbers of qubits.</span></span>  <span data-ttu-id="e8eef-330">[Toffoli 시뮬레이터](xref:microsoft.quantum.machines.toffoli-simulator)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-330">Learn more about [Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator).</span></span>
- <span data-ttu-id="e8eef-331">퀀텀 컴퓨터에서 Q# 작업의 지정된 인스턴스를 실행하는 데 필요한 리소스를 추정하는 간단한 리소스 추정기를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-331">adds a simple resource estimator that estimates the resources required to run a given instancee of a Q# operation on a quantum computer.</span></span>  <span data-ttu-id="e8eef-332">[리소스 추정기](xref:microsoft.quantum.machines.resources-estimator)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-332">Learn more about the [Resource Estimator](xref:microsoft.quantum.machines.resources-estimator).</span></span>


## <a name="version-0318112802"></a><span data-ttu-id="e8eef-333">버전 0.3.1811.2802</span><span class="sxs-lookup"><span data-stu-id="e8eef-333">Version 0.3.1811.2802</span></span>

<span data-ttu-id="e8eef-334">*릴리스 날짜: 2018년 11월 28일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-334">*Release date: November 28, 2018*</span></span>

<span data-ttu-id="e8eef-335">어차피 VS Code 확장에서 사용하지 않고 있었지만 `event-stream` NPM 패키지와 관련된 [확장 제거](https://code.visualstudio.com/blogs/2018/11/26/event-stream) 작업 시 플래그를 지정하고 마켓플레이스에서 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-335">Even though our VS Code extension was not using it, it was flagged and removed from the marketplace during [the extensions purge](https://code.visualstudio.com/blogs/2018/11/26/event-stream) related to the `event-stream` NPM package.</span></span> <span data-ttu-id="e8eef-336">이 버전은 확장이 빨간색 플래그를 트리거할 수 있게 만드는 모든 런타임 종속성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-336">This version removes all runtime dependencies that could make the extension trigger any red flags.</span></span>

<span data-ttu-id="e8eef-337">이전에 확장을 설치한 경우, Visual Studio Marketplace에서 [Microsoft Quantum Development Kit for Visual Studio Code](vscode:extension/quantum.quantum-devkit-vscode) 확장을 방문한 다음, 설치를 눌러 다시 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-337">If you had previously installed the extension you will need to install it again by visiting the [Microsoft Quantum Development Kit for Visual Studio Code](vscode:extension/quantum.quantum-devkit-vscode) extension on the Visual Studio Marketplace and press Install.</span></span> <span data-ttu-id="e8eef-338">불편을 드려 죄송합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-338">We are sorry about the inconvenience.</span></span>


## <a name="version-0318111511"></a><span data-ttu-id="e8eef-339">버전 0.3.1811.1511</span><span class="sxs-lookup"><span data-stu-id="e8eef-339">Version 0.3.1811.1511</span></span>

<span data-ttu-id="e8eef-340">*릴리스 날짜: 2018년 11월 20일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-340">*Release date: November 20, 2018*</span></span>

<span data-ttu-id="e8eef-341">이 릴리스는 일부 사용자가 Visual Studio 확장을 로드할 수 없게 만드는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-341">This release fixes a bug that prevented some users to successfully load the Visual Studio extension.</span></span>

## <a name="version-031811203"></a><span data-ttu-id="e8eef-342">버전 0.3.1811.203</span><span class="sxs-lookup"><span data-stu-id="e8eef-342">Version 0.3.1811.203</span></span>

<span data-ttu-id="e8eef-343">*릴리스 날짜: 2018년 11월 2일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-343">*Release date: November 2, 2018*</span></span>

<span data-ttu-id="e8eef-344">이 릴리스에는 다음과 같은 몇 가지 버그 수정이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-344">This release includes a few bug fixes, including:</span></span>

* <span data-ttu-id="e8eef-345">`DumpMachine`을 호출하면 특정 상황에서 시뮬레이터의 상태가 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-345">Invoking `DumpMachine` could change the state of the simulator under certain situations.</span></span>
* <span data-ttu-id="e8eef-346">2\.1.403 이전의 .NET Core 버전을 사용하여 프로젝트를 빌드할 때 표시되는 컴파일 경고를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-346">Removed compilation warnings when building projects using a version of .NET Core previous to 2.1.403.</span></span>
* <span data-ttu-id="e8eef-347">설명서를 정리했습니다. 특히 VS Code 또는 Visual Studio에서 마우스로 가리킬 때 표시되는 도구 설명을 정리했습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-347">Clean up of documentation, specially the tooltips shown during mouse hover in VS Code or Visual Studio.</span></span>

## <a name="version-0318102508"></a><span data-ttu-id="e8eef-348">버전 0.3.1810.2508</span><span class="sxs-lookup"><span data-stu-id="e8eef-348">Version 0.3.1810.2508</span></span>

<span data-ttu-id="e8eef-349">*릴리스 날짜: 2018년 10월 29일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-349">*Release date: October 29, 2018*</span></span>

<span data-ttu-id="e8eef-350">이 릴리스에는 새 언어 기능과 향상된 개발자 환경이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-350">This release includes new language features and an improved developer experience:</span></span>

* <span data-ttu-id="e8eef-351">이 릴리스에는 Q#용 언어 서버뿐만 아니라 Visual Studio 및 Visual Studio Code용 클라이언트 통합도 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-351">This release includes a language server for Q#, as well as the client integrations for Visual Studio and Visual Studio Code.</span></span> <span data-ttu-id="e8eef-352">이렇게 하면 입력 시 오류 및 경고에 구불구불한 밑줄이 쳐지는 형태로 실시간 피드백을 포함하는 새 IntelliSense 기능 집합을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-352">This enables a new set of IntelliSense features along with live feedback on typing in form of squiggly underlinings of errors and warnings.</span></span> 
* <span data-ttu-id="e8eef-353">이 업데이트는 진단 메시지를 전반적으로 크게 개선합니다. 탐색이 쉬워지고 진단 범위가 정확해지며 가리켜서 표시된 정보에서 추가 정보를 쉽게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-353">This update greatly improves diagnostic messages in general, with easy navigation to and precise ranges for diagnostics and additional details in the displayed hover information.</span></span>
* <span data-ttu-id="e8eef-354">Q# 언어는 개발자가 언어 기능에 대한 일반적인 작업과 새로운 향상 작업을 통합하여 강력한 퀀텀 계산을 수행할 수 있게 하는 방식으로 확장되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-354">The Q# language has been extended in ways that unifies the ways developers can do common operations and new enhancements to the language features to powerfully express quantum computation.</span></span>  <span data-ttu-id="e8eef-355">이 릴리스를 통해 Q# 언어에 몇 가지 주요 변경 사항이 적용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-355">There are a handful of breaking changes to the Q# language with this release.</span></span>   

<span data-ttu-id="e8eef-356">이 릴리스에는 새 퀀텀 화학 라이브러리도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-356">This release also includes a new quantum chemistry library:</span></span>

* <span data-ttu-id="e8eef-357">화학 라이브러리에는 다음과 같은 새로운 Hamiltonian 시뮬레이션 기능이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-357">The chemistry library contains new Hamiltonian simulation features, including:</span></span>
    - <span data-ttu-id="e8eef-358">시뮬레이션 정확성을 향상하는 임의의 짝수 차원의 Trotter–Suzuki 통합자입니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-358">Trotter–Suzuki integrators of arbitrary even order for improved simulation accuracy.</span></span>
    - <span data-ttu-id="e8eef-359">$T$-게이트의 복잡성을 줄이기 위해 화학별 최적화를 사용하는 큐비트화 시뮬레이션 기술입니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-359">Qubitization simulation technique with chemistry-specific optimizations for reducing $T$-gate complexity.</span></span>
* <span data-ttu-id="e8eef-360">분자의 표현을 가져오고 시뮬레이션하는 데 사용할 수 있는 Broombridge 스키마(Hamiltonian의 탄생지로 기념되는 [랜드마크](https://en.wikipedia.org/wiki/Broom_Bridge)에서 딴 이름)라는 새로운 오픈 소스 스키마를 도입했습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-360">A new open source schema, called Broombridge Schema (in reference to a [landmark](https://en.wikipedia.org/wiki/Broom_Bridge) celebrated as a birthplace of Hamiltonians), is introduced for importing representations of molecules and simulating them.</span></span>
* <span data-ttu-id="e8eef-361">Broombridge 스키마를 사용하여 정의된 여러 화학 표현을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-361">Multiple chemical representations defined using the Broombridge Schema are provided.</span></span>  <span data-ttu-id="e8eef-362">이러한 모델은 오픈 소스 고성능 계산 화학 도구인 [NWChem](http://www.nwchem-sw.org/)에 의해 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-362">These models were generated by [NWChem](http://www.nwchem-sw.org/), an open source high-performance computational chemistry tool.</span></span>
* <span data-ttu-id="e8eef-363">자습서 및 샘플에서는 화학 라이브러리 및 Broombridge 데이터 모델을 사용하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-363">Tutorials and Samples describe how to use the chemistry library and the Broombridge data models to:</span></span>
    - <span data-ttu-id="e8eef-364">화학 라이브러리를 사용하여 간단한 Hamiltonian 구성</span><span class="sxs-lookup"><span data-stu-id="e8eef-364">Construct simple Hamiltonians using the chemistry library</span></span>
    - <span data-ttu-id="e8eef-365">단계 추정으로 수소화 리튬의 지반 에너지와 여기 에너지를 시각화합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-365">Visualize ground and excited energies of Lithium Hydride using phase estimation.</span></span>
    - <span data-ttu-id="e8eef-366">퀀텀 화학 시뮬레이션의 리소스 추정 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-366">Perform resource estimates of quantum chemistry simulation.</span></span>
    - <span data-ttu-id="e8eef-367">Broombridge 스키마로 표시되는 분자의 에너지 수준을 추정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-367">Estimate energy levels of molecules represented by the Broombridge schema.</span></span>
* <span data-ttu-id="e8eef-368">설명서에서는 NWChem을 사용하여 Q#로 퀀텀 시뮬레이션용 추가 화학 모델을 생성하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-368">Documentation describes how to use NWChem to generate additional chemical models for quantum simulation with Q#.</span></span>

<span data-ttu-id="e8eef-369">[Quantum Development Kit 화학 라이브러리](xref:microsoft.quantum.chemistry.concepts.intro)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-369">Learn more about the [Quantum Development Kit chemistry library](xref:microsoft.quantum.chemistry.concepts.intro).</span></span>

<span data-ttu-id="e8eef-370">새 화학 라이브러리를 기점으로 라이브러리를 [Microsoft/QuantumLibraries](https://github.com/Microsoft/QuantumLibraries)의 새 GitHub 리포지토리로 분리합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-370">With the new chemistry library, we are separating out the libraries into a new GitHub repo, [Microsoft/QuantumLibraries](https://github.com/Microsoft/QuantumLibraries).</span></span>  <span data-ttu-id="e8eef-371">샘플은 [Microsoft/Quantum](https://github.com/Microsoft/Quantum) 리포지토리에 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-371">The samples remain in the repo [Microsoft/Quantum](https://github.com/Microsoft/Quantum).</span></span>  <span data-ttu-id="e8eef-372">두 리포지토리에 모두 기여해 주셔서 감사합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-372">We welcome contributions to both!</span></span>

<span data-ttu-id="e8eef-373">이 릴리스에는 커뮤니티에서 보고한 이슈에 대한 버그 수정 및 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-373">This release includes bug fixes and features for issues reported by the community:</span></span>

* <span data-ttu-id="e8eef-374">Intellisense for Q#?</span><span class="sxs-lookup"><span data-stu-id="e8eef-374">Intellisense for Q#?</span></span> <span data-ttu-id="e8eef-375">([UserVoice](https://quantum.uservoice.com/forums/906943/suggestions/32656918))</span><span class="sxs-lookup"><span data-stu-id="e8eef-375">([UserVoice](https://quantum.uservoice.com/forums/906943/suggestions/32656918)).</span></span>
* <span data-ttu-id="e8eef-376">.qs 파일([UserVoice](https://quantum.uservoice.com/forums/906097/suggestions/32593049))</span><span class="sxs-lookup"><span data-stu-id="e8eef-376">.qs files ([UserVoice](https://quantum.uservoice.com/forums/906097/suggestions/32593049)).</span></span>
* <span data-ttu-id="e8eef-377">If 문에서 중괄호가 간단히 표시될 때 오류 메시지 개선([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/34718518))</span><span class="sxs-lookup"><span data-stu-id="e8eef-377">Improve error message when curly braces are abbreviated in if statement ([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/34718518)).</span></span>
* <span data-ttu-id="e8eef-378">변경 가능한 (재)바인딩 시 튜플 분해 지원([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/35020444))</span><span class="sxs-lookup"><span data-stu-id="e8eef-378">Support tuple deconstruction at mutable (re-)binding ([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/35020444)).</span></span>
* <span data-ttu-id="e8eef-379">제공된 BitFlipCode를 실행하는 동안 오류 발생([UserVoice](https://quantum.uservoice.com/forums/906940/suggestions/35008546))</span><span class="sxs-lookup"><span data-stu-id="e8eef-379">Error Running Provided BitFlipCode ([UserVoice](https://quantum.uservoice.com/forums/906940/suggestions/35008546)).</span></span>
* <span data-ttu-id="e8eef-380">H2SimulationGUI가 경우에 따라 큰 증가를 표시함([UserVoice](https://quantum.uservoice.com/forums/906946/suggestions/34668370))</span><span class="sxs-lookup"><span data-stu-id="e8eef-380">H2SimulationGUI displays big peaks sometimes ([UserVoice](https://quantum.uservoice.com/forums/906946/suggestions/34668370)).</span></span>

### <a name="community-contributions"></a><span data-ttu-id="e8eef-381">커뮤니티 기여</span><span class="sxs-lookup"><span data-stu-id="e8eef-381">Community Contributions</span></span>

<span data-ttu-id="e8eef-382">**감사합니다.**</span><span class="sxs-lookup"><span data-stu-id="e8eef-382">**Thank you!**</span></span> <span data-ttu-id="e8eef-383">[http://github.com/Microsoft/Quantum](http://github.com/Microsoft/Quantum ) 에서 열려 있는 코드베이스에 기여해 주신 다음 분들께 감사의 말씀을 드립니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-383">to the following contributors to our open code base at http://github.com/Microsoft/Quantum.</span></span> <span data-ttu-id="e8eef-384">이러한 기여는 Q# 코드의 다양한 샘플을 모으는 데 큰 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-384">These contributions add significantly to the rich samples of Q# code:</span></span>

* <span data-ttu-id="e8eef-385">Rolf Huisman([@RolfHuisman](https://github.com/RolfHuisman)): Q# 변환기에 대한 QASM을 만들어 QASM/Q# 개발자의 환경을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-385">Rolf Huisman ([@RolfHuisman](https://github.com/RolfHuisman)): Improved the experience for QASM/Q# developers by creating a QASM to Q# translator.</span></span> <span data-ttu-id="e8eef-386">[PR #58](https://github.com/Microsoft/Quantum/pull/58).</span><span class="sxs-lookup"><span data-stu-id="e8eef-386">[PR #58](https://github.com/Microsoft/Quantum/pull/58).</span></span>

* <span data-ttu-id="e8eef-387">Andrew Helwer([@ahelwer](https://github.com/ahelwer)):  비지역 관련 퀀텀 게임인 CHSH 게임을 구현하는 샘플에 기여했습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-387">Andrew Helwer ([@ahelwer](https://github.com/ahelwer)):  Contributed a sample implementing the CHSH Game, a quantum game related to non-locality.</span></span>  <span data-ttu-id="e8eef-388">[PR #84](https://github.com/Microsoft/Quantum/pull/84).</span><span class="sxs-lookup"><span data-stu-id="e8eef-388">[PR #84](https://github.com/Microsoft/Quantum/pull/84).</span></span>

<span data-ttu-id="e8eef-389">모두를 위해 설명서, 맞춤법 및 오타 수정 작업에 기여하여 콘텐츠를 개선해 주신 Rohit Gupta([@guptarohit](https://github.com/guptarohit),[PR #90](https://github.com/Microsoft/quantum/pull/90)), Tanaka Takayoshi([@tanaka-takayoshi](https://github.com/tanaka-takayoshi),[PR #289](https://github.com/MicrosoftDocs/quantum-docs-pr/pull/289)) 및 Lee James O'Riordan([@mlxd](https://github.com/mlxd),[PR #96](https://github.com/Microsoft/Quantum/pull/96)) 님께도 감사의 말씀을 드립니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-389">Thank you also to Rohit Gupta ([@guptarohit](https://github.com/guptarohit),[PR #90](https://github.com/Microsoft/quantum/pull/90)), Tanaka Takayoshi ([@tanaka-takayoshi](https://github.com/tanaka-takayoshi),[PR #289](https://github.com/MicrosoftDocs/quantum-docs-pr/pull/289)), and Lee James O'Riordan ([@mlxd](https://github.com/mlxd),[PR #96](https://github.com/Microsoft/Quantum/pull/96)) for their work improving the content for all of us through documentation, spelling and typo corrections!</span></span> 

## <a name="version-021809701"></a><span data-ttu-id="e8eef-390">버전 0.2.1809.701</span><span class="sxs-lookup"><span data-stu-id="e8eef-390">Version 0.2.1809.701</span></span>

<span data-ttu-id="e8eef-391">*릴리스 날짜:* 2018년 9월 10일</span><span class="sxs-lookup"><span data-stu-id="e8eef-391">*Release date: September 10, 2018*</span></span>

<span data-ttu-id="e8eef-392">이 릴리스에는 커뮤니티에서 보고한</span><span class="sxs-lookup"><span data-stu-id="e8eef-392">This release includes bug fixes for issues reported by the community.</span></span> <span data-ttu-id="e8eef-393">다음 이슈 등에 대한 버그 수정이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-393">Including:</span></span>

* <span data-ttu-id="e8eef-394">시프트 연산자를 사용할 수 없음([GitHub](https://github.com/Microsoft/Quantum/issues/75))</span><span class="sxs-lookup"><span data-stu-id="e8eef-394">Unable to use shift operator ([GitHub](https://github.com/Microsoft/Quantum/issues/75)).</span></span>
* <span data-ttu-id="e8eef-395">`DumpMachine` / `DumpRegister`가 콘솔에 인쇄될 때 `QCTraceSimulator`에서 실패함([UserVoice](https://quantum.uservoice.com/forums/906946/suggestions/34709680))</span><span class="sxs-lookup"><span data-stu-id="e8eef-395">`DumpMachine` / `DumpRegister` fails on `QCTraceSimulator` when printing to console ([UserVoice](https://quantum.uservoice.com/forums/906946/suggestions/34709680)).</span></span>
* <span data-ttu-id="e8eef-396">0큐비트 할당 허용([UserVoice](https://quantum.uservoice.com/forums/906208-q-language/suggestions/34768069-allow-allocating-0-qubits))</span><span class="sxs-lookup"><span data-stu-id="e8eef-396">Allow allocating 0 qubits ([UserVoice](https://quantum.uservoice.com/forums/906208-q-language/suggestions/34768069-allow-allocating-0-qubits)).</span></span>
* <span data-ttu-id="e8eef-397">`AssertQubitState`에 명시적 Complex() 호출이 필요함([UserVoice](https://quantum.uservoice.com/forums/906208-q-language/suggestions/34713733-assertqubitstate-requires-explicit-complex-call))</span><span class="sxs-lookup"><span data-stu-id="e8eef-397">`AssertQubitState` requires explicit Complex() call ([UserVoice](https://quantum.uservoice.com/forums/906208-q-language/suggestions/34713733-assertqubitstate-requires-explicit-complex-call)).</span></span>
* <span data-ttu-id="e8eef-398">`Measure` 작업이 macOS에서 항상 `One`을 반환함([UserVoice](https://quantum.uservoice.com/forums/906940/suggestions/35008546))</span><span class="sxs-lookup"><span data-stu-id="e8eef-398">`Measure` operation always returns `One` on macOS ([UserVoice](https://quantum.uservoice.com/forums/906940/suggestions/35008546)).</span></span>

<span data-ttu-id="e8eef-399">감사합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-399">Thanks!</span></span> 

## <a name="version-0218063001"></a><span data-ttu-id="e8eef-400">버전 0.2.1806.3001</span><span class="sxs-lookup"><span data-stu-id="e8eef-400">Version 0.2.1806.3001</span></span>

<span data-ttu-id="e8eef-401">*릴리스 날짜: 2018년 6월 30일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-401">*Release date: June 30, 2018*</span></span>

<span data-ttu-id="e8eef-402">이 릴리스는 [GitHub에 보고된 이슈 #48](https://github.com/Microsoft/Quantum/issues/48)에 대한 빠른 수정입니다(사용자 이름에 공백이 포함된 경우 Q# 컴파일이 실패함).</span><span class="sxs-lookup"><span data-stu-id="e8eef-402">This releases is just a quick fix for [issue #48 reported on GitHub](https://github.com/Microsoft/Quantum/issues/48) (Q# compilation fails if user name contains a blank space).</span></span> <span data-ttu-id="e8eef-403">해당하는 새 버전(`0.2.1806.3001-preview`)이 포함된 `0.2.1806.1503`과 같은 업데이트 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-403">Follow same update instructions as `0.2.1806.1503` with the corresponding new version (`0.2.1806.3001-preview`).</span></span>

## <a name="version-0218061503"></a><span data-ttu-id="e8eef-404">버전 0.2.1806.1503</span><span class="sxs-lookup"><span data-stu-id="e8eef-404">Version 0.2.1806.1503</span></span>

<span data-ttu-id="e8eef-405">*릴리스 날짜: 2018년 6월 22일*</span><span class="sxs-lookup"><span data-stu-id="e8eef-405">*Release date: June 22, 2018*</span></span>

<span data-ttu-id="e8eef-406">이 릴리스에는 향상된 디버깅 환경 및 향상된 성능뿐 아니라 다양한 커뮤니티 기여도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-406">This release includes several community contributions as well as an improved debugging experience and improved performance.</span></span>  <span data-ttu-id="e8eef-407">특히 다음에 대한 내용을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-407">Specifically:</span></span>

* <span data-ttu-id="e8eef-408">QuantumSimulator 대상 머신에 대한 작고 큰 시뮬레이션에서 모두 성능이 향상됨</span><span class="sxs-lookup"><span data-stu-id="e8eef-408">Performance improvements on both small and large simulations for the QuantumSimulator target machine.</span></span>
* <span data-ttu-id="e8eef-409">향상된 디버깅 기능</span><span class="sxs-lookup"><span data-stu-id="e8eef-409">Improved debugging functionality.</span></span>
* <span data-ttu-id="e8eef-410">버그 수정, 새 도우미 함수, 작업 및 새 샘플의 커뮤니티 기여</span><span class="sxs-lookup"><span data-stu-id="e8eef-410">Community contributions in bug fixes, new helper functions, operations and new samples.</span></span>

### <a name="performance-improvements"></a><span data-ttu-id="e8eef-411">성능 향상</span><span class="sxs-lookup"><span data-stu-id="e8eef-411">Performance improvements</span></span>

<span data-ttu-id="e8eef-412">이 업데이트에는 모든 머신에서 많고 적은 큐비트의 상당한 성능 향상이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-412">This update includes significant performance improvements for simulation of large and small numbers of qubits for all the target machines.</span></span>  <span data-ttu-id="e8eef-413">이 향상된 기능은 Quantum Development Kit에서 표준 샘플인 H<sub>2</sub> 시뮬레이션을 사용하여 쉽게 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-413">This improvement is easily visible with the H<sub>2</sub> simulation that is a standard sample in the Quantum Development Kit.</span></span>

### <a name="improved-debugging-functionality"></a><span data-ttu-id="e8eef-414">향상된 디버깅 기능</span><span class="sxs-lookup"><span data-stu-id="e8eef-414">Improved debugging functionality</span></span>

<span data-ttu-id="e8eef-415">이 업데이트는 다음과 같은 새 디버깅 기능을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-415">This update adds new debugging functionality:</span></span>
* <span data-ttu-id="e8eef-416">특정 시점에 대상 퀀텀 머신에 대한 wave 함수 정보를 출력하는 두 개의 새 작업 @"microsoft.quantum.extensions.diagnostics.dumpmachine" 및 @"microsoft.quantum.extensions.diagnostics.dumpregister"를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-416">Added two new operations,  @"microsoft.quantum.extensions.diagnostics.dumpmachine" and @"microsoft.quantum.extensions.diagnostics.dumpregister" that output wave function information about the target quantum machine at a point in time.</span></span>  
* <span data-ttu-id="e8eef-417">Visual Studio에서는 단일 큐비트에서 $\ket{1}$를 측정할 확률이 이제 QuantumSimulator 대상 머신의 디버깅 창에 자동으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-417">In Visual Studio, the probability of measuring a $\ket{1}$ on a single qubit is now automatically shown in the debugging window for the QuantumSimulator target machine.</span></span>
* <span data-ttu-id="e8eef-418">Visual Studio에서는 **Autos** 및 **Locals** 디버그 창에서 변수 속성 표시가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-418">In Visual Studio, improved the display of variable properties in the **Autos** and **Locals** debug windows.</span></span> 

<span data-ttu-id="e8eef-419">[테스트 및 디버깅](xref:microsoft.quantum.guide.testingdebugging)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-419">Learn more about [Testing and Debugging](xref:microsoft.quantum.guide.testingdebugging).</span></span>

### <a name="community-contributions"></a><span data-ttu-id="e8eef-420">커뮤니티 기여</span><span class="sxs-lookup"><span data-stu-id="e8eef-420">Community Contributions</span></span>

<span data-ttu-id="e8eef-421">Q# 코더 커뮤니티는 성장하고 있으며 http://github.com/Microsoft/quantum 에서 열려 있는 코드베이스에 제출된 첫 번째 사용자가 라이브러리 및 샘플에 기여해 주셔서 감사합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-421">The Q# coder community is growing and we are thrilled to see the first user contributed libraries and samples that were submitted to our open code base at http://github.com/Microsoft/quantum.</span></span>  <span data-ttu-id="e8eef-422">**다음 기여자분들께**</span><span class="sxs-lookup"><span data-stu-id="e8eef-422">**A big Thank you!**</span></span> <span data-ttu-id="e8eef-423">깊은 감사의 말씀을 드립니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-423">to the following contributors:</span></span>
* <span data-ttu-id="e8eef-424">Mathias Soeken([@msoeken](https://github.com/msoeken)): 지정된 순열을 구현하도록 Toffoli 네트워크를 생성하는 변환 기반 논리 합성 메서드를 정의하는 샘플에 기여했습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-424">Mathias Soeken ([@msoeken](https://github.com/msoeken)):  contributed a sample defining a transformation based logic synthesis method that constructs Toffoli networks to implement a given permutation.</span></span> <span data-ttu-id="e8eef-425">이 코드는 전체적으로 Q# 함수 및 작업으로 작성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-425">The code is written entirely in Q# functions and operations.</span></span>  <span data-ttu-id="e8eef-426">[PR #41](https://github.com/Microsoft/Quantum/pull/41).</span><span class="sxs-lookup"><span data-stu-id="e8eef-426">[PR #41](https://github.com/Microsoft/Quantum/pull/41).</span></span>
* <span data-ttu-id="e8eef-427">RolfHuisman([@RolfHuisman](https://github.com/RolfHuisman)): Microsoft MVP Rolf Huisman은 클래식 제어 흐름 및 제한된 퀀텀 작업이 포함되지 않은 제한된 프로그램 클래스에 대한 Q# 코드에서 플랫 QASM 코드를 생성하는 샘플에 기여했습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-427">RolfHuisman ([@RolfHuisman](https://github.com/RolfHuisman)): Microsoft MVP Rolf Huisman contributed a sample that generates flat QASM code from Q# code for a restricted class of programs that do not have classical control flow and restricted quantum operations.</span></span> [<span data-ttu-id="e8eef-428">PR #59</span><span class="sxs-lookup"><span data-stu-id="e8eef-428">PR #59</span></span>](https://github.com/Microsoft/Quantum/pull/59)
* <span data-ttu-id="e8eef-429">Sarah Kasier([@crazy4pi314](https://github.com/crazy4pi314)): 제어된 작업에 대한 라이브러리 함수를 제출하여 코드베이스를 개선하도록 도왔습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-429">Sarah Kasier ([@crazy4pi314](https://github.com/crazy4pi314)): helped to improve our code base by submitting a library function for controlled operations.</span></span> [<span data-ttu-id="e8eef-430">PR #53</span><span class="sxs-lookup"><span data-stu-id="e8eef-430">PR #53</span></span>](https://github.com/Microsoft/Quantum/pull/53)
* <span data-ttu-id="e8eef-431">Jessica Lemieux([@Lemj3111](https://github.com/Lemj3111)): @"microsoft.quantum.canon.quantumphaseestimation"을 수정하고 새 단위 테스트를 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-431">Jessica Lemieux ([@Lemj3111](https://github.com/Lemj3111)): fixed @"microsoft.quantum.canon.quantumphaseestimation" and created new unit tests.</span></span>  [<span data-ttu-id="e8eef-432">PR #54</span><span class="sxs-lookup"><span data-stu-id="e8eef-432">PR #54</span></span>](https://github.com/Microsoft/Quantum/pull/54)
* <span data-ttu-id="e8eef-433">Tama McGlinn([@TamaHobbit](https://github.com/TamaHobbit)): QuantumSimulator 인스턴스가 삭제되었는지 확인하여 Teleportation 샘플을 정리했습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-433">Tama McGlinn ([@TamaHobbit](https://github.com/TamaHobbit)): cleaned the Teleportation sample by making sure the QuantumSimulator instance is disposed.</span></span> [<span data-ttu-id="e8eef-434">PR #20</span><span class="sxs-lookup"><span data-stu-id="e8eef-434">PR #20</span></span>](https://github.com/Microsoft/Quantum/pull/20)

<span data-ttu-id="e8eef-435">또한 큰 **감사 합니다.**</span><span class="sxs-lookup"><span data-stu-id="e8eef-435">Additionally, a big **Thank You!**</span></span> <span data-ttu-id="e8eef-436">Commercial Engineering Services 팀의 기여자로서 Hackathon이 진행되는 동안 설명서에 중요한 변경 내용을 제공해 주신 다음 Microsoft 소프트웨어 엔지니어분들께도 깊은 감사의 말씀을 드립니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-436">to these Microsoft Software Engineers from the Commercial Engineering Services team contributors who made valuable changes to our documentation during their Hackathon.</span></span>  <span data-ttu-id="e8eef-437">해당 변경 내용은 모두를 위한 설명 및 온보딩 환경을 크게 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-437">Their changes vastly improved the clarity and onboarding experience for all of us:</span></span>
* <span data-ttu-id="e8eef-438">Sascha Corti</span><span class="sxs-lookup"><span data-stu-id="e8eef-438">Sascha Corti</span></span>
* <span data-ttu-id="e8eef-439">Mihaela Curmei</span><span class="sxs-lookup"><span data-stu-id="e8eef-439">Mihaela Curmei</span></span>
* <span data-ttu-id="e8eef-440">John Donnelly</span><span class="sxs-lookup"><span data-stu-id="e8eef-440">John Donnelly</span></span>
* <span data-ttu-id="e8eef-441">Kirill Logachev</span><span class="sxs-lookup"><span data-stu-id="e8eef-441">Kirill Logachev</span></span>
* <span data-ttu-id="e8eef-442">Jan Pospisil</span><span class="sxs-lookup"><span data-stu-id="e8eef-442">Jan Pospisil</span></span>
* <span data-ttu-id="e8eef-443">Anita Ramanan</span><span class="sxs-lookup"><span data-stu-id="e8eef-443">Anita Ramanan</span></span>
* <span data-ttu-id="e8eef-444">Frances Tibble</span><span class="sxs-lookup"><span data-stu-id="e8eef-444">Frances Tibble</span></span>
* <span data-ttu-id="e8eef-445">Alessandro Vozza</span><span class="sxs-lookup"><span data-stu-id="e8eef-445">Alessandro Vozza</span></span>

### <a name="update-existing-projects"></a><span data-ttu-id="e8eef-446">기존 프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="e8eef-446">Update existing projects</span></span>

<span data-ttu-id="e8eef-447">이 릴리스는 이전 버전과 완벽하게 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-447">This release is fully backwards compatible.</span></span> <span data-ttu-id="e8eef-448">프로젝트의 nuget 패키지를 버전 `0.2.1806.1503-preview`로 업데이트하고 모든 중간 파일이 다시 생성되도록 **전체 다시 빌드**를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-448">Just update the nuget pakages in your projects to version `0.2.1806.1503-preview` and do a **full rebuild** to make sure all intermediate files are regenerated.</span></span>

<span data-ttu-id="e8eef-449">Visual Studio에서 [패키지 업데이트](https://docs.microsoft.com/nuget/tools/package-manager-ui#updating-a-package) 방법에 대한 일반적인 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-449">From Visual Studio, follow the normal instructions on how to [update a package](https://docs.microsoft.com/nuget/tools/package-manager-ui#updating-a-package).</span></span>

<span data-ttu-id="e8eef-450">명령줄에 대한 프로젝트 템플릿을 업데이트하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-450">To update project templates for the command line, run the following command:</span></span>
```
dotnet new -i "Microsoft.Quantum.ProjectTemplates::0.2.1806.1503-preview"
```

<span data-ttu-id="e8eef-451">이 명령을 실행한 후 `dotnet new <project-type> -lang Q#`을 사용하여 생성된 새 프로젝트는 자동으로 이 버전의 Quantum Development Kit를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-451">After running this command, any new projects created using `dotnet new <project-type> -lang Q#` will automatically use this version of the Quantum Development Kit.</span></span>

<span data-ttu-id="e8eef-452">최신 버전을 사용하도록 기존 프로젝트를 업데이트하려면 각 프로젝트의 디렉터리 내에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-452">To update an existing project to use the newest version, run the following command from within the directory for each project:</span></span>

```
dotnet add package Microsoft.Quantum.Development.Kit -v "0.2.1806.1503-preview"
dotnet add package Microsoft.Quantum.Canon -v "0.2.1806.1503-preview"
```

<span data-ttu-id="e8eef-453">또한 기존 프로젝트에서 유닛 테스트에 XUnit 통합을 사용하는 경우 유사한 명령을 사용하여 해당 패키지를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-453">If an existing project also uses XUnit integration for unit testing, then a similar command can be used to update that package as well:</span></span>
```
dotnet add package Microsoft.Quantum.Xunit -v "0.2.1806.1503-preview"
```

<span data-ttu-id="e8eef-454">테스트 프로젝트에서 사용하는 XUnit 버전에 따라 XUnit을 2.3.1로 업데이트해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-454">Depending on the version of XUnit that your test project uses, you may also need to update XUnit to 2.3.1:</span></span>
```
dotnet add package xunit -v "2.3.1" 
```

<span data-ttu-id="e8eef-455">업데이트한 후에는 다음을 수행하여 이전 버전에서 생성된 모든 임시 파일을 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-455">After the update, make sure you remove all temporary files generated by the previous version by doing:</span></span>
```
dotnet clean 
```

### <a name="known-issues"></a><span data-ttu-id="e8eef-456">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="e8eef-456">Known Issues</span></span>

<span data-ttu-id="e8eef-457">보고할 알려진 추가 이슈가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-457">No aditional known issues to report.</span></span>


## <a name="version-0218022202"></a><span data-ttu-id="e8eef-458">버전 0.2.1802.2202</span><span class="sxs-lookup"><span data-stu-id="e8eef-458">Version 0.2.1802.2202</span></span>

<span data-ttu-id="e8eef-459">*릴리스 날짜:* 2018년 2월 26일</span><span class="sxs-lookup"><span data-stu-id="e8eef-459">*Release date: February 26, 2018*</span></span>

<span data-ttu-id="e8eef-460">이 릴리스에서는 더 많은 플랫폼, 언어 상호 운용성 및 성능 향상에 대한 개발을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-460">This release brings support for development on more platforms, language interoperability, and performance enhancements.</span></span> <span data-ttu-id="e8eef-461">특히 다음에 대한 내용을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-461">Specifically:</span></span>

- <span data-ttu-id="e8eef-462">macOS 및 Linux 기반 개발 지원</span><span class="sxs-lookup"><span data-stu-id="e8eef-462">Support for macOS- and Linux-based development.</span></span> 
- <span data-ttu-id="e8eef-463">플랫폼 간 Visual Studio Code 지원을 포함한 .NET Core 호환성</span><span class="sxs-lookup"><span data-stu-id="e8eef-463">.NET Core compatibility, including support for Visual Studio Code across platforms.</span></span>
- <span data-ttu-id="e8eef-464">Quantum Development Kit 라이브러리의 전체 오픈 소스 라이선스</span><span class="sxs-lookup"><span data-stu-id="e8eef-464">A full Open Source license for the Quantum Development Kit Libraries.</span></span>
- <span data-ttu-id="e8eef-465">20개 이상의 큐비트가 필요한 프로젝트에서 시뮬레이터 성능을 개선함</span><span class="sxs-lookup"><span data-stu-id="e8eef-465">Improved simulator performance on projects requiring 20 or more qubits.</span></span>
- <span data-ttu-id="e8eef-466">Python 언어와 상호 운용성(Windows에서 사용할 수 있는 미리 보기 릴리스)</span><span class="sxs-lookup"><span data-stu-id="e8eef-466">Interoperability with the Python language (preview release available on Windows).</span></span>

### <a name="net-editions"></a><span data-ttu-id="e8eef-467">.NET 버전</span><span class="sxs-lookup"><span data-stu-id="e8eef-467">.NET Editions</span></span>

<span data-ttu-id="e8eef-468">.NET 플랫폼은 두 가지 버전인, Windows와 함께 제공되는 .NET Framework 및 Windows, macOS 및 Linux에서 사용 가능한 오픈 소스 .NET Core를 통해 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-468">The .NET platform is available through two different editions, the .NET Framework that is provided with Windows, and the open-source .NET Core that is available on Windows, macOS and Linux.</span></span>
<span data-ttu-id="e8eef-469">이 릴리스에서는 대부분의 Quantum Development Kit 부분이 Framework 및 Core에 공통적인 클래스 세트인 .NET Standard용 라이브러리로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-469">With this release, most parts of the Quantum Development Kit are provided as libraries for .NET Standard, the set of classes common to both Framework and Core.</span></span>
<span data-ttu-id="e8eef-470">따라서 이 라이브러리는 최신 버전의 .NET Framework 또는 .NET Core와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-470">These libraries are therefore compatible with recent versions of either .NET Framework or .NET Core.</span></span>

<span data-ttu-id="e8eef-471">따라서 Quantum Development Kit를 사용하여 작성된 프로젝트를 최대한 이식 가능하게 하려면 Quantum Development Kit를 사용하여 작성된 라이브러리 프로젝트의 대상을 .NET Standard로 지정하지만 콘솔 애플리케이션의 대상을 .NET Core로 지정하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-471">Thus, to help ensure that projects written using the Quantum Development Kit are as portable as possible, we recommend that library projects written using the Quantum Development Kit target .NET Standard, while console applications target .NET Core.</span></span>
<span data-ttu-id="e8eef-472">이전 릴리스의 Quantum Development Kit는 .NET Framework만 지원했으므로 기존 프로젝트를 마이그레이션해야 할 수 있습니다. 이 작업을 수행하는 방법에 대한 자세한 내용은 아래를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-472">Since previous releases of the Quantum Development Kit only supported .NET Framework, you may need to migrate your existing projects; see below for details on how to do this.</span></span>

### <a name="project-migration"></a><span data-ttu-id="e8eef-473">프로젝트 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="e8eef-473">Project Migration</span></span>

<span data-ttu-id="e8eef-474">이전 버전의 Quantum Development Kit를 사용하여 만든 프로젝트에서 사용된 NuGet 패키지를 업데이트하지 않는 한 해당 프로젝트는 계속 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-474">Projects created using previous versions of Quantum Development Kit will still work, as long as you don't update the NuGet packages used in them.</span></span> <span data-ttu-id="e8eef-475">기존 코드를 새 버전으로 마이그레이션하려면 다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-475">To migrate existing code to the new version, perform the following steps:</span></span>
1. <span data-ttu-id="e8eef-476">올바른 형식의 Q# 프로젝트 템플릿(애플리케이션, 라이브러리 또는 테스트 프로젝트)을 사용하여 새 .NET Core 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-476">Create a new .NET Core project using the right type of Q# project template (Application, Library or Test Project).</span></span>
2. <span data-ttu-id="e8eef-477">이전 프로젝트에서 새 프로젝트로 기존 .qs 및 .cs/.fs 파일을 복사합니다([추가] > [기존 항목] 사용).</span><span class="sxs-lookup"><span data-stu-id="e8eef-477">Copy existing .qs and .cs/.fs files from the old project to the new project (using Add > Existing Item).</span></span> <span data-ttu-id="e8eef-478">AssemblyInfo.cs 파일을 복사하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-478">Do not copy the AssemblyInfo.cs file.</span></span>
3. <span data-ttu-id="e8eef-479">새 프로젝트를 빌드하고 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-479">Build and run the new project.</span></span>

<span data-ttu-id="e8eef-480">Microsoft.Quantum.Canon 네임스페이스의 RandomWalkPhaseEstimation 작업은 [Microsoft/Quantum-NC](https://github.com/microsoft/quantum-nc) 리포지토리의 Microsoft.Research.Quantum.RandomWalkPhaseEstimation 네임스페이스로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-480">Please note that the operation RandomWalkPhaseEstimation from the namespace Microsoft.Quantum.Canon was moved into the namespace Microsoft.Research.Quantum.RandomWalkPhaseEstimation in the [Microsoft/Quantum-NC](https://github.com/microsoft/quantum-nc) repository.</span></span>

### <a name="known-issues"></a><span data-ttu-id="e8eef-481">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="e8eef-481">Known Issues</span></span>

- <span data-ttu-id="e8eef-482">Q#으로 작성된 테스트에서는 `--filter`에 대한 `dotnet test` 옵션이 제대로 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-482">The `--filter` option to `dotnet test` does not work correctly for tests written in Q#.</span></span>
  <span data-ttu-id="e8eef-483">따라서 Visual Studio Code에서 개별 단위 테스트를 실행할 수 없습니다. 명령줄에서 `dotnet test`를 사용하여 모든 테스트를 다시 실행하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-483">As a result, individual unit tests cannot be run in Visual Studio Code; we recommend using `dotnet test` at the command line to re-run all tests.</span></span>

## <a name="version-0118011707"></a><span data-ttu-id="e8eef-484">버전 0.1.1801.1707</span><span class="sxs-lookup"><span data-stu-id="e8eef-484">Version 0.1.1801.1707</span></span>

<span data-ttu-id="e8eef-485">*릴리스 날짜:* 2018년 1월 18일</span><span class="sxs-lookup"><span data-stu-id="e8eef-485">*Release date: January 18, 2018*</span></span>

<span data-ttu-id="e8eef-486">이 릴리스에서는 커뮤니티에서 보고한 일부 이슈를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-486">This release fixes some issues reported by the community.</span></span> <span data-ttu-id="e8eef-487">구체적으로는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-487">Namely:</span></span>

- <span data-ttu-id="e8eef-488">이제 시뮬레이터는 초기 AVX 사용 가능 CPU 이외의 CPU를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-488">The simulator now works with early non-AVX-enabled CPUs.</span></span>
- <span data-ttu-id="e8eef-489">국가별 10진수 설정으로 인해 Q# 파서가 실패하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-489">Regional decimal settings will not cause the Q# parser to fail.</span></span>
- <span data-ttu-id="e8eef-490">`SignD` 기본 작업은 이제 `Double`이 아닌 `Int`을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-490">`SignD` primitive operation now returns `Int` rather than `Double`.</span></span>


## <a name="version-011712901"></a><span data-ttu-id="e8eef-491">버전 0.1.1712.901</span><span class="sxs-lookup"><span data-stu-id="e8eef-491">Version 0.1.1712.901</span></span>

<span data-ttu-id="e8eef-492">*릴리스 날짜:* 2017년 12월 11일</span><span class="sxs-lookup"><span data-stu-id="e8eef-492">*Release date: December 11, 2017*</span></span>

### <a name="known-issues"></a><span data-ttu-id="e8eef-493">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="e8eef-493">Known Issues</span></span>

#### <a name="hardware-and-software-requirements"></a><span data-ttu-id="e8eef-494">하드웨어 및 소프트웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="e8eef-494">Hardware and Software Requirements</span></span>

- <span data-ttu-id="e8eef-495">Quantum Development Kit에 포함된 시뮬레이터를 사용하려면 Microsoft Windows의 64비트 설치를 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-495">The simulator included with the Quantum Development Kit requires a 64-bit installation of Microsoft Windows to run.</span></span>
- <span data-ttu-id="e8eef-496">Quantum Development Kit와 함께 설치되는 Microsoft의 퀀텀 시뮬레이터에서는 AVX(고급 벡터 확장)를 활용하며 AVX 사용 가능 CPU가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-496">Microsoft's quantum simulator, installed with the Quantum Development Kit, utilizes Advanced Vector Extensions (AVX), and requires an AVX-enabled CPU.</span></span> <span data-ttu-id="e8eef-497">Q1 2011(Sandy Bridge) 이상에서 제공되는 Intel 프로세서는 AVX를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-497">Intel processors shipped in Q1 2011 (Sandy Bridge) or later support AVX.</span></span> <span data-ttu-id="e8eef-498">초기 CPU에 대한 지원을 평가하고 나중에 세부 정보를 발표할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-498">We are evaluating support for earlier CPUs and may announce details at a later time.</span></span>

#### <a name="project-creation"></a><span data-ttu-id="e8eef-499">프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="e8eef-499">Project Creation</span></span>

- <span data-ttu-id="e8eef-500">Q#을 사용할 솔루션(.sln)을 만드는 경우 이 솔루션은 솔루션의 각 프로젝트(.csproj) 보다 높은 수준의 단일 디렉터리여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-500">When creating a solution (.sln) that will use Q#, the solution must be one directory higher than each project (.csproj) in the solution.</span></span> <span data-ttu-id="e8eef-501">새 솔루션을 만드는 경우 “새 프로젝트” 대화 상자에서 “솔루션용 디렉터리 만들기” 확인란이 선택되었는지 확인하여 이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-501">When creating a new solution, this can be accomplished by making sure that the "Create directory for solution" checkbox on the "New Project" dialog box is checked.</span></span> <span data-ttu-id="e8eef-502">이 작업을 수행하지 않으면 Quantum Development Kit NuGet 패키지를 수동으로 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-502">If this is not done, the Quantum Development Kit NuGet packages will need to be installed manually.</span></span>

#### <a name="q"></a><span data-ttu-id="e8eef-503">Q#</span><span class="sxs-lookup"><span data-stu-id="e8eef-503">Q#</span></span>

- <span data-ttu-id="e8eef-504">Intellisense는 Q# 코드에 대한 적절한 오류를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-504">Intellisense does not display proper errors for Q# code.</span></span> <span data-ttu-id="e8eef-505">올바른 Q# 오류를 보려면 Visual Studio 오류 목록에 빌드 오류가 표시되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-505">Make sure that you are displaying Build errors in the Visual Studio Error List to see correct Q# errors.</span></span> <span data-ttu-id="e8eef-506">또한 빌드를 완료한 후에도 Q# 오류는 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-506">Also note that Q# errors will not show up until after you've done a build.</span></span>
- <span data-ttu-id="e8eef-507">부분 애플리케이션에서 변경 가능한 배열을 사용하면 예기치 않은 동작이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-507">Using a mutable array in a partial application may lead to unexpected behavior.</span></span>
- <span data-ttu-id="e8eef-508">변경할 수 없는 배열을 변경 가능한 배열에 바인딩하면(a = b로 설정, 여기서 b는 변경 가능한 배열) 예기치 않은 동작이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-508">Binding an immutable array to a mutable array (let a = b, where b is a mutable array) may lead to unexpected behavior.</span></span>
- <span data-ttu-id="e8eef-509">프로파일링, 코드 검사 및 기타 VS 플러그 인이 항상 Q# 줄 및 블록을 정확하게 계산하는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-509">Profiling, code coverage and other VS plugins may not always count Q# lines and blocks accurately.</span></span>
- <span data-ttu-id="e8eef-510">Q# 컴파일러는 보간된 문자열의 유효성을 검사하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-510">The Q# compiler does not validate interpolated strings.</span></span> <span data-ttu-id="e8eef-511">Q# 보간된 문자열에서 식을 사용하거나 철자가 잘못된 변수 이름을 사용하여 C# 컴파일 오류를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-511">It is possible to create C# compilation errors by misspelling variable names or using expressions in Q# interpolated strings.</span></span>

#### <a name="simulation"></a><span data-ttu-id="e8eef-512">시뮬레이션</span><span class="sxs-lookup"><span data-stu-id="e8eef-512">Simulation</span></span>

- <span data-ttu-id="e8eef-513">퀀텀 시뮬레이터는 OpenMP를 사용하여 필요한 선형 대수를 병렬로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-513">The Quantum Simulator uses OpenMP to parallelize the linear algebra required.</span></span> <span data-ttu-id="e8eef-514">기본적으로 OpenMP는 사용 가능한 모든 하드웨어 스레드를 사용합니다. 즉, 필요한 조정이 실제 작업을 방해하기 때문에 적은 수의 큐비트를 포함하는 프로그램이 느리게 실행되는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-514">By default OpenMP uses all available hardware threads, which means that programs with small numbers of qubits will often run slowly because the coordination required will dwarf the actual work.</span></span> <span data-ttu-id="e8eef-515">환경 변수 OMP_NUM_THREADS를 작은 수로 설정하여 이 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-515">This can be fixed by setting the environment variable OMP_NUM_THREADS to a small number.</span></span> <span data-ttu-id="e8eef-516">대략적으로 스레드 1개는 최대 4개 정도의 큐비트에 적합하며 알고리즘에 따라 많이 달라지지만 큐비트당 추가 스레드가 적합합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-516">As a very rough rule of thumb, 1 thread is good for up to about 4 qubits, and then an additional thread per qubit is good, although this is highly dependent on your algorithm.</span></span>

#### <a name="debugging"></a><span data-ttu-id="e8eef-517">디버깅</span><span class="sxs-lookup"><span data-stu-id="e8eef-517">Debugging</span></span>

- <span data-ttu-id="e8eef-518">F11(한 단계씩 코드 실행)은 Q# 코드에서 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-518">F11 (step in) doesn't work in Q# code.</span></span>
- <span data-ttu-id="e8eef-519">중단점 및 단일 단계 일시 중지에서 Q# 코드의 코드 강조 표시는 정확하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-519">Code highlighting in Q# code at a breakpoint or single-step pause is sometimes inaccurate.</span></span> <span data-ttu-id="e8eef-520">올바른 줄이 강조 표시되지만 때때로 강조 표시가 줄의 잘못된 열에서 시작 및 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-520">The correct line will be highlighted, but sometimes the highlight will start and end at incorrect columns on the line.</span></span>

#### <a name="testing"></a><span data-ttu-id="e8eef-521">테스트</span><span class="sxs-lookup"><span data-stu-id="e8eef-521">Testing</span></span>

- <span data-ttu-id="e8eef-522">테스트는 64비트 모드로 실행되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-522">Tests must be executed in 64-bit mode.</span></span> <span data-ttu-id="e8eef-523">BadImageFormatException으로 인해 테스트에 실패한 경우 [테스트] 메뉴로 이동하고 [테스트 설정] > [기본 프로세서 아키텍처] > [X64]를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-523">If your tests are failing with a BadImageFormatException, go to the Test menu and select Test Settings > Default Processor Architecture > X64.</span></span>
- <span data-ttu-id="e8eef-524">일부 테스트는 실행하는 데 오랜 시간이 걸립니다(컴퓨터에 따라 5분 정도 걸릴 수 있음).</span><span class="sxs-lookup"><span data-stu-id="e8eef-524">Some tests take a long time (possibly as much as 5 minutes depending on your computer) to run.</span></span> <span data-ttu-id="e8eef-525">일부 테스트에서는 20개 이상의 큐비트를 사용하므로 정상적인 상황입니다. 현재 가장 큰 테스트는 23개의 큐비트에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-525">This is normal, as some use over twenty qubits; our largest test currently runs on 23 qubits.</span></span>

#### <a name="samples"></a><span data-ttu-id="e8eef-526">샘플</span><span class="sxs-lookup"><span data-stu-id="e8eef-526">Samples</span></span>

- <span data-ttu-id="e8eef-527">일부 머신에서는 환경 변수 OMP_NUM_THREADS가 “1”로 설정된 경우가 아니면 일부 작은 샘플이 느리게 실행될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-527">On some machines, some small samples may run slowly unless the environment variable OMP_NUM_THREADS is set to "1".</span></span> <span data-ttu-id="e8eef-528">또한 “시뮬레이션”에서 릴리스 정보를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8eef-528">See also the release note under "Simulation".</span></span>

#### <a name="libraries"></a><span data-ttu-id="e8eef-529">라이브러리</span><span class="sxs-lookup"><span data-stu-id="e8eef-529">Libraries</span></span>

- <span data-ttu-id="e8eef-530">서로 다른 인수로 작업에 전달된 큐비트는 모두 개별 큐비트라고 암시적으로 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-530">There is an implicit assumption that the qubits passed to an operation in different arguments are all distinct.</span></span> <span data-ttu-id="e8eef-531">예를 들어 모든 라이브러리 작업(및 모든 시뮬레이터)은 제어된 NOT에 전달된 두 개의 큐비트는 서로 다른 큐비트라고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-531">For instance, all of the library operations (and all of the simulators) assume that the two qubits passed to a controlled NOT are different qubits.</span></span> <span data-ttu-id="e8eef-532">이 가정에 위배되면 예기치 않은 결과가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-532">Violating this assumption may lead to unpredictable unexpected.</span></span> <span data-ttu-id="e8eef-533">퀀텀 컴퓨터 추적 프로그램 시뮬레이터를 사용하여 이를 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-533">It is possible to test for this using the quantum computer tracer simulator.</span></span>
- <span data-ttu-id="e8eef-534">Microsoft.Quantum.Bind 함수는 경우에 따라 예상대로 작동하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-534">The Microsoft.Quantum.Bind function may not act as expected in all cases.</span></span>
- <span data-ttu-id="e8eef-535">Microsoft.Quantum.Extensions.Math 네임스페이스에서 SignD 함수는 Int가 아니라 Double을 반환합니다. 단, 기본 System.Math.Sign 함수는 항상 정수를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-535">In the Microsoft.Quantum.Extensions.Math namespace, the SignD function returns a Double rather than an Int, although the underlying System.Math.Sign function always returns an integer.</span></span> <span data-ttu-id="e8eef-536">이 double은 모두 정확한 이진 표현을 포함하므로 1.0, -1.0 및 0.0에 결과를 비교하는 것이 안전합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eef-536">It is safe to compare the result against 1.0, -1.0, and 0.0, since these doubles all have exact binary representations.</span></span>
