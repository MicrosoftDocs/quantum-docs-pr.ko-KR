---
title: Quantum Development Kit 미리 보기 릴리스 정보
description: Quantum Development Kit 미리 보기 릴리스 정보
author: natke
ms.author: nakersha
ms.date: 09/30/2019
ms.topic: article
uid: microsoft.quantum.relnotes
ms.openlocfilehash: 868d256270516cf99c228a757a11c6dc1a6319df
ms.sourcegitcommit: c93fea5980d1d46fbda1e7c7153831b9337134bf
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/04/2019
ms.locfileid: "73463330"
---
# <a name="microsoft-quantum-development-kit-release-notes"></a><span data-ttu-id="933ee-103">Microsoft Quantum Development Kit 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="933ee-103">Microsoft Quantum Development Kit Release Notes</span></span>

<span data-ttu-id="933ee-104">이 문서에는 각 Quantum Development Kit 릴리스에 대한 정보가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-104">This article contains information on each Quantum Development Kit release.</span></span>

<span data-ttu-id="933ee-105">설치 지침은[설치 가이드](xref:microsoft.quantum.install)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-105">For installation instructions, please refer to the [install guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="933ee-106">업데이트 지침은 [업데이트 가이드](xref:microsoft.quantum.update)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-106">For update instructions, please refer to the [update guide](xref:microsoft.quantum.update).</span></span>

## <a name="version-0101911307"></a><span data-ttu-id="933ee-107">버전 0.10.1911.307</span><span class="sxs-lookup"><span data-stu-id="933ee-107">Version 0.10.1911.307</span></span>

<span data-ttu-id="933ee-108">*릴리스 날짜: 2019년 11월 1일*</span><span class="sxs-lookup"><span data-stu-id="933ee-108">*Release date: November 1st, 2019*</span></span>

<span data-ttu-id="933ee-109">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-109">This release contains the following:</span></span>

- <span data-ttu-id="933ee-110">.NET Core SDK 버전에 종속되지 않도록 언어 서버를 자체 포함 실행 파일로 배포하는 Visual Studio Code 및 Visual Studio 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="933ee-110">Updates to Visual Studio Code & Visual Studio extensions to deploy language server as a self-contained executable, eliminating the .NET Core SDK version dependency</span></span>  
- <span data-ttu-id="933ee-111">.NET Core 3.0으로 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="933ee-111">Migration to .NET Core 3.0</span></span>
- <span data-ttu-id="933ee-112">새 `Fail` 메서드가 도입된 Microsoft.Quantum.Simulation.Core.IOperationFactory의 주요 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-112">Breaking change to Microsoft.Quantum.Simulation.Core.IOperationFactory with introduction of new `Fail` method.</span></span> <span data-ttu-id="933ee-113">SimulatorBase를 확장하지 않는 사용자 지정 시뮬레이터에만 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-113">It affects only custom simulators that do not extend SimulatorBase.</span></span> <span data-ttu-id="933ee-114">자세한 내용은 [GitHub에서 끌어오기 요청 보기를 참조하세요](https://github.com/microsoft/qsharp-runtime/pull/59).</span><span class="sxs-lookup"><span data-stu-id="933ee-114">For more details, [view the pull request on GitHub](https://github.com/microsoft/qsharp-runtime/pull/59).</span></span>
- <span data-ttu-id="933ee-115">사용되지 않는 특성에 대한 새로운 지원</span><span class="sxs-lookup"><span data-stu-id="933ee-115">New support for Deprecated attributes</span></span>

<span data-ttu-id="933ee-116">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [컴파일러](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [런타임](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) 및 [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed)에 대한 비공개 PR의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-116">See the full list of closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) and [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

## <a name="version-0919093002"></a><span data-ttu-id="933ee-117">버전 0.9.1909.3002</span><span class="sxs-lookup"><span data-stu-id="933ee-117">Version 0.9.1909.3002</span></span>

<span data-ttu-id="933ee-118">*릴리스 날짜: 2019년 9월 30일*</span><span class="sxs-lookup"><span data-stu-id="933ee-118">*Release date: September 30th, 2019*</span></span>

<span data-ttu-id="933ee-119">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-119">This release contains the following:</span></span>

- <span data-ttu-id="933ee-120">Visual Studio 2019(버전 16.3 이상) 및 Visual Studio Code에서 Q# 코드 완성에 대한 새로운 지원</span><span class="sxs-lookup"><span data-stu-id="933ee-120">New support for Q# code completion in Visual Studio 2019 (versions 16.3 & later) & Visual Studio Code</span></span>
- <span data-ttu-id="933ee-121">양자 가산기에 대한 새 [Quantum Kata](https://github.com/Microsoft/QuantumKatas)</span><span class="sxs-lookup"><span data-stu-id="933ee-121">New [Quantum Kata](https://github.com/Microsoft/QuantumKatas) for quantum adders</span></span>

<span data-ttu-id="933ee-122">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [컴파일러](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [런타임](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) 및 [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed)에 대한 비공개 PR의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-122">See the full list of closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) and [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

## <a name="version-09-packagereference-0919082902"></a><span data-ttu-id="933ee-123">버전 0.9(*PackageReference 0.9.1908.2902*)</span><span class="sxs-lookup"><span data-stu-id="933ee-123">Version 0.9 (*PackageReference 0.9.1908.2902*)</span></span>

<span data-ttu-id="933ee-124">*릴리스 날짜: 2019년 8월 29일*</span><span class="sxs-lookup"><span data-stu-id="933ee-124">*Release date: August 29th, 2019*</span></span>

<span data-ttu-id="933ee-125">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-125">This release contains the following:</span></span>

- <span data-ttu-id="933ee-126">Q#의 [접합 문](xref:microsoft.quantum.language.statements#conjugations)에 대한 새로운 지원</span><span class="sxs-lookup"><span data-stu-id="933ee-126">New support for [conjugation statements](xref:microsoft.quantum.language.statements#conjugations) in Q#</span></span>
- <span data-ttu-id="933ee-127">컴파일러의 새 코드 작업(예: "바꿀 내용", "설명서 추가" 및 단순 배열 항목 업데이트)</span><span class="sxs-lookup"><span data-stu-id="933ee-127">New code actions in the compiler, such as: "replace with", "add documentation", and simple array item update</span></span>
- <span data-ttu-id="933ee-128">설치 템플릿 및 새 프로젝트 명령이 Visual Studio Code 확장에 추가됨</span><span class="sxs-lookup"><span data-stu-id="933ee-128">Added install template and new project commands to Visual Studio Code extension</span></span>
- <span data-ttu-id="933ee-129">ApplyIf 조합기의 새 변형(예: [Microsoft.Quantum.Canon.ApplyIfOne](xref:microsoft.quantum.canon.applyifone))이 추가됨</span><span class="sxs-lookup"><span data-stu-id="933ee-129">Added new variants of ApplyIf combinator such as [Microsoft.Quantum.Canon.ApplyIfOne](xref:microsoft.quantum.canon.applyifone)</span></span>
- <span data-ttu-id="933ee-130">추가 [Quantum Katas](https://github.com/Microsoft/QuantumKatas)가 Jupyter Notebook으로 변환됨</span><span class="sxs-lookup"><span data-stu-id="933ee-130">Additional [Quantum Katas](https://github.com/Microsoft/QuantumKatas) converted to Jupyter Notebooks</span></span>
- <span data-ttu-id="933ee-131">Visual Studio 확장에는 이제 Visual Studio 2019가 필요함</span><span class="sxs-lookup"><span data-stu-id="933ee-131">Visual Studio Extension now requires Visual Studio 2019</span></span>

<span data-ttu-id="933ee-132">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [컴파일러](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [런타임](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) 및 [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed)에 대한 비공개 PR의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-132">See the full list of closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) and [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

<span data-ttu-id="933ee-133">여기에는 변경 내용이 요약되어 있으며, 기존 프로그램을 업그레이드하는 방법에 대한 지침도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-133">The changes are summarized here as well as instructions for upgrading your existing programs.</span></span>  <span data-ttu-id="933ee-134">이러한 변경 내용은 [Q# 개발 블로그](https://devblogs.microsoft.com/qsharp)에서 자세히 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-134">Read more about these changes on the [Q# dev blog](https://devblogs.microsoft.com/qsharp).</span></span>

## <a name="version-08-packagereference-0819071701"></a><span data-ttu-id="933ee-135">버전 0.8(*PackageReference 0.8.1907.1701*)</span><span class="sxs-lookup"><span data-stu-id="933ee-135">Version 0.8 (*PackageReference 0.8.1907.1701*)</span></span>

<span data-ttu-id="933ee-136">*릴리스 날짜: 2019년 7월 12일*</span><span class="sxs-lookup"><span data-stu-id="933ee-136">*Release date: July 12, 2019*</span></span>

<span data-ttu-id="933ee-137">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-137">This release contains the following:</span></span>

- <span data-ttu-id="933ee-138">배열 조각화에 대한 새 인덱싱 위치 - 자세한 내용은 [언어 참조](xref:microsoft.quantum.language.expressions#array-slices)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-138">New indexing locations for slicing arrays, [see the language reference](xref:microsoft.quantum.language.expressions#array-slices) for more information.</span></span>
- <span data-ttu-id="933ee-139">[Microsoft Container Registry](https://github.com/microsoft/ContainerRegistry)에서 호스팅되는 Docker 파일이 추가됨 - 자세한 내용은 [IQ# 리포지토리](https://github.com/microsoft/iqsharp/blob/master/README.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-139">Added Dockerfile hosted on the [Microsoft Container Registry](https://github.com/microsoft/ContainerRegistry), see the [IQ# repository for more information](https://github.com/microsoft/iqsharp/blob/master/README.md)</span></span>
- <span data-ttu-id="933ee-140">[추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)에 대한 호환성이 손상되는 변경, 구성 설정 업데이트, 이름 변경 - [업데이트된 이름에 대한 .NET API 브라우저](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulatorconfiguration)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-140">Breaking change for [the trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), update to configuration settings, name changes; see the [.NET API Browser for the updated names](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulatorconfiguration).</span></span>

<span data-ttu-id="933ee-141">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) 및 [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed)에 대한 비공개 PR의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-141">See the full list of closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) and [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

## <a name="version-07-packagereference-0719053109"></a><span data-ttu-id="933ee-142">버전 0.7(*PackageReference 0.7.1905.3109*)</span><span class="sxs-lookup"><span data-stu-id="933ee-142">Version 0.7 (*PackageReference 0.7.1905.3109*)</span></span>

<span data-ttu-id="933ee-143">*릴리스 날짜: 2019년 5월 31일*</span><span class="sxs-lookup"><span data-stu-id="933ee-143">*Release date: May 31, 2019*</span></span>

<span data-ttu-id="933ee-144">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-144">This release contains the following:</span></span>
- <span data-ttu-id="933ee-145">Q# 언어에 추가된 항목</span><span class="sxs-lookup"><span data-stu-id="933ee-145">additions to the Q# language,</span></span> 
- <span data-ttu-id="933ee-146">화학 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="933ee-146">updates to the chemistry library,</span></span> 
- <span data-ttu-id="933ee-147">새 숫자 라이브러리</span><span class="sxs-lookup"><span data-stu-id="933ee-147">a new numerics library.</span></span>

<span data-ttu-id="933ee-148">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) 및 [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed)에 대한 비공개 PR의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-148">See the full list of closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) and [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

<span data-ttu-id="933ee-149">여기에는 변경 내용이 요약되어 있으며, 기존 프로그램을 업그레이드하는 방법에 대한 지침도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-149">The changes are summarized here as well as instructions for upgrading your existing programs.</span></span>  <span data-ttu-id="933ee-150">이러한 변경 내용은 [Q# 개발 블로그](https://devblogs.microsoft.com/qsharp)에서 자세히 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-150">Read more about these changes on the [Q# dev blog](https://devblogs.microsoft.com/qsharp).</span></span>

### <a name="q-language-syntax"></a><span data-ttu-id="933ee-151">Q # 언어 구문</span><span class="sxs-lookup"><span data-stu-id="933ee-151">Q# language syntax</span></span>
<span data-ttu-id="933ee-152">이 릴리스에 추가된 새 Q# 언어 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-152">This release adds new Q# language syntax:</span></span>
* <span data-ttu-id="933ee-153">[사용자 정의 형식](xref:microsoft.quantum.language.type-model#user-defined-types)에 대해 명명된 항목이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-153">Add named items for [user-defined types](xref:microsoft.quantum.language.type-model#user-defined-types).</span></span>  
* <span data-ttu-id="933ee-154">이제 사용자 정의 형식 생성자를 함수로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-154">User-defined type constructors can now be used as functions.</span></span>
* <span data-ttu-id="933ee-155">[복사 및 업데이트](xref:microsoft.quantum.language.expressions#copy-and-update-expressions)(copy-and-update) 및 [적용 및 재할당]((xref:microsoft.quantum.language.statements#rebinding-of-mutable-symbols))(apply-and-reassign) 지원이 사용자 정의 형식에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-155">Add support for [copy-and-update](xref:microsoft.quantum.language.expressions#copy-and-update-expressions) and [apply-and-reassign]((xref:microsoft.quantum.language.statements#rebinding-of-mutable-symbols)) in user-defined types.</span></span>
* <span data-ttu-id="933ee-156">[성공할 때까지 반복](xref:microsoft.quantum.language.statements#repeat-until-success-loop)(repeat-until-success) 루프에 대한 픽스업 블록은 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-156">Fixup-block for [repeat-until-success](xref:microsoft.quantum.language.statements#repeat-until-success-loop) loops is now optional.</span></span>
* <span data-ttu-id="933ee-157">이제 작동 중이 아닌 함수에서 while 루프를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-157">We now support while loops in functions (not in operations).</span></span>

### <a name="library"></a><span data-ttu-id="933ee-158">라이브러리</span><span class="sxs-lookup"><span data-stu-id="933ee-158">Library</span></span> 

<span data-ttu-id="933ee-159">이 릴리스에는 숫자 라이브러리가 추가되었습니다. [새 숫자 라이브러리를 사용](xref:microsoft.quantum.numerics.usage)하는 방법에 대한 자세한 정보를 알아보고, [새 샘플](https://github.com/microsoft/quantum/tree/master/Numerics)을 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-159">This release adds a numerics library: Learn more about how to [use the new numerics library](xref:microsoft.quantum.numerics.usage) and try out the [new samples](https://github.com/microsoft/quantum/tree/master/Numerics).</span></span>  <span data-ttu-id="933ee-160">[PR #102](https://github.com/Microsoft/QuantumLibraries/pull/102)</span><span class="sxs-lookup"><span data-stu-id="933ee-160">[PR #102](https://github.com/Microsoft/QuantumLibraries/pull/102).</span></span>  

<span data-ttu-id="933ee-161">이 릴리스에서는 화학 라이브러리가 확장 및 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-161">This release reorganizes extends and updates the chemistry library:</span></span>
* <span data-ttu-id="933ee-162">구성 요소, 확장성, 일반 코드 정리의 모듈화가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-162">Improves modularity of components, extensibility, general code cleanup.</span></span>  <span data-ttu-id="933ee-163">[PR #58](https://github.com/microsoft/QuantumLibraries/pull/58)</span><span class="sxs-lookup"><span data-stu-id="933ee-163">[PR #58](https://github.com/microsoft/QuantumLibraries/pull/58).</span></span>
* <span data-ttu-id="933ee-164">[다중 참조 wavefunction(파동 함수)](xref:microsoft.quantum.chemistry.concepts.multireference)에 대한 지원(스파스 다중 참조 파동 함수 및 단일 결합 클러스터 모두)이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-164">Add support for [multi-reference wavefunctions](xref:microsoft.quantum.chemistry.concepts.multireference), both sparse multi-reference wavefunctions and unitary coupled cluster.</span></span>  <span data-ttu-id="933ee-165">[PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110)</span><span class="sxs-lookup"><span data-stu-id="933ee-165">[PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110).</span></span>
* <span data-ttu-id="933ee-166">(감사합니다!) [1QBit](https://1qbit.com) 기여자([@valentinS4t1qbit](https://github.com/ValentinS4t1qbit)): 변이 가설 풀이(variational ansatz)를 사용한 에너지 평가입니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-166">(Thank you!) [1QBit](https://1qbit.com) contributor ([@valentinS4t1qbit](https://github.com/ValentinS4t1qbit)): Energy evaluation using variational ansatz.</span></span> <span data-ttu-id="933ee-167">[PR #120](https://github.com/Microsoft/QuantumLibraries/pull/120)</span><span class="sxs-lookup"><span data-stu-id="933ee-167">[PR #120](https://github.com/Microsoft/QuantumLibraries/pull/120).</span></span>
* <span data-ttu-id="933ee-168">[Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) 스키마가 새 [0.2 버전](xref:microsoft.quantum.libraries.chemistry.schema.spec_v_0_2)으로 업데이트되고, 단일 결합 클러스터 사양이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-168">Updating [Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) schema to new [version 0.2](xref:microsoft.quantum.libraries.chemistry.schema.spec_v_0_2), adding unitary coupled cluster specification.</span></span> <span data-ttu-id="933ee-169">[Issue #65](https://github.com/microsoft/QuantumLibraries/issues/65)</span><span class="sxs-lookup"><span data-stu-id="933ee-169">[Issue #65](https://github.com/microsoft/QuantumLibraries/issues/65).</span></span>
* <span data-ttu-id="933ee-170">Python 상호 운용성이 화학 라이브러리 기능에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-170">Adding Python interoperability to chemistry library functions.</span></span> <span data-ttu-id="933ee-171">이 [샘플](https://github.com/microsoft/Quantum/tree/master/Chemistry/PythonIntegration)을 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-171">Try out this [sample](https://github.com/microsoft/Quantum/tree/master/Chemistry/PythonIntegration).</span></span> <span data-ttu-id="933ee-172">[Issue #53](https://github.com/microsoft/QuantumLibraries/issues/53), [PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110)</span><span class="sxs-lookup"><span data-stu-id="933ee-172">[Issue #53](https://github.com/microsoft/QuantumLibraries/issues/53) [PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110).</span></span>

## <a name="version-061905"></a><span data-ttu-id="933ee-173">버전 0.6.1905</span><span class="sxs-lookup"><span data-stu-id="933ee-173">Version 0.6.1905</span></span>

<span data-ttu-id="933ee-174">*릴리스 날짜: 2019년 5월 3일*</span><span class="sxs-lookup"><span data-stu-id="933ee-174">*Release date: May 3, 2019*</span></span>

<span data-ttu-id="933ee-175">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-175">This release contains the following:</span></span>
- <span data-ttu-id="933ee-176">Q# 언어 변경</span><span class="sxs-lookup"><span data-stu-id="933ee-176">makes changes to the Q# language,</span></span> 
- <span data-ttu-id="933ee-177">Quantum Development Kit 라이브러리 재구성</span><span class="sxs-lookup"><span data-stu-id="933ee-177">restructures the Quantum Development Kit libraries,</span></span> 
- <span data-ttu-id="933ee-178">새 샘플 추가</span><span class="sxs-lookup"><span data-stu-id="933ee-178">adds new samples, and</span></span> 
- <span data-ttu-id="933ee-179">버그 수정</span><span class="sxs-lookup"><span data-stu-id="933ee-179">fixes bugs.</span></span>  <span data-ttu-id="933ee-180">[라이브러리](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) 및 [샘플](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed)에 대한 몇 가지 비공개 PR</span><span class="sxs-lookup"><span data-stu-id="933ee-180">Several closed PRs for [libraries](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) and [samples](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).</span></span>  

<span data-ttu-id="933ee-181">여기에는 변경 내용이 요약되어 있으며, 기존 프로그램을 업그레이드하는 방법에 대한 지침도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-181">The changes are summarized here as well as instructions for upgrading your existing programs.</span></span>  <span data-ttu-id="933ee-182">이러한 변경 내용은 devblogs.microsoft.com/qsharp에서 자세히 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-182">You can read more about these changes on devblogs.microsoft.com/qsharp.</span></span>

### <a name="q-language-syntax"></a><span data-ttu-id="933ee-183">Q # 언어 구문</span><span class="sxs-lookup"><span data-stu-id="933ee-183">Q# language syntax</span></span>
<span data-ttu-id="933ee-184">이 릴리스에 추가된 새 Q# 언어 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-184">This release adds new Q# language syntax:</span></span>
* <span data-ttu-id="933ee-185">`+` 연산자를 사용하여 [양자 연산 특수화(제어 및 수반(adjoint))를 표현하는 간단한 방법](xref:microsoft.quantum.language.type-model#functors)이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-185">Add a [shorthand way to express specializations of quantum operations](xref:microsoft.quantum.language.type-model#functors) (control and adjoints) with `+` operators.</span></span>  <span data-ttu-id="933ee-186">이전 구문은 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-186">The old syntax is deprecated.</span></span>  <span data-ttu-id="933ee-187">이전 구문(예: `: adjoint`)을 사용하는 프로그램은 계속 작동하지만 컴파일 시간 경고가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-187">Programs that use the old syntax (e.g., `: adjoint`) will continue to work, but a compile time warning will be generated.</span></span>  
* <span data-ttu-id="933ee-188">새로운 [복사 및 업데이트](xref:microsoft.quantum.language.expressions#copy-and-update-expressions) 연산자인 `w/`가 추가되었습니다. 이는 배열 만들기를 기존 배열의 수정으로 표현하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-188">Add a new operator for [copy-and-update](xref:microsoft.quantum.language.expressions#copy-and-update-expressions), `w/`, can be used to express array creation as a modification of an existing array.</span></span>
* <span data-ttu-id="933ee-189">일반적인 [적용 및 업데이트(apply-and-update) 문](xref:microsoft.quantum.language.statements#rebinding-of-mutable-symbols)(예: `+=`, `w/=`)이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-189">Add the common [apply-and-upate statement](xref:microsoft.quantum.language.statements#rebinding-of-mutable-symbols), e.g., `+=`, `w/=`.</span></span>
* <span data-ttu-id="933ee-190">짧은 네임스페이스 이름을 지정하는 방법이 [open 지시문](xref:microsoft.quantum.language.file-structure#open-directives)에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-190">Add a way to specify a short name for namespaces in [open directives](xref:microsoft.quantum.language.file-structure#open-directives).</span></span>

<span data-ttu-id="933ee-191">이 릴리즈에서는 더 이상 배열 요소를 set 문의 왼쪽에 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-191">With this release, we no longer allow an array element to be specified on the left side of a set statement.</span></span>  <span data-ttu-id="933ee-192">이는 실제로 연산 결과에서 항상 수정을 통해 새 배열을 만드는 경우 구문에서 이 배열을 변경할 수 있음을 의미하기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-192">This is because that syntax implies that arrays are mutable when in fact, the result of the operation has always been the creation of a new array with the modification.</span></span>  <span data-ttu-id="933ee-193">대신, 동일한 결과를 얻기 위해 새 복사 및 업데이트 연산자인 `w/`를 사용하라는 제안과 함께 컴파일러 오류가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-193">Instead, a compiler error will be generated with a suggestion to use the new copy-and-update operator, `w/`, to accomplish the same result.</span></span>  

### <a name="library-restructuring"></a><span data-ttu-id="933ee-194">라이브러리 재구성</span><span class="sxs-lookup"><span data-stu-id="933ee-194">Library restructuring</span></span>
<span data-ttu-id="933ee-195">이 릴리스에서는 라이브러리를 다음과 같이 일관된 방식으로 확장할 수 있도록 재구성합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-195">This release reorganizes the libraries to enable their growth in a consistent way:</span></span>
* <span data-ttu-id="933ee-196">Microsoft.Quantum.Primitive 네임스페이스의 이름을 Microsoft.Quantum.Intrinsic으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-196">Renames the Microsoft.Quantum.Primitive namespace  to Microsoft.Quantum.Intrinsic.</span></span>  <span data-ttu-id="933ee-197">이러한 연산은 대상 머신에서 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-197">These operations are implemented by the target machine.</span></span>  <span data-ttu-id="933ee-198">Microsoft.Quantum.Primitive 네임스페이스는 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-198">The Microsoft.Quantum.Primitive namespace is deprecated.</span></span>  <span data-ttu-id="933ee-199">프로그램에서 더 이상 사용되지 않는 이름을 사용하여 연산과 함수를 호출하는 경우 런타임 경고에서 이를 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-199">A runtime warning will advise when programs call operations and functions using deprecated names.</span></span>

* <span data-ttu-id="933ee-200">Microsoft.Quantum.Canon 패키지의 이름을 Microsoft.Quantum.Standard로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-200">Renames the Microsoft.Quantum.Canon package to Microsoft.Quantum.Standard.</span></span>  <span data-ttu-id="933ee-201">이 패키지에는 대부분의 Q# 프로그램에 공통된 네임스페이스가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-201">This package contains namespaces that are common to most Q# programs.</span></span>  <span data-ttu-id="933ee-202">다음 내용이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-202">This includes:</span></span>  
    - <span data-ttu-id="933ee-203">일반 연산에 대한 Microsoft.Quantum.Canon</span><span class="sxs-lookup"><span data-stu-id="933ee-203">Microsoft.Quantum.Canon for common operations</span></span>
    - <span data-ttu-id="933ee-204">범용 산술 연산용 Microsoft.Quantum.Arithmetic</span><span class="sxs-lookup"><span data-stu-id="933ee-204">Microsoft.Quantum.Arithmetic for general purpose arithmetic operations</span></span>
    - <span data-ttu-id="933ee-205">큐비트 상태를 준비하는 데 사용되는 연산에 대한 Microsoft.Quantum.Preparation</span><span class="sxs-lookup"><span data-stu-id="933ee-205">Microsoft.Quantum.Preparation for operations used to prepare qubit state</span></span>
    - <span data-ttu-id="933ee-206">시뮬레이션 기능에 대한 Microsoft.Quantum.Simulation</span><span class="sxs-lookup"><span data-stu-id="933ee-206">Microsoft.Quantum.Simulation for simulation functionality</span></span>

<span data-ttu-id="933ee-207">이 변경으로 인해 Microsoft.Quatum.Canon 네임스페이스에 대한 단일 "open" 문이 포함된 프로그램에서 다른 세 개의 새 네임스페이스로 이동된 연산을 참조하는 경우 빌드 오류가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-207">With this change, programs that include a single "open" statement for the namespace Microsoft.Quatum.Canon may encounter build errors if the program references operations that were moved to the other three new namespaces.</span></span>  <span data-ttu-id="933ee-208">세 개의 새 네임스페이스에 대한 추가 open 문을 추가하면 이 문제를 간단히 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-208">Adding the additional open statements for the three new namespaces is a straightforward way to resolve this issue.</span></span>  

* <span data-ttu-id="933ee-209">내부 연산이 다른 네임스페이스로 재구성되었으므로 여러 네임스페이스가 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-209">Several namespaces have been deprecated as the operations within have been reorganized to other namespaces.</span></span> <span data-ttu-id="933ee-210">이러한 네임스페이스를 사용하는 프로그램은 계속 작동하며, 컴파일 시간 경고는 연산이 정의된 네임스페이스를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-210">Programs that use these namespaces will continue to work, and a compile time warning will denote the namespace where the operation is defined.</span></span>  

* <span data-ttu-id="933ee-211">Microsoft.Quantum.Arithmetic 네임스페이스는 <xref:microsoft.quantum.arithmetic.littleendian> 사용자 정의 형식을 사용하도록 일반화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-211">The Microsoft.Quantum.Arithmetic namespace has been normalized to use the <xref:microsoft.quantum.arithmetic.littleendian> user-defined type.</span></span> <span data-ttu-id="933ee-212">little endian으로 변환해야 하는 경우, 함수 [BigEndianAsLittleEndian](xref:microsoft.quantum.arithmetic.bigendianaslittleendian)을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-212">Use the function [BigEndianAsLittleEndian](xref:microsoft.quantum.arithmetic.bigendianaslittleendian) when needed to convert to little endian.</span></span>  

* <span data-ttu-id="933ee-213">몇몇 호출 가능 항목(함수 및 작업)의 이름이 [Q# 스타일 가이드](xref:microsoft.quantum.contributing.style)에 맞춰 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-213">The names of several callables (functions and operations) have been changed to conform to the [Q# Style Guide](xref:microsoft.quantum.contributing.style).</span></span>  <span data-ttu-id="933ee-214">이전 호출 가능 이름은 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-214">The old callable names are deprecated.</span></span>  <span data-ttu-id="933ee-215">이전 호출 가능 항목을 사용하는 프로그램은 계속 작동하지만 컴파일 시간 경고가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-215">Programs that use the old callables will continue to work with a compile time warning.</span></span> 

### <a name="new-samples"></a><span data-ttu-id="933ee-216">새 샘플</span><span class="sxs-lookup"><span data-stu-id="933ee-216">New Samples</span></span>

<span data-ttu-id="933ee-217">[F# 드라이버에 Q#를 사용하는 샘플](https://github.com/Microsoft/Quantum/pull/164)을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-217">We added a [sample of using Q# with F# driver](https://github.com/Microsoft/Quantum/pull/164).</span></span>  

<span data-ttu-id="933ee-218">**감사합니다.**</span><span class="sxs-lookup"><span data-stu-id="933ee-218">**Thank you!**</span></span> <span data-ttu-id="933ee-219">http://github.com/Microsoft/Quantum 에서 열려 있는 코드베이스에 기여해 주신 분들께 감사의 말씀을 전합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-219">to the following contributor to our open code base at http://github.com/Microsoft/Quantum.</span></span> <span data-ttu-id="933ee-220">이러한 기여는 Q# 코드의 다양한 샘플을 모으는 데 큰 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-220">These contributions add significantly to the rich samples of Q# code:</span></span>

* <span data-ttu-id="933ee-221">Mathias Soeken([@msoeken](https://github.com/msoeken)): Oracle 함수 합성.</span><span class="sxs-lookup"><span data-stu-id="933ee-221">Mathias Soeken ([@msoeken](https://github.com/msoeken)): Oracle function synthesis.</span></span> <span data-ttu-id="933ee-222">[PR #135](https://github.com/Microsoft/Quantum/pull/135).</span><span class="sxs-lookup"><span data-stu-id="933ee-222">[PR #135](https://github.com/Microsoft/Quantum/pull/135).</span></span>

### <a name="migrating-existing-projects-to-061905"></a><span data-ttu-id="933ee-223">기존 프로젝트를 0.6.1905로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-223">Migrating existing projects to 0.6.1905.</span></span>

<span data-ttu-id="933ee-224">QDK를 업데이트하려면 [설치 가이드](xref:microsoft.quantum.install)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-224">See the [install guide](xref:microsoft.quantum.install) to update the QDK.</span></span>
  
<span data-ttu-id="933ee-225">Quantum Development Kit 버전 0.5의 기존 Q# 프로젝트가 있는 경우, 해당 프로젝트를 최신 버전으로 마이그레이션하는 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-225">If you have existing Q# projects from version 0.5 of the Quantum Development Kit, the following are the steps to migrate those projects to the newest version.</span></span>

    1. <span data-ttu-id="933ee-226">프로젝트는 순서대로 업그레이드해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-226">Projects need to be upgraded in order.</span></span>  <span data-ttu-id="933ee-227">솔루션의 프로젝트가 여러 개인 경우, 각 프로젝트를 참조 순서대로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-227">If you have a solution with multiple projects, update each project in the order they are referenced.</span></span>
    2. <span data-ttu-id="933ee-228">명령줄에서 `dotnet clean`을 실행하여 기존의 모든 이진 파일과 중간 파일을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-228">From a command line, Run `dotnet clean` to remove all existing binaries and intermediate files.</span></span>
    3. <span data-ttu-id="933ee-229">텍스트 편집기에서 .csproj 파일을 편집하여 모든 "Microsoft.Quantum" `PackageReference`의 버전을 0.6.1904 버전으로 변경하고 "Microsoft.Quantum.Canon" 패키지 이름을 "Microsoft.Quantum.Standard"로 변경합니다. 예:</span><span class="sxs-lookup"><span data-stu-id="933ee-229">In a text editor, edit the .csproj file to change the version of all the "Microsoft.Quantum" `PackageReference` to version 0.6.1904, and change the "Microsoft.Quantum.Canon" package name to "Microsoft.Quantum.Standard", for example:</span></span>

         ```xml
        <PackageReference Include="Microsoft.Quantum.Standard" Version="0.6.1905.301" />
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.6.1905.301" />
        ```
    4. <span data-ttu-id="933ee-230">명령줄에서 다음 명령을 실행합니다. `dotnet msbuild`</span><span class="sxs-lookup"><span data-stu-id="933ee-230">From the command line, run this command: `dotnet msbuild`</span></span>  
    5. <span data-ttu-id="933ee-231">이를 실행한 후에도 여전히 위에 나열한 변경 내용으로 인해 수동으로 오류를 해결해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-231">After running this, you might still need to manually address errors due to changes listed above.</span></span>  <span data-ttu-id="933ee-232">대부분의 경우 Visual Studio 또는 Visual Studio Code의 IntelliSense가 이러한 오류를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-232">In many cases, these errors will also be reported by IntelliSense in Visual Studio or Visual Studio Code.</span></span>
        - <span data-ttu-id="933ee-233">Visual Studio 2019 또는 Visual Studio Code에서 프로젝트의 루트 폴더 또는 포함 솔루션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-233">Open the root folder of the project or the containing solution in Visual Studio 2019 or Visual Studio Code.</span></span>
        - <span data-ttu-id="933ee-234">편집기에서 .qs 파일을 열면 출력 창에 Q# 언어 확장의 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-234">After opening a .qs file in the editor, you should see the output of the Q# language extension in the output window.</span></span>
        - <span data-ttu-id="933ee-235">프로젝트를 로드한 후(출력 창에 표시됨), 각 파일을 열어 남은 모든 문제를 수동으로 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-235">After the project has loaded successfully (indicated in the output window) open each file and manually to address all remaining issues.</span></span>

> [!NOTE]
> * <span data-ttu-id="933ee-236">0\.6 릴리스의 경우, Quantum Development Kit에 포함된 언어 서버는 여러 작업 영역을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-236">For the 0.6 release, the language server included with the Quantum Development Kit does not support multiple workspaces.</span></span>
> * <span data-ttu-id="933ee-237">Visual Studio Code에서 프로젝트 작업을 하려면 해당 프로젝트 자체와 참조된 모든 프로젝트가 포함된 루트 폴더를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-237">In order to work with a project in Visual Studio Code, open the root folder containing the project itself and all referenced projects.</span></span>   
> * <span data-ttu-id="933ee-238">Visual Studio에서 솔루션을 사용하려면 솔루션에 포함된 모든 프로젝트가 솔루션이 있는 폴더나 그 하위 폴더 중 하나에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-238">In order to work with a solution in Visual Studio, all projects contained in the solution need to be in the same folder as the solution or in one of its subfolders.</span></span>  
> * <span data-ttu-id="933ee-239">0\.6 이상에 마이그레이션된 프로젝트와 이전 패키지 버전을 사용하는 프로젝트 간의 참조는 지원되지 **않습니다**.</span><span class="sxs-lookup"><span data-stu-id="933ee-239">References between projects migrated to 0.6 and higher and projects using older package versions are **not** supported.</span></span>

## <a name="version-051904"></a><span data-ttu-id="933ee-240">버전 0.5.1904</span><span class="sxs-lookup"><span data-stu-id="933ee-240">Version 0.5.1904</span></span>

<span data-ttu-id="933ee-241">*릴리스 날짜: 2019년 4월 15일*</span><span class="sxs-lookup"><span data-stu-id="933ee-241">*Release date: April 15, 2019*</span></span>

<span data-ttu-id="933ee-242">이 릴리스에는 버그 수정이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-242">This release contains bug fixes.</span></span>


## <a name="version-051903"></a><span data-ttu-id="933ee-243">버전 0.5.1903</span><span class="sxs-lookup"><span data-stu-id="933ee-243">Version 0.5.1903</span></span>

<span data-ttu-id="933ee-244">*릴리스 날짜: 2019년 3월 27일*</span><span class="sxs-lookup"><span data-stu-id="933ee-244">*Release date: March 27, 2019*</span></span>

<span data-ttu-id="933ee-245">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-245">This release contains the following:</span></span>

- <span data-ttu-id="933ee-246">Q#를 학습할 수 있는 좋은 방법을 제공하는 Jupyter Notebook에 대한 지원이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-246">Adds support for Jupyter Notebook, which offers a great way to learn about Q#.</span></span>  <span data-ttu-id="933ee-247">[새 Jupyter Notebook 샘플을 확인하고 사용자 고유의 노트북을 작성하는 방법을 알아보세요](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="933ee-247">[Check out new Jupyter Notebook samples and learn how to write your own Notebooks](xref:microsoft.quantum.install).</span></span> 

- <span data-ttu-id="933ee-248">정수 adder 산술을 Quantum Canon 라이브러리에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-248">Adds integer adder arithmetic to the Quantum Canon library.</span></span>  <span data-ttu-id="933ee-249">[새 정수 adder를 사용하는 방법](https://github.com/Microsoft/Quantum/blob/master/Samples/src/Arithmetic/Adder%20Example.ipynb)을 설명하는 Jupyter Notebook도 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-249">See also a Jupyter Notebook that [describes how to use the new integer adders](https://github.com/Microsoft/Quantum/blob/master/Samples/src/Arithmetic/Adder%20Example.ipynb).</span></span>

- <span data-ttu-id="933ee-250">커뮤니티가 보고한 DumpRegister 문제의 버그를 수정했습니다([#148](https://github.com/Microsoft/Quantum/issues/148)).</span><span class="sxs-lookup"><span data-stu-id="933ee-250">Bug fix for DumpRegister issue reported by the community ([#148](https://github.com/Microsoft/Quantum/issues/148)).</span></span>

- <span data-ttu-id="933ee-251">[문 사용](xref:microsoft.quantum.language.statements) 내에서 반환하는 기능을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-251">Added ability to return from within a [using statement](xref:microsoft.quantum.language.statements).</span></span>

- <span data-ttu-id="933ee-252">[시작 가이드](xref:microsoft.quantum.install)를 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-252">Revamped [getting started guide](xref:microsoft.quantum.install).</span></span>


## <a name="version-051902"></a><span data-ttu-id="933ee-253">버전 0.5.1902</span><span class="sxs-lookup"><span data-stu-id="933ee-253">Version 0.5.1902</span></span>

<span data-ttu-id="933ee-254">*릴리스 날짜: 2019년 2월 27일*</span><span class="sxs-lookup"><span data-stu-id="933ee-254">*Release date: February 27, 2019*</span></span>

<span data-ttu-id="933ee-255">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-255">This release contains the following:</span></span>

- <span data-ttu-id="933ee-256">플랫폼 간 Python 호스트에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-256">Adds support for a cross-platform Python host.</span></span>  <span data-ttu-id="933ee-257">Python의 `qsharp` 패키지를 사용하면 Python 내에서 Q# 작업 및 함수를 쉽게 시뮬레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-257">The `qsharp` package for Python makes it easy to simulate Q# operations and functions from within Python.</span></span> <span data-ttu-id="933ee-258">[Python 상호 운용성](xref:microsoft.quantum.install)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-258">Learn more about [Python interoperability](xref:microsoft.quantum.install).</span></span> 

- <span data-ttu-id="933ee-259">Visual Studio 및 Visual Studio Code 확장은 이제 기호 이름 바꾸기(예: 함수 및 작업)를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-259">The Visual Studio and Visual Studio Code extensions now support renaming of symbols (e.g., functions and operations).</span></span>

- <span data-ttu-id="933ee-260">이제 Visual Studio 2019에 Visual Studio 확장을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-260">The Visual Studio extension can now be installed on Visual Studio 2019.</span></span>

## <a name="version-041901"></a><span data-ttu-id="933ee-261">버전 0.4.1901</span><span class="sxs-lookup"><span data-stu-id="933ee-261">Version 0.4.1901</span></span>

<span data-ttu-id="933ee-262">*릴리스 날짜: 2019년 1월 30일*</span><span class="sxs-lookup"><span data-stu-id="933ee-262">*Release date: January 30, 2019*</span></span>

<span data-ttu-id="933ee-263">이 릴리스에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-263">This release contains the following:</span></span>

- <span data-ttu-id="933ee-264">임의적 크기의 부호 있는 정수를 나타내는 새 기본 형식인 BigInt에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-264">adds support for a new primitive type, BigInt, which represents a signed integer of arbitrary size.</span></span>  <span data-ttu-id="933ee-265">[BigInt 형식](xref:microsoft.quantum.language.type-model)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-265">Learn more about [BigInt type](xref:microsoft.quantum.language.type-model).</span></span>
- <span data-ttu-id="933ee-266">매우 많은 수의 큐비트로 X, CNOT, 다중 제어 X 퀀텀 작업을 시뮬레이션할 수 있는 특별한 용도의 고속 시뮬레이터인 새 Toffoli 시뮬레이터를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-266">adds new Toffoli simulator, a special purpose fast simulator that can simulate X, CNOT and multi-controlled X quantum operations with very large numbers of qubits.</span></span>  <span data-ttu-id="933ee-267">[Toffoli 시뮬레이터](xref:microsoft.quantum.machines.toffoli-simulator)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-267">Learn more about [Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator).</span></span>
- <span data-ttu-id="933ee-268">퀀텀 컴퓨터에서 Q# 작업의 지정된 인스턴스를 실행하는 데 필요한 리소스를 추정하는 간단한 리소스 추정기를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-268">adds a simple resource estimator that estimates the resources required to run a given instancee of a Q# operation on a quantum computer.</span></span>  <span data-ttu-id="933ee-269">[리소스 추정기](xref:microsoft.quantum.machines.resources-estimator)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-269">Learn more about the [Resource Estimator](xref:microsoft.quantum.machines.resources-estimator).</span></span>


## <a name="version-0318112802"></a><span data-ttu-id="933ee-270">버전 0.3.1811.2802</span><span class="sxs-lookup"><span data-stu-id="933ee-270">Version 0.3.1811.2802</span></span>

<span data-ttu-id="933ee-271">*릴리스 날짜: 2018년 11월 28일*</span><span class="sxs-lookup"><span data-stu-id="933ee-271">*Release date: November 28, 2018*</span></span>

<span data-ttu-id="933ee-272">어차피 VS Code 확장에서 사용하지 않고 있었지만 `event-stream` NPM 패키지와 관련된 [확장 제거](https://code.visualstudio.com/blogs/2018/11/26/event-stream) 작업 시 플래그를 지정하고 마켓플레이스에서 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-272">Even though our VS Code extension was not using it, it was flagged and removed from the marketplace during [the extensions purge](https://code.visualstudio.com/blogs/2018/11/26/event-stream) related to the `event-stream` NPM package.</span></span> <span data-ttu-id="933ee-273">이 버전은 확장이 빨간색 플래그를 트리거할 수 있게 만드는 모든 런타임 종속성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-273">This version removes all runtime dependencies that could make the extension trigger any red flags.</span></span>

<span data-ttu-id="933ee-274">이전에 확장을 설치한 경우, Visual Studio Marketplace에서 [Microsoft Quantum Development Kit for Visual Studio Code](vscode:extension/quantum.quantum-devkit-vscode) 확장을 방문한 다음, 설치를 눌러 다시 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-274">If you had previously installed the extension you will need to install it again by visiting the [Microsoft Quantum Development Kit for Visual Studio Code](vscode:extension/quantum.quantum-devkit-vscode) extension on the Visual Studio Marketplace and press Install.</span></span> <span data-ttu-id="933ee-275">불편을 드려 죄송합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-275">We are sorry about the inconvenience.</span></span>


## <a name="version-0318111511"></a><span data-ttu-id="933ee-276">버전 0.3.1811.1511</span><span class="sxs-lookup"><span data-stu-id="933ee-276">Version 0.3.1811.1511</span></span>

<span data-ttu-id="933ee-277">*릴리스 날짜: 2018년 11월 20일*</span><span class="sxs-lookup"><span data-stu-id="933ee-277">*Release date: November 20, 2018*</span></span>

<span data-ttu-id="933ee-278">이 릴리스는 일부 사용자가 Visual Studio 확장을 로드할 수 없게 만드는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-278">This release fixes a bug that prevented some users to successfully load the Visual Studio extension.</span></span>

<span data-ttu-id="933ee-279">Quantum Development Kit의 0.2 버전에서 업그레이드하는 경우, [Q# 언어 변경 내용 및 Q# 프로그램 마이그레이션](xref:microsoft.quantum.relnotes.migration-0-3)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-279">If you are upgrading from a 0.2 version of the Quantum Development Kit, learn more about [Q# language changes and migrating your Q# program](xref:microsoft.quantum.relnotes.migration-0-3).</span></span>

## <a name="version-031811203"></a><span data-ttu-id="933ee-280">버전 0.3.1811.203</span><span class="sxs-lookup"><span data-stu-id="933ee-280">Version 0.3.1811.203</span></span>

<span data-ttu-id="933ee-281">*릴리스 날짜: 2018년 11월 2일*</span><span class="sxs-lookup"><span data-stu-id="933ee-281">*Release date: November 2, 2018*</span></span>

<span data-ttu-id="933ee-282">이 릴리스에는 다음과 같은 몇 가지 버그 수정이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-282">This release includes a few bug fixes, including:</span></span>

* <span data-ttu-id="933ee-283">`DumpMachine`을 호출하면 특정 상황에서 시뮬레이터의 상태가 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-283">Invoking `DumpMachine` could change the state of the simulator under certain situations.</span></span>
* <span data-ttu-id="933ee-284">2\.1.403 이전의 .NET Core 버전을 사용하여 프로젝트를 빌드할 때 표시되는 컴파일 경고를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-284">Removed compilation warnings when building projects using a version of .NET Core previous to 2.1.403.</span></span>
* <span data-ttu-id="933ee-285">설명서를 정리했습니다. 특히 VS Code 또는 Visual Studio에서 마우스로 가리킬 때 표시되는 도구 설명을 정리했습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-285">Clean up of documentation, specially the tooltips shown during mouse hover in VS Code or Visual Studio.</span></span>

<span data-ttu-id="933ee-286">Quantum Development Kit의 0.2 버전에서 업그레이드하는 경우, [Q# 언어 변경 내용 및 Q# 프로그램 마이그레이션](xref:microsoft.quantum.relnotes.migration-0-3)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-286">If you are upgrading from a 0.2 version of the Quantum Development Kit, learn more about [Q# language changes and migrating your Q# program](xref:microsoft.quantum.relnotes.migration-0-3).</span></span>

## <a name="version-0318102508"></a><span data-ttu-id="933ee-287">버전 0.3.1810.2508</span><span class="sxs-lookup"><span data-stu-id="933ee-287">Version 0.3.1810.2508</span></span>

<span data-ttu-id="933ee-288">*릴리스 날짜: 2018년 10월 29일*</span><span class="sxs-lookup"><span data-stu-id="933ee-288">*Release date: October 29, 2018*</span></span>

<span data-ttu-id="933ee-289">이 릴리스에는 새 언어 기능과 향상된 개발자 환경이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-289">This release includes new language features and an improved developer experience:</span></span>

* <span data-ttu-id="933ee-290">이 릴리스에는 Q#용 언어 서버뿐만 아니라 Visual Studio 및 Visual Studio Code용 클라이언트 통합도 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-290">This release includes a language server for Q#, as well as the client integrations for Visual Studio and Visual Studio Code.</span></span> <span data-ttu-id="933ee-291">이렇게 하면 입력 시 오류 및 경고에 구불구불한 밑줄이 쳐지는 형태로 실시간 피드백을 포함하는 새 IntelliSense 기능 집합을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-291">This enables a new set of IntelliSense features along with live feedback on typing in form of squiggly underlinings of errors and warnings.</span></span> 
* <span data-ttu-id="933ee-292">이 업데이트는 진단 메시지를 전반적으로 크게 개선합니다. 탐색이 쉬워지고 진단 범위가 정확해지며 가리켜서 표시된 정보에서 추가 정보를 쉽게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-292">This update greatly improves diagnostic messages in general, with easy navigation to and precise ranges for diagnostics and additional details in the displayed hover information.</span></span>
* <span data-ttu-id="933ee-293">Q# 언어는 개발자가 언어 기능에 대한 일반적인 작업과 새로운 향상 작업을 통합하여 강력한 퀀텀 계산을 수행할 수 있게 하는 방식으로 확장되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-293">The Q# language has been extended in ways that unifies the ways developers can do common operations and new enhancements to the language features to powerfully express quantum computation.</span></span>  <span data-ttu-id="933ee-294">이 릴리스를 통해 Q# 언어에 몇 가지 주요 변경 사항이 적용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-294">There are a handful of breaking changes to the Q# language with this release.</span></span>   

<span data-ttu-id="933ee-295">[Q# 언어 변경 내용 및 Q# 프로그램 마이그레이션](xref:microsoft.quantum.relnotes.migration-0-3)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-295">Learn more about [Q# language changes and migrating your Q# program](xref:microsoft.quantum.relnotes.migration-0-3).</span></span>

<span data-ttu-id="933ee-296">이 릴리스에는 새 퀀텀 화학 라이브러리도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-296">This release also includes a new quantum chemistry library:</span></span>

* <span data-ttu-id="933ee-297">화학 라이브러리에는 다음과 같은 새로운 Hamiltonian 시뮬레이션 기능이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-297">The chemistry library contains new Hamiltonian simulation features, including:</span></span>
    - <span data-ttu-id="933ee-298">시뮬레이션 정확성을 향상하는 임의의 짝수 차원의 Trotter–Suzuki 통합자입니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-298">Trotter–Suzuki integrators of arbitrary even order for improved simulation accuracy.</span></span>
    - <span data-ttu-id="933ee-299">$T$-게이트의 복잡성을 줄이기 위해 화학별 최적화를 사용하는 큐비트화 시뮬레이션 기술입니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-299">Qubitization simulation technique with chemistry-specific optimizations for reducing $T$-gate complexity.</span></span>
* <span data-ttu-id="933ee-300">분자의 표현을 가져오고 시뮬레이션하는 데 사용할 수 있는 Broombridge 스키마(Hamiltonian의 탄생지로 기념되는 [랜드마크](https://en.wikipedia.org/wiki/Broom_Bridge)에서 딴 이름)라는 새로운 오픈 소스 스키마를 도입했습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-300">A new open source schema, called Broombridge Schema (in reference to a [landmark](https://en.wikipedia.org/wiki/Broom_Bridge) celebrated as a birthplace of Hamiltonians), is introduced for importing representations of molecules and simulating them.</span></span>
* <span data-ttu-id="933ee-301">Broombridge 스키마를 사용하여 정의된 여러 화학 표현을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-301">Multiple chemical representations defined using the Broombridge Schema are provided.</span></span>  <span data-ttu-id="933ee-302">이러한 모델은 오픈 소스 고성능 계산 화학 도구인 [NWChem](http://www.nwchem-sw.org/)에 의해 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-302">These models were generated by [NWChem](http://www.nwchem-sw.org/), an open source high-performance computational chemistry tool.</span></span>
* <span data-ttu-id="933ee-303">자습서 및 샘플에서는 화학 라이브러리 및 Broombridge 데이터 모델을 사용하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-303">Tutorials and Samples describe how to use the chemistry library and the Broombridge data models to:</span></span>
    - <span data-ttu-id="933ee-304">화학 라이브러리를 사용하여 간단한 Hamiltonian 구성</span><span class="sxs-lookup"><span data-stu-id="933ee-304">Construct simple Hamiltonians using the chemistry library</span></span>
    - <span data-ttu-id="933ee-305">단계 추정으로 수소화 리튬의 지반 에너지와 여기 에너지를 시각화합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-305">Visualize ground and excited energies of Lithium Hydride using phase estimation.</span></span>
    - <span data-ttu-id="933ee-306">퀀텀 화학 시뮬레이션의 리소스 추정 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-306">Perform resource estimates of quantum chemistry simulation.</span></span>
    - <span data-ttu-id="933ee-307">Broombridge 스키마로 표시되는 분자의 에너지 수준을 추정합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-307">Estimate energy levels of molecules represented by the Broombridge schema.</span></span>
* <span data-ttu-id="933ee-308">설명서에서는 NWChem을 사용하여 Q#로 퀀텀 시뮬레이션용 추가 화학 모델을 생성하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-308">Documentation describes how to use NWChem to generate additional chemical models for quantum simulation with Q#.</span></span>

<span data-ttu-id="933ee-309">[Quantum Development Kit 화학 라이브러리](xref:microsoft.quantum.chemistry.concepts.intro)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-309">Learn more about the [Quantum Development Kit chemistry library](xref:microsoft.quantum.chemistry.concepts.intro).</span></span>

<span data-ttu-id="933ee-310">새 화학 라이브러리를 기점으로 라이브러리를 [Microsoft/QuantumLibraries](https://github.com/Microsoft/QuantumLibraries)의 새 GitHub 리포지토리로 분리합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-310">With the new chemistry library, we are separating out the libraries into a new GitHub repo, [Microsoft/QuantumLibraries](https://github.com/Microsoft/QuantumLibraries).</span></span>  <span data-ttu-id="933ee-311">샘플은 [Microsoft/Quantum](https://github.com/Microsoft/Quantum) 리포지토리에 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-311">The samples remain in the repo [Microsoft/Quantum](https://github.com/Microsoft/Quantum).</span></span>  <span data-ttu-id="933ee-312">두 리포지토리에 모두 기여해 주셔서 감사합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-312">We welcome contributions to both!</span></span>

<span data-ttu-id="933ee-313">이 릴리스에는 커뮤니티에서 보고한 이슈에 대한 버그 수정 및 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-313">This release includes bug fixes and features for issues reported by the community:</span></span>

* <span data-ttu-id="933ee-314">Intellisense for Q#?</span><span class="sxs-lookup"><span data-stu-id="933ee-314">Intellisense for Q#?</span></span> <span data-ttu-id="933ee-315">([UserVoice](https://quantum.uservoice.com/forums/906943/suggestions/32656918))</span><span class="sxs-lookup"><span data-stu-id="933ee-315">([UserVoice](https://quantum.uservoice.com/forums/906943/suggestions/32656918)).</span></span>
* <span data-ttu-id="933ee-316">.qs 파일([UserVoice](https://quantum.uservoice.com/forums/906097/suggestions/32593049))</span><span class="sxs-lookup"><span data-stu-id="933ee-316">.qs files ([UserVoice](https://quantum.uservoice.com/forums/906097/suggestions/32593049)).</span></span>
* <span data-ttu-id="933ee-317">If 문에서 중괄호가 간단히 표시될 때 오류 메시지 개선([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/34718518))</span><span class="sxs-lookup"><span data-stu-id="933ee-317">Improve error message when curly braces are abbreviated in if statement ([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/34718518)).</span></span>
* <span data-ttu-id="933ee-318">변경 가능한 (재)바인딩 시 튜플 분해 지원([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/35020444))</span><span class="sxs-lookup"><span data-stu-id="933ee-318">Support tuple deconstruction at mutable (re-)binding ([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/35020444)).</span></span>
* <span data-ttu-id="933ee-319">제공된 BitFlipCode를 실행하는 동안 오류 발생([UserVoice](https://quantum.uservoice.com/forums/906940/suggestions/35008546))</span><span class="sxs-lookup"><span data-stu-id="933ee-319">Error Running Provided BitFlipCode ([UserVoice](https://quantum.uservoice.com/forums/906940/suggestions/35008546)).</span></span>
* <span data-ttu-id="933ee-320">H2SimulationGUI가 경우에 따라 큰 증가를 표시함([UserVoice](https://quantum.uservoice.com/forums/906946/suggestions/34668370))</span><span class="sxs-lookup"><span data-stu-id="933ee-320">H2SimulationGUI displays big peaks sometimes ([UserVoice](https://quantum.uservoice.com/forums/906946/suggestions/34668370)).</span></span>

### <a name="community-contributions"></a><span data-ttu-id="933ee-321">커뮤니티 기여</span><span class="sxs-lookup"><span data-stu-id="933ee-321">Community Contributions</span></span>

<span data-ttu-id="933ee-322">**감사합니다.**</span><span class="sxs-lookup"><span data-stu-id="933ee-322">**Thank you!**</span></span> <span data-ttu-id="933ee-323">http://github.com/Microsoft/Quantum 에서 열려 있는 코드베이스에 기여해 주신 다음 분들께 감사의 말씀을 드립니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-323">to the following contributors to our open code base at http://github.com/Microsoft/Quantum.</span></span> <span data-ttu-id="933ee-324">이분들의 기여 덕분에 Q# 코드의 샘플이 매우 다양해졌습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-324">These contributions add significantly to the rich samples of Q# code:</span></span>

* <span data-ttu-id="933ee-325">Rolf Huisman([@RolfHuisman](https://github.com/RolfHuisman)): Q# 변환기에 대한 QASM을 만들어 QASM/Q# 개발자의 환경을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-325">Rolf Huisman ([@RolfHuisman](https://github.com/RolfHuisman)): Improved the experience for QASM/Q# developers by creating a QASM to Q# translator.</span></span> <span data-ttu-id="933ee-326">[PR #58](https://github.com/Microsoft/Quantum/pull/58).</span><span class="sxs-lookup"><span data-stu-id="933ee-326">[PR #58](https://github.com/Microsoft/Quantum/pull/58).</span></span>

* <span data-ttu-id="933ee-327">Andrew Helwer([@ahelwer](https://github.com/ahelwer)):  비지역 관련 퀀텀 게임인 CHSH 게임을 구현하는 샘플에 기여했습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-327">Andrew Helwer ([@ahelwer](https://github.com/ahelwer)):  Contributed a sample implementing the CHSH Game, a quantum game related to non-locality.</span></span>  <span data-ttu-id="933ee-328">[PR #84](https://github.com/Microsoft/Quantum/pull/84).</span><span class="sxs-lookup"><span data-stu-id="933ee-328">[PR #84](https://github.com/Microsoft/Quantum/pull/84).</span></span>

<span data-ttu-id="933ee-329">모두를 위해 설명서, 맞춤법 및 오타 수정 작업에 기여하여 콘텐츠를 개선해 주신 Rohit Gupta([@guptarohit](https://github.com/guptarohit),[PR #90](https://github.com/Microsoft/quantum/pull/90)), Tanaka Takayoshi([@tanaka-takayoshi](https://github.com/tanaka-takayoshi),[PR #289](https://github.com/MicrosoftDocs/quantum-docs-pr/pull/289)) 및 Lee James O'Riordan([@mlxd](https://github.com/mlxd),[PR #96](https://github.com/Microsoft/Quantum/pull/96)) 님께도 감사의 말씀을 드립니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-329">Thank you also to Rohit Gupta ([@guptarohit](https://github.com/guptarohit),[PR #90](https://github.com/Microsoft/quantum/pull/90)), Tanaka Takayoshi ([@tanaka-takayoshi](https://github.com/tanaka-takayoshi),[PR #289](https://github.com/MicrosoftDocs/quantum-docs-pr/pull/289)), and Lee James O'Riordan ([@mlxd](https://github.com/mlxd),[PR #96](https://github.com/Microsoft/Quantum/pull/96)) for their work improving the content for all of us through documentation, spelling and typo corrections!</span></span> 

## <a name="version-021809701"></a><span data-ttu-id="933ee-330">버전 0.2.1809.701</span><span class="sxs-lookup"><span data-stu-id="933ee-330">Version 0.2.1809.701</span></span>

<span data-ttu-id="933ee-331">릴리스 날짜:  2018년 9월 10일</span><span class="sxs-lookup"><span data-stu-id="933ee-331">*Release date: September 10, 2018*</span></span>

<span data-ttu-id="933ee-332">이 릴리스에는 커뮤니티에서 보고한</span><span class="sxs-lookup"><span data-stu-id="933ee-332">This release includes bug fixes for issues reported by the community.</span></span> <span data-ttu-id="933ee-333">다음 이슈 등에 대한 버그 수정이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-333">Including:</span></span>

* <span data-ttu-id="933ee-334">시프트 연산자를 사용할 수 없음([GitHub](https://github.com/Microsoft/Quantum/issues/75))</span><span class="sxs-lookup"><span data-stu-id="933ee-334">Unable to use shift operator ([GitHub](https://github.com/Microsoft/Quantum/issues/75)).</span></span>
* <span data-ttu-id="933ee-335">`DumpMachine` / `DumpRegister`가 콘솔에 인쇄될 때 `QCTraceSimulator`에서 실패함([UserVoice](https://quantum.uservoice.com/forums/906946/suggestions/34709680))</span><span class="sxs-lookup"><span data-stu-id="933ee-335">`DumpMachine` / `DumpRegister` fails on `QCTraceSimulator` when printing to console ([UserVoice](https://quantum.uservoice.com/forums/906946/suggestions/34709680)).</span></span>
* <span data-ttu-id="933ee-336">0큐비트 할당 허용([UserVoice](https://quantum.uservoice.com/forums/906208-q-language/suggestions/34768069-allow-allocating-0-qubits))</span><span class="sxs-lookup"><span data-stu-id="933ee-336">Allow allocating 0 qubits ([UserVoice](https://quantum.uservoice.com/forums/906208-q-language/suggestions/34768069-allow-allocating-0-qubits)).</span></span>
* <span data-ttu-id="933ee-337">`AssertQubitState`에 명시적 Complex() 호출이 필요함([UserVoice](https://quantum.uservoice.com/forums/906208-q-language/suggestions/34713733-assertqubitstate-requires-explicit-complex-call))</span><span class="sxs-lookup"><span data-stu-id="933ee-337">`AssertQubitState` requires explicit Complex() call ([UserVoice](https://quantum.uservoice.com/forums/906208-q-language/suggestions/34713733-assertqubitstate-requires-explicit-complex-call)).</span></span>
* <span data-ttu-id="933ee-338">`Measure` 작업이 macOS에서 항상 `One`을 반환함([UserVoice](https://quantum.uservoice.com/forums/906940/suggestions/35008546))</span><span class="sxs-lookup"><span data-stu-id="933ee-338">`Measure` operation always returns `One` on macOS ([UserVoice](https://quantum.uservoice.com/forums/906940/suggestions/35008546)).</span></span>

<span data-ttu-id="933ee-339">감사합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-339">Thanks!</span></span> 

## <a name="version-0218063001"></a><span data-ttu-id="933ee-340">버전 0.2.1806.3001</span><span class="sxs-lookup"><span data-stu-id="933ee-340">Version 0.2.1806.3001</span></span>

<span data-ttu-id="933ee-341">릴리스 날짜:  2018년 6월 30일</span><span class="sxs-lookup"><span data-stu-id="933ee-341">*Release date: June 30, 2018*</span></span>

<span data-ttu-id="933ee-342">이 릴리스는 [GitHub에 보고된 이슈 #48](https://github.com/Microsoft/Quantum/issues/48)에 대한 빠른 수정입니다(사용자 이름에 공백이 포함된 경우 Q# 컴파일이 실패함).</span><span class="sxs-lookup"><span data-stu-id="933ee-342">This releases is just a quick fix for [issue #48 reported on GitHub](https://github.com/Microsoft/Quantum/issues/48) (Q# compilation fails if user name contains a blank space).</span></span> <span data-ttu-id="933ee-343">해당하는 새 버전(`0.2.1806.3001-preview`)이 포함된 `0.2.1806.1503`과 같은 업데이트 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-343">Follow same update instructions as `0.2.1806.1503` with the corresponding new version (`0.2.1806.3001-preview`).</span></span>

## <a name="version-0218061503"></a><span data-ttu-id="933ee-344">버전 0.2.1806.1503</span><span class="sxs-lookup"><span data-stu-id="933ee-344">Version 0.2.1806.1503</span></span>

<span data-ttu-id="933ee-345">릴리스 날짜:  2018년 6월 22일</span><span class="sxs-lookup"><span data-stu-id="933ee-345">*Release date: June 22, 2018*</span></span>

<span data-ttu-id="933ee-346">이 릴리스에는 향상된 디버깅 환경 및 향상된 성능뿐 아니라 다양한 커뮤니티 기여도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-346">This release includes several community contributions as well as an improved debugging experience and improved performance.</span></span>  <span data-ttu-id="933ee-347">구체적으로 살펴보면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-347">Specifically:</span></span>

* <span data-ttu-id="933ee-348">QuantumSimulator 대상 머신에 대한 작고 큰 시뮬레이션에서 모두 성능이 향상됨</span><span class="sxs-lookup"><span data-stu-id="933ee-348">Performance improvements on both small and large simulations for the QuantumSimulator target machine.</span></span>
* <span data-ttu-id="933ee-349">향상된 디버깅 기능</span><span class="sxs-lookup"><span data-stu-id="933ee-349">Improved debugging functionality.</span></span>
* <span data-ttu-id="933ee-350">버그 수정, 새 도우미 함수, 작업 및 새 샘플의 커뮤니티 기여</span><span class="sxs-lookup"><span data-stu-id="933ee-350">Community contributions in bug fixes, new helper functions, operations and new samples.</span></span>

### <a name="performance-improvements"></a><span data-ttu-id="933ee-351">성능 개선</span><span class="sxs-lookup"><span data-stu-id="933ee-351">Performance improvements</span></span>

<span data-ttu-id="933ee-352">이 업데이트에는 모든 머신에서 많고 적은 큐비트의 상당한 성능 향상이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-352">This update includes significant performance improvements for simulation of large and small numbers of qubits for all the target machines.</span></span>  <span data-ttu-id="933ee-353">이 향상된 기능은 Quantum Development Kit에서 표준 샘플인 H<sub>2</sub> 시뮬레이션을 사용하여 쉽게 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-353">This improvement is easily visible with the H<sub>2</sub> simulation that is a standard sample in the Quantum Development Kit.</span></span>

### <a name="improved-debugging-functionality"></a><span data-ttu-id="933ee-354">향상된 디버깅 기능</span><span class="sxs-lookup"><span data-stu-id="933ee-354">Improved debugging functionality</span></span>

<span data-ttu-id="933ee-355">이 업데이트는 다음과 같은 새 디버깅 기능을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-355">This update adds new debugging functionality:</span></span>
* <span data-ttu-id="933ee-356">특정 시점에 대상 퀀텀 머신에 대한 wave 함수 정보를 출력하는 두 개의 새 작업 @"microsoft.quantum.extensions.diagnostics.dumpmachine" 및 @"microsoft.quantum.extensions.diagnostics.dumpregister"를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-356">Added two new operations,  @"microsoft.quantum.extensions.diagnostics.dumpmachine" and @"microsoft.quantum.extensions.diagnostics.dumpregister" that output wave function information about the target quantum machine at a point in time.</span></span>  
* <span data-ttu-id="933ee-357">Visual Studio에서는 단일 큐비트에서 $\ket{1}$를 측정할 확률이 이제 QuantumSimulator 대상 머신의 디버깅 창에 자동으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-357">In Visual Studio, the probability of measuring a $\ket{1}$ on a single qubit is now automatically shown in the debugging window for the QuantumSimulator target machine.</span></span>
* <span data-ttu-id="933ee-358">Visual Studio에서는 **Autos** 및 **Locals** 디버그 창에서 변수 속성 표시가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-358">In Visual Studio, improved the display of variable properties in the **Autos** and **Locals** debug windows.</span></span> 

<span data-ttu-id="933ee-359">[테스트 및 디버깅](xref:microsoft.quantum.techniques.testing-and-debugging)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-359">Learn more about [Testing and Debugging](xref:microsoft.quantum.techniques.testing-and-debugging).</span></span>

### <a name="community-contributions"></a><span data-ttu-id="933ee-360">커뮤니티 기여</span><span class="sxs-lookup"><span data-stu-id="933ee-360">Community Contributions</span></span>

<span data-ttu-id="933ee-361">Q# 코더 커뮤니티는 성장하고 있으며 http://github.com/Microsoft/quantum 에서 열려 있는 코드베이스에 제출된 첫 번째 사용자가 라이브러리 및 샘플에 기여해 주셔서 감사합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-361">The Q# coder community is growing and we are thrilled to see the first user contributed libraries and samples that were submitted to our open code base at http://github.com/Microsoft/quantum.</span></span>  <span data-ttu-id="933ee-362">다음 기여자분들께 \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="933ee-362">**A big Thank you!**</span></span> <span data-ttu-id="933ee-363">깊은 감사의 말씀을 드립니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-363">to the following contributors:</span></span>
* <span data-ttu-id="933ee-364">Mathias Soeken([@msoeken](https://github.com/msoeken)): 지정된 순열을 구현하도록 Toffoli 네트워크를 생성하는 변환 기반 논리 합성 메서드를 정의하는 샘플에 기여했습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-364">Mathias Soeken ([@msoeken](https://github.com/msoeken)):  contributed a sample defining a transformation based logic synthesis method that constructs Toffoli networks to implement a given permutation.</span></span> <span data-ttu-id="933ee-365">이 코드는 전체적으로 Q# 함수 및 작업으로 작성됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-365">The code is written entirely in Q# functions and operations.</span></span>  <span data-ttu-id="933ee-366">[PR #41](https://github.com/Microsoft/Quantum/pull/41).</span><span class="sxs-lookup"><span data-stu-id="933ee-366">[PR #41](https://github.com/Microsoft/Quantum/pull/41).</span></span>
* <span data-ttu-id="933ee-367">RolfHuisman([@RolfHuisman](https://github.com/RolfHuisman)): Microsoft MVP Rolf Huisman은 클래식 제어 흐름 및 제한된 퀀텀 작업이 포함되지 않은 제한된 프로그램 클래스에 대한 Q# 코드에서 플랫 QASM 코드를 생성하는 샘플에 기여했습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-367">RolfHuisman ([@RolfHuisman](https://github.com/RolfHuisman)): Microsoft MVP Rolf Huisman contributed a sample that generates flat QASM code from Q# code for a restricted class of programs that do not have classical control flow and restricted quantum operations.</span></span> [<span data-ttu-id="933ee-368">PR #59</span><span class="sxs-lookup"><span data-stu-id="933ee-368">PR #59</span></span>](https://github.com/Microsoft/Quantum/pull/59)
* <span data-ttu-id="933ee-369">Sarah Kasier([@crazy4pi314](https://github.com/crazy4pi314)): 제어된 작업에 대한 라이브러리 함수를 제출하여 코드베이스를 개선하도록 도왔습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-369">Sarah Kasier ([@crazy4pi314](https://github.com/crazy4pi314)): helped to improve our code base by submitting a library function for controlled operations.</span></span> [<span data-ttu-id="933ee-370">PR #53</span><span class="sxs-lookup"><span data-stu-id="933ee-370">PR #53</span></span>](https://github.com/Microsoft/Quantum/pull/53)
* <span data-ttu-id="933ee-371">Jessica Lemieux([@Lemj3111](https://github.com/Lemj3111)): @"microsoft.quantum.canon.quantumphaseestimation"을 수정하고 새 단위 테스트를 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-371">Jessica Lemieux ([@Lemj3111](https://github.com/Lemj3111)): fixed @"microsoft.quantum.canon.quantumphaseestimation" and created new unit tests.</span></span>  [<span data-ttu-id="933ee-372">PR #54</span><span class="sxs-lookup"><span data-stu-id="933ee-372">PR #54</span></span>](https://github.com/Microsoft/Quantum/pull/54)
* <span data-ttu-id="933ee-373">Tama McGlinn([@TamaHobbit](https://github.com/TamaHobbit)): QuantumSimulator 인스턴스가 삭제되었는지 확인하여 Teleportation 샘플을 정리했습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-373">Tama McGlinn ([@TamaHobbit](https://github.com/TamaHobbit)): cleaned the Teleportation sample by making sure the QuantumSimulator instance is disposed.</span></span> [<span data-ttu-id="933ee-374">PR #20</span><span class="sxs-lookup"><span data-stu-id="933ee-374">PR #20</span></span>](https://github.com/Microsoft/Quantum/pull/20)

<span data-ttu-id="933ee-375">또한 \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="933ee-375">Additionally, a big **Thank You!**</span></span> <span data-ttu-id="933ee-376">Commercial Engineering Services 팀의 기여자로서 Hackathon이 진행되는 동안 설명서에 중요한 변경 내용을 제공해 주신 다음 Microsoft 소프트웨어 엔지니어분들께도 깊은 감사의 말씀을 드립니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-376">to these Microsoft Software Engineers from the Commercial Engineering Services team contributors who made valuable changes to our documentation during their Hackathon.</span></span>  <span data-ttu-id="933ee-377">해당 변경 내용은 모두를 위한 설명 및 온보딩 환경을 크게 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-377">Their changes vastly improved the clarity and onboarding experience for all of us:</span></span>
* <span data-ttu-id="933ee-378">Sascha Corti</span><span class="sxs-lookup"><span data-stu-id="933ee-378">Sascha Corti</span></span>
* <span data-ttu-id="933ee-379">Mihaela Curmei</span><span class="sxs-lookup"><span data-stu-id="933ee-379">Mihaela Curmei</span></span>
* <span data-ttu-id="933ee-380">John Donnelly</span><span class="sxs-lookup"><span data-stu-id="933ee-380">John Donnelly</span></span>
* <span data-ttu-id="933ee-381">Kirill Logachev</span><span class="sxs-lookup"><span data-stu-id="933ee-381">Kirill Logachev</span></span>
* <span data-ttu-id="933ee-382">Jan Pospisil</span><span class="sxs-lookup"><span data-stu-id="933ee-382">Jan Pospisil</span></span>
* <span data-ttu-id="933ee-383">Anita Ramanan</span><span class="sxs-lookup"><span data-stu-id="933ee-383">Anita Ramanan</span></span>
* <span data-ttu-id="933ee-384">Frances Tibble</span><span class="sxs-lookup"><span data-stu-id="933ee-384">Frances Tibble</span></span>
* <span data-ttu-id="933ee-385">Alessandro Vozza</span><span class="sxs-lookup"><span data-stu-id="933ee-385">Alessandro Vozza</span></span>

### <a name="update-existing-projects"></a><span data-ttu-id="933ee-386">기존 프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="933ee-386">Update existing projects</span></span>

<span data-ttu-id="933ee-387">이 릴리스는 이전 버전과 완벽하게 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-387">This release is fully backwards compatible.</span></span> <span data-ttu-id="933ee-388">프로젝트의 nuget 패키지를 버전 `0.2.1806.1503-preview`로 업데이트하고 모든 중간 파일이 다시 생성되도록 **전체 다시 빌드**를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-388">Just update the nuget pakages in your projects to version `0.2.1806.1503-preview` and do a **full rebuild** to make sure all intermediate files are regenerated.</span></span>

<span data-ttu-id="933ee-389">Visual Studio에서 [패키지 업데이트](https://docs.microsoft.com/nuget/tools/package-manager-ui#updating-a-package) 방법에 대한 일반적인 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-389">From Visual Studio, follow the normal instructions on how to [update a package](https://docs.microsoft.com/nuget/tools/package-manager-ui#updating-a-package).</span></span>

<span data-ttu-id="933ee-390">명령줄에 대한 프로젝트 템플릿을 업데이트하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-390">To update project templates for the command line, run the following command:</span></span>
```
dotnet new -i "Microsoft.Quantum.ProjectTemplates::0.2.1806.1503-preview"
```

<span data-ttu-id="933ee-391">이 명령을 실행한 후 `dotnet new <project-type> -lang Q#`을 사용하여 생성된 새 프로젝트는 자동으로 이 버전의 Quantum Development Kit를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-391">After running this command, any new projects created using `dotnet new <project-type> -lang Q#` will automatically use this version of the Quantum Development Kit.</span></span>

<span data-ttu-id="933ee-392">최신 버전을 사용하도록 기존 프로젝트를 업데이트하려면 각 프로젝트의 디렉터리 내에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-392">To update an existing project to use the newest version, run the following command from within the directory for each project:</span></span>

```
dotnet add package Microsoft.Quantum.Development.Kit -v "0.2.1806.1503-preview"
dotnet add package Microsoft.Quantum.Canon -v "0.2.1806.1503-preview"
```

<span data-ttu-id="933ee-393">또한 기존 프로젝트에서 유닛 테스트에 XUnit 통합을 사용하는 경우 유사한 명령을 사용하여 해당 패키지를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-393">If an existing project also uses XUnit integration for unit testing, then a similar command can be used to update that package as well:</span></span>
```
dotnet add package Microsoft.Quantum.Xunit -v "0.2.1806.1503-preview"
```

<span data-ttu-id="933ee-394">테스트 프로젝트에서 사용하는 XUnit 버전에 따라 XUnit을 2.3.1로 업데이트해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-394">Depending on the version of XUnit that your test project uses, you may also need to update XUnit to 2.3.1:</span></span>
```
dotnet add package xunit -v "2.3.1" 
```

<span data-ttu-id="933ee-395">업데이트한 후에는 다음을 수행하여 이전 버전에서 생성된 모든 임시 파일을 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-395">After the update, make sure you remove all temporary files generated by the previous version by doing:</span></span>
```
dotnet clean 
```

### <a name="known-issues"></a><span data-ttu-id="933ee-396">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="933ee-396">Known Issues</span></span>

<span data-ttu-id="933ee-397">보고할 알려진 추가 이슈가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-397">No aditional known issues to report.</span></span>


## <a name="version-0218022202"></a><span data-ttu-id="933ee-398">버전 0.2.1802.2202</span><span class="sxs-lookup"><span data-stu-id="933ee-398">Version 0.2.1802.2202</span></span>

<span data-ttu-id="933ee-399">릴리스 날짜:  2018년 2월 26일</span><span class="sxs-lookup"><span data-stu-id="933ee-399">*Release date: February 26, 2018*</span></span>

<span data-ttu-id="933ee-400">이 릴리스에서는 더 많은 플랫폼, 언어 상호 운용성 및 성능 향상에 대한 개발을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-400">This release brings support for development on more platforms, language interoperability, and performance enhancements.</span></span> <span data-ttu-id="933ee-401">구체적으로 살펴보면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-401">Specifically:</span></span>

- <span data-ttu-id="933ee-402">macOS 및 Linux 기반 개발 지원</span><span class="sxs-lookup"><span data-stu-id="933ee-402">Support for macOS- and Linux-based development.</span></span> 
- <span data-ttu-id="933ee-403">플랫폼 간 Visual Studio Code 지원을 포함한 .NET Core 호환성</span><span class="sxs-lookup"><span data-stu-id="933ee-403">.NET Core compatibility, including support for Visual Studio Code across platforms.</span></span>
- <span data-ttu-id="933ee-404">Quantum Development Kit 라이브러리의 전체 오픈 소스 라이선스</span><span class="sxs-lookup"><span data-stu-id="933ee-404">A full Open Source license for the Quantum Development Kit Libraries.</span></span>
- <span data-ttu-id="933ee-405">20개 이상의 큐비트가 필요한 프로젝트에서 시뮬레이터 성능을 개선함</span><span class="sxs-lookup"><span data-stu-id="933ee-405">Improved simulator performance on projects requiring 20 or more qubits.</span></span>
- <span data-ttu-id="933ee-406">Python 언어와 상호 운용성(Windows에서 사용할 수 있는 미리 보기 릴리스)</span><span class="sxs-lookup"><span data-stu-id="933ee-406">Interoperability with the Python language (preview release available on Windows).</span></span>

### <a name="net-editions"></a><span data-ttu-id="933ee-407">.NET 버전</span><span class="sxs-lookup"><span data-stu-id="933ee-407">.NET Editions</span></span>

<span data-ttu-id="933ee-408">.NET 플랫폼은 두 가지 버전인, Windows와 함께 제공되는 .NET Framework 및 Windows, macOS 및 Linux에서 사용 가능한 오픈 소스 .NET Core를 통해 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-408">The .NET platform is available through two different editions, the .NET Framework that is provided with Windows, and the open-source .NET Core that is available on Windows, macOS and Linux.</span></span>
<span data-ttu-id="933ee-409">이 릴리스에서는 대부분의 Quantum Development Kit 부분이 Framework 및 Core에 공통적인 클래스 세트인 .NET Standard용 라이브러리로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-409">With this release, most parts of the Quantum Development Kit are provided as libraries for .NET Standard, the set of classes common to both Framework and Core.</span></span>
<span data-ttu-id="933ee-410">따라서 이 라이브러리는 최신 버전의 .NET Framework 또는 .NET Core와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-410">These libraries are therefore compatible with recent versions of either .NET Framework or .NET Core.</span></span>

<span data-ttu-id="933ee-411">따라서 Quantum Development Kit를 사용하여 작성된 프로젝트를 최대한 이식 가능하게 하려면 Quantum Development Kit를 사용하여 작성된 라이브러리 프로젝트의 대상을 .NET Standard로 지정하지만 콘솔 애플리케이션의 대상을 .NET Core로 지정하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-411">Thus, to help ensure that projects written using the Quantum Development Kit are as portable as possible, we recommend that library projects written using the Quantum Development Kit target .NET Standard, while console applications target .NET Core.</span></span>
<span data-ttu-id="933ee-412">이전 릴리스의 Quantum Development Kit는 .NET Framework만 지원했으므로 기존 프로젝트를 마이그레이션해야 할 수 있습니다. 이 작업을 수행하는 방법에 대한 자세한 내용은 아래를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-412">Since previous releases of the Quantum Development Kit only supported .NET Framework, you may need to migrate your existing projects; see below for details on how to do this.</span></span>

### <a name="project-migration"></a><span data-ttu-id="933ee-413">프로젝트 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="933ee-413">Project Migration</span></span>

<span data-ttu-id="933ee-414">이전 버전의 Quantum Development Kit를 사용하여 만든 프로젝트에서 사용된 NuGet 패키지를 업데이트하지 않는 한 해당 프로젝트는 계속 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-414">Projects created using previous versions of Quantum Development Kit will still work, as long as you don't update the NuGet packages used in them.</span></span> <span data-ttu-id="933ee-415">기존 코드를 새 버전으로 마이그레이션하려면 다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-415">To migrate existing code to the new version, perform the following steps:</span></span>
1. <span data-ttu-id="933ee-416">올바른 형식의 Q# 프로젝트 템플릿(애플리케이션, 라이브러리 또는 테스트 프로젝트)을 사용하여 새 .NET Core 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-416">Create a new .NET Core project using the right type of Q# project template (Application, Library or Test Project).</span></span>
2. <span data-ttu-id="933ee-417">이전 프로젝트에서 새 프로젝트로 기존 .qs 및 .cs/.fs 파일을 복사합니다([추가] > [기존 항목] 사용).</span><span class="sxs-lookup"><span data-stu-id="933ee-417">Copy existing .qs and .cs/.fs files from the old project to the new project (using Add > Existing Item).</span></span> <span data-ttu-id="933ee-418">AssemblyInfo.cs 파일을 복사하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-418">Do not copy the AssemblyInfo.cs file.</span></span>
3. <span data-ttu-id="933ee-419">새 프로젝트를 빌드하고 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-419">Build and run the new project.</span></span>

<span data-ttu-id="933ee-420">Microsoft.Quantum.Canon 네임스페이스의 RandomWalkPhaseEstimation 작업은 [Microsoft/Quantum-NC](https://github.com/microsoft/quantum-nc) 리포지토리의 Microsoft.Research.Quantum.RandomWalkPhaseEstimation 네임스페이스로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-420">Please note that the operation RandomWalkPhaseEstimation from the namespace Microsoft.Quantum.Canon was moved into the namespace Microsoft.Research.Quantum.RandomWalkPhaseEstimation in the [Microsoft/Quantum-NC](https://github.com/microsoft/quantum-nc) repository.</span></span>

### <a name="known-issues"></a><span data-ttu-id="933ee-421">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="933ee-421">Known Issues</span></span>

- <span data-ttu-id="933ee-422">Q#으로 작성된 테스트에서는 `--filter`에 대한 `dotnet test` 옵션이 제대로 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-422">The `--filter` option to `dotnet test` does not work correctly for tests written in Q#.</span></span>
  <span data-ttu-id="933ee-423">따라서 Visual Studio Code에서 개별 단위 테스트를 실행할 수 없습니다. 명령줄에서 `dotnet test`를 사용하여 모든 테스트를 다시 실행하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-423">As a result, individual unit tests cannot be run in Visual Studio Code; we recommend using `dotnet test` at the command line to re-run all tests.</span></span>

## <a name="version-0118011707"></a><span data-ttu-id="933ee-424">버전 0.1.1801.1707</span><span class="sxs-lookup"><span data-stu-id="933ee-424">Version 0.1.1801.1707</span></span>

<span data-ttu-id="933ee-425">릴리스 날짜:  2018년 1월 18일</span><span class="sxs-lookup"><span data-stu-id="933ee-425">*Release date: January 18, 2018*</span></span>

<span data-ttu-id="933ee-426">이 릴리스에서는 커뮤니티에서 보고한 일부 이슈를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-426">This release fixes some issues reported by the community.</span></span> <span data-ttu-id="933ee-427">구체적으로는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-427">Namely:</span></span>

- <span data-ttu-id="933ee-428">이제 시뮬레이터는 초기 AVX 사용 가능 CPU 이외의 CPU를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-428">The simulator now works with early non-AVX-enabled CPUs.</span></span>
- <span data-ttu-id="933ee-429">국가별 10진수 설정으로 인해 Q# 파서가 실패하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-429">Regional decimal settings will not cause the Q# parser to fail.</span></span>
- <span data-ttu-id="933ee-430">`SignD` 기본 작업은 이제 `Double`이 아닌 `Int`을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-430">`SignD` primitive operation now returns `Int` rather than `Double`.</span></span>


## <a name="version-011712901"></a><span data-ttu-id="933ee-431">버전 0.1.1712.901</span><span class="sxs-lookup"><span data-stu-id="933ee-431">Version 0.1.1712.901</span></span>

<span data-ttu-id="933ee-432">릴리스 날짜:  2017년 12월 11일</span><span class="sxs-lookup"><span data-stu-id="933ee-432">*Release date: December 11, 2017*</span></span>

### <a name="known-issues"></a><span data-ttu-id="933ee-433">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="933ee-433">Known Issues</span></span>

#### <a name="hardware-and-software-requirements"></a><span data-ttu-id="933ee-434">하드웨어 및 소프트웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="933ee-434">Hardware and Software Requirements</span></span>

- <span data-ttu-id="933ee-435">Quantum Development Kit에 포함된 시뮬레이터를 사용하려면 Microsoft Windows의 64비트 설치를 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-435">The simulator included with the Quantum Development Kit requires a 64-bit installation of Microsoft Windows to run.</span></span>
- <span data-ttu-id="933ee-436">Quantum Development Kit와 함께 설치되는 Microsoft의 퀀텀 시뮬레이터에서는 AVX(Advanced Vector Extensions)를 활용하며 AVX 사용 가능 CPU가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-436">Microsoft's quantum simulator, installed with the Quantum Development Kit, utilizes Advanced Vector Extensions (AVX), and requires an AVX-enabled CPU.</span></span> <span data-ttu-id="933ee-437">Q1 2011(Sandy Bridge) 이상에서 제공되는 Intel 프로세서는 AVX를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-437">Intel processors shipped in Q1 2011 (Sandy Bridge) or later support AVX.</span></span> <span data-ttu-id="933ee-438">초기 CPU에 대한 지원을 평가하고 나중에 세부 정보를 발표할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-438">We are evaluating support for earlier CPUs and may announce details at a later time.</span></span>

#### <a name="project-creation"></a><span data-ttu-id="933ee-439">프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="933ee-439">Project Creation</span></span>

- <span data-ttu-id="933ee-440">Q#을 사용할 솔루션(.sln)을 만드는 경우 이 솔루션은 솔루션의 각 프로젝트(.csproj) 보다 높은 수준의 단일 디렉터리여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-440">When creating a solution (.sln) that will use Q#, the solution must be one directory higher than each project (.csproj) in the solution.</span></span> <span data-ttu-id="933ee-441">새 솔루션을 만드는 경우 “새 프로젝트” 대화 상자에서 “솔루션용 디렉터리 만들기” 확인란이 선택되었는지 확인하여 이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-441">When creating a new solution, this can be accomplished by making sure that the "Create directory for solution" checkbox on the "New Project" dialog box is checked.</span></span> <span data-ttu-id="933ee-442">이 작업을 수행하지 않으면 Quantum Development Kit NuGet 패키지를 수동으로 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-442">If this is not done, the Quantum Development Kit NuGet packages will need to be installed manually.</span></span>

#### <a name="q"></a><span data-ttu-id="933ee-443">Q#</span><span class="sxs-lookup"><span data-stu-id="933ee-443">Q#</span></span>

- <span data-ttu-id="933ee-444">Intellisense는 Q# 코드에 대한 적절한 오류를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-444">Intellisense does not display proper errors for Q# code.</span></span> <span data-ttu-id="933ee-445">올바른 Q# 오류를 보려면 Visual Studio 오류 목록에 빌드 오류가 표시되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-445">Make sure that you are displaying Build errors in the Visual Studio Error List to see correct Q# errors.</span></span> <span data-ttu-id="933ee-446">또한 빌드를 완료한 후에도 Q# 오류는 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-446">Also note that Q# errors will not show up until after you've done a build.</span></span>
- <span data-ttu-id="933ee-447">부분 애플리케이션에서 변경 가능한 배열을 사용하면 예기치 않은 동작이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-447">Using a mutable array in a partial application may lead to unexpected behavior.</span></span>
- <span data-ttu-id="933ee-448">변경할 수 없는 배열을 변경 가능한 배열에 바인딩하면(a = b로 설정, 여기서 b는 변경 가능한 배열) 예기치 않은 동작이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-448">Binding an immutable array to a mutable array (let a = b, where b is a mutable array) may lead to unexpected behavior.</span></span>
- <span data-ttu-id="933ee-449">프로파일링, 코드 검사 및 기타 VS 플러그 인이 항상 Q# 줄 및 블록을 정확하게 계산하는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-449">Profiling, code coverage and other VS plugins may not always count Q# lines and blocks accurately.</span></span>
- <span data-ttu-id="933ee-450">Q# 컴파일러는 보간된 문자열의 유효성을 검사하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-450">The Q# compiler does not validate interpolated strings.</span></span> <span data-ttu-id="933ee-451">Q# 보간된 문자열에서 식을 사용하거나 철자가 잘못된 변수 이름을 사용하여 C# 컴파일 오류를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-451">It is possible to create C# compilation errors by misspelling variable names or using expressions in Q# interpolated strings.</span></span>

#### <a name="simulation"></a><span data-ttu-id="933ee-452">시뮬레이션</span><span class="sxs-lookup"><span data-stu-id="933ee-452">Simulation</span></span>

- <span data-ttu-id="933ee-453">퀀텀 시뮬레이터는 OpenMP를 사용하여 필요한 선형 대수를 병렬로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-453">The Quantum Simulator uses OpenMP to parallelize the linear algebra required.</span></span> <span data-ttu-id="933ee-454">기본적으로 OpenMP는 사용 가능한 모든 하드웨어 스레드를 사용합니다. 즉, 필요한 조정이 실제 작업을 방해하기 때문에 적은 수의 큐비트를 포함하는 프로그램이 느리게 실행되는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-454">By default OpenMP uses all available hardware threads, which means that programs with small numbers of qubits will often run slowly because the coordination required will dwarf the actual work.</span></span> <span data-ttu-id="933ee-455">환경 변수 OMP_NUM_THREADS를 작은 수로 설정하여 이 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-455">This can be fixed by setting the environment variable OMP_NUM_THREADS to a small number.</span></span> <span data-ttu-id="933ee-456">대략적으로 스레드 1개는 최대 4개 정도의 큐비트에 적합하며 알고리즘에 따라 많이 달라지지만 큐비트당 추가 스레드가 적합합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-456">As a very rough rule of thumb, 1 thread is good for up to about 4 qubits, and then an additional thread per qubit is good, although this is highly dependent on your algorithm.</span></span>

#### <a name="debugging"></a><span data-ttu-id="933ee-457">디버그</span><span class="sxs-lookup"><span data-stu-id="933ee-457">Debugging</span></span>

- <span data-ttu-id="933ee-458">F11(한 단계씩 코드 실행)은 Q# 코드에서 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-458">F11 (step in) doesn't work in Q# code.</span></span>
- <span data-ttu-id="933ee-459">중단점 및 단일 단계 일시 중지에서 Q# 코드의 코드 강조 표시는 정확하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-459">Code highlighting in Q# code at a breakpoint or single-step pause is sometimes inaccurate.</span></span> <span data-ttu-id="933ee-460">올바른 줄이 강조 표시되지만 때때로 강조 표시가 줄의 잘못된 열에서 시작 및 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-460">The correct line will be highlighted, but sometimes the highlight will start and end at incorrect columns on the line.</span></span>

#### <a name="testing"></a><span data-ttu-id="933ee-461">테스트</span><span class="sxs-lookup"><span data-stu-id="933ee-461">Testing</span></span>

- <span data-ttu-id="933ee-462">테스트는 64비트 모드로 실행되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-462">Tests must be executed in 64-bit mode.</span></span> <span data-ttu-id="933ee-463">BadImageFormatException으로 인해 테스트에 실패한 경우 [테스트] 메뉴로 이동하고 [테스트 설정] > [기본 프로세서 아키텍처] > [X64]를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-463">If your tests are failing with a BadImageFormatException, go to the Test menu and select Test Settings > Default Processor Architecture > X64.</span></span>
- <span data-ttu-id="933ee-464">일부 테스트는 실행하는 데 오랜 시간이 걸립니다(컴퓨터에 따라 5분 정도 걸릴 수 있음).</span><span class="sxs-lookup"><span data-stu-id="933ee-464">Some tests take a long time (possibly as much as 5 minutes depending on your computer) to run.</span></span> <span data-ttu-id="933ee-465">일부 테스트에서는 20개 이상의 큐비트를 사용하므로 정상적인 상황입니다. 현재 가장 큰 테스트는 23개의 큐비트에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-465">This is normal, as some use over twenty qubits; our largest test currently runs on 23 qubits.</span></span>

#### <a name="samples"></a><span data-ttu-id="933ee-466">샘플</span><span class="sxs-lookup"><span data-stu-id="933ee-466">Samples</span></span>

- <span data-ttu-id="933ee-467">일부 머신에서는 환경 변수 OMP_NUM_THREADS가 “1”로 설정된 경우가 아니면 일부 작은 샘플이 느리게 실행될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-467">On some machines, some small samples may run slowly unless the environment variable OMP_NUM_THREADS is set to "1".</span></span> <span data-ttu-id="933ee-468">또한 “시뮬레이션”에서 릴리스 정보를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933ee-468">See also the release note under "Simulation".</span></span>

#### <a name="libraries"></a><span data-ttu-id="933ee-469">라이브러리</span><span class="sxs-lookup"><span data-stu-id="933ee-469">Libraries</span></span>

- <span data-ttu-id="933ee-470">서로 다른 인수로 작업에 전달된 큐비트는 모두 개별 큐비트라고 암시적으로 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-470">There is an implicit assumption that the qubits passed to an operation in different arguments are all distinct.</span></span> <span data-ttu-id="933ee-471">예를 들어 모든 라이브러리 작업(및 모든 시뮬레이터)은 제어된 NOT에 전달된 두 개의 큐비트는 서로 다른 큐비트라고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-471">For instance, all of the library operations (and all of the simulators) assume that the two qubits passed to a controlled NOT are different qubits.</span></span> <span data-ttu-id="933ee-472">이 가정에 위배되면 예기치 않은 결과가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-472">Violating this assumption may lead to unpredictable unexpected.</span></span> <span data-ttu-id="933ee-473">퀀텀 컴퓨터 추적 프로그램 시뮬레이터를 사용하여 이를 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-473">It is possible to test for this using the quantum computer tracer simulator.</span></span>
- <span data-ttu-id="933ee-474">Microsoft.Quantum.Bind 함수는 경우에 따라 예상대로 작동하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-474">The Microsoft.Quantum.Bind function may not act as expected in all cases.</span></span>
- <span data-ttu-id="933ee-475">Microsoft.Quantum.Extensions.Math 네임스페이스에서 SignD 함수는 Int가 아니라 Double을 반환합니다. 단, 기본 System.Math.Sign 함수는 항상 정수를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-475">In the Microsoft.Quantum.Extensions.Math namespace, the SignD function returns a Double rather than an Int, although the underlying System.Math.Sign function always returns an integer.</span></span> <span data-ttu-id="933ee-476">이 double은 모두 정확한 이진 표현을 포함하므로 1.0, -1.0 및 0.0에 결과를 비교하는 것이 안전합니다.</span><span class="sxs-lookup"><span data-stu-id="933ee-476">It is safe to compare the result against 1.0, -1.0, and 0.0, since these doubles all have exact binary representations.</span></span>
