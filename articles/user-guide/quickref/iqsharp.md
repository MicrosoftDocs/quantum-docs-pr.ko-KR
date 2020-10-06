---
title: '- Q# 매직 명령'
description: Q#Jupyter 노트북을 사용 하는 매직 명령에 대 한 빠른 참조 페이지 Q#
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
uid: microsoft.quantum.guide.quickref.iqsharp
no-loc:
- Q#
- $$v
ms.openlocfilehash: 4549afb84bf0084160079e3cef3a7f94dffcda3e
ms.sourcegitcommit: d98190988ff03146d9ca2b0d325870cd717d729a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/06/2020
ms.locfileid: "91771342"
---
# <a name="ino-locq-magic-commands"></a><span data-ttu-id="65ebd-103">- Q# 매직 명령</span><span class="sxs-lookup"><span data-stu-id="65ebd-103">IQ# Magic Commands</span></span>

### <a name="general"></a><span data-ttu-id="65ebd-104">일반</span><span class="sxs-lookup"><span data-stu-id="65ebd-104">General</span></span>

- <span data-ttu-id="65ebd-105">[`%config`](xref:microsoft.quantum.iqsharp.magic-ref.config): 구성 옵션을 설정 하거나 쿼리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-105">[`%config`](xref:microsoft.quantum.iqsharp.magic-ref.config): Allows setting or querying configuration options.</span></span>
- <span data-ttu-id="65ebd-106">[`%estimate`](xref:microsoft.quantum.iqsharp.magic-ref.estimate): ResourcesEstimator 대상 컴퓨터에서 지정 된 함수 또는 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-106">[`%estimate`](xref:microsoft.quantum.iqsharp.magic-ref.estimate): Runs a given function or operation on the ResourcesEstimator target machine.</span></span>
- <span data-ttu-id="65ebd-107">[`%lsmagic`](xref:microsoft.quantum.iqsharp.magic-ref.lsmagic): 현재 사용할 수 있는 모든 매직 명령의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-107">[`%lsmagic`](xref:microsoft.quantum.iqsharp.magic-ref.lsmagic): Returns a list of all currently available magic commands.</span></span>
- <span data-ttu-id="65ebd-108">[`%lsopen`](xref:microsoft.quantum.iqsharp.magic-ref.lsopen): 현재 열린 네임 스페이스 및 해당 별칭을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-108">[`%lsopen`](xref:microsoft.quantum.iqsharp.magic-ref.lsopen): Lists currently opened namespaces and their aliases.</span></span>
- <span data-ttu-id="65ebd-109">[`%package`](xref:microsoft.quantum.iqsharp.magic-ref.package): NuGet 패키지를 로드 하는 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-109">[`%package`](xref:microsoft.quantum.iqsharp.magic-ref.package): Provides the ability to load a NuGet package.</span></span>
- <span data-ttu-id="65ebd-110">[`%performance`](xref:microsoft.quantum.iqsharp.magic-ref.performance):이 커널에 대 한 현재 성능 메트릭을 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-110">[`%performance`](xref:microsoft.quantum.iqsharp.magic-ref.performance): Reports current performance metrics for this kernel.</span></span>
- <span data-ttu-id="65ebd-111">[`%project`](xref:microsoft.quantum.iqsharp.magic-ref.project): 프로젝트 참조를 보거나 추가 하는 기능을 제공 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="65ebd-111">[`%project`](xref:microsoft.quantum.iqsharp.magic-ref.project): Provides the ability to view or add Q# project references.</span></span> 
- <span data-ttu-id="65ebd-112">[`%simulate`](xref:microsoft.quantum.iqsharp.magic-ref.simulate): QuantumSimulator 대상 컴퓨터에서 지정 된 함수 또는 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-112">[`%simulate`](xref:microsoft.quantum.iqsharp.magic-ref.simulate): Runs a given function or operation on the QuantumSimulator target machine.</span></span>
- <span data-ttu-id="65ebd-113">[`%toffoli`](xref:microsoft.quantum.iqsharp.magic-ref.toffoli): ToffoliSimulator 대상 컴퓨터에서 지정 된 함수 또는 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-113">[`%toffoli`](xref:microsoft.quantum.iqsharp.magic-ref.toffoli): Runs a given function or operation on the ToffoliSimulator target machine.</span></span>
- <span data-ttu-id="65ebd-114">[`%who`](xref:microsoft.quantum.iqsharp.magic-ref.who): Q# 현재 세션에서 사용할 수 있는 작업을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-114">[`%who`](xref:microsoft.quantum.iqsharp.magic-ref.who): Lists the Q# operations available in the current session.</span></span>
- <span data-ttu-id="65ebd-115">[`%workspace`](xref:microsoft.quantum.iqsharp.magic-ref.workspace): 현재 작업 영역과 관련 된 작업을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-115">[`%workspace`](xref:microsoft.quantum.iqsharp.magic-ref.workspace): Provides actions related to the current workspace.</span></span>

### <a name="azure-quantum-integration"></a><span data-ttu-id="65ebd-116">Azure 퀀텀 통합</span><span class="sxs-lookup"><span data-stu-id="65ebd-116">Azure Quantum integration</span></span>

- <span data-ttu-id="65ebd-117">[`%azure.connect`](xref:microsoft.quantum.iqsharp.magic-ref.azure.connect): Azure 퀀텀 작업 영역에 연결 하거나 현재 연결 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-117">[`%azure.connect`](xref:microsoft.quantum.iqsharp.magic-ref.azure.connect): Connects to an Azure Quantum workspace or displays current connection status.</span></span>
- <span data-ttu-id="65ebd-118">[`%azure.execute`](xref:microsoft.quantum.iqsharp.magic-ref.azure.execute): Azure 퀀텀 작업 영역에 작업을 제출 하 고 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-118">[`%azure.execute`](xref:microsoft.quantum.iqsharp.magic-ref.azure.execute): Submits a job to an Azure Quantum workspace and waits for completion.</span></span>
- <span data-ttu-id="65ebd-119">[`%azure.jobs`](xref:microsoft.quantum.iqsharp.magic-ref.azure.jobs): 현재 Azure 퀀텀 작업 영역에서 작업 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-119">[`%azure.jobs`](xref:microsoft.quantum.iqsharp.magic-ref.azure.jobs): Displays a list of jobs in the current Azure Quantum workspace.</span></span>
- <span data-ttu-id="65ebd-120">[`%azure.output`](xref:microsoft.quantum.iqsharp.magic-ref.azure.output): 현재 Azure 퀀텀 작업 영역에서 작업에 대 한 결과를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-120">[`%azure.output`](xref:microsoft.quantum.iqsharp.magic-ref.azure.output): Displays results for a job in the current Azure Quantum workspace.</span></span>
- <span data-ttu-id="65ebd-121">[`%azure.status`](xref:microsoft.quantum.iqsharp.magic-ref.azure.status): 현재 Azure 퀀텀 작업 영역에서 작업의 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-121">[`%azure.status`](xref:microsoft.quantum.iqsharp.magic-ref.azure.status): Displays status for a job in the current Azure Quantum workspace.</span></span>
- <span data-ttu-id="65ebd-122">[`%azure.submit`](xref:microsoft.quantum.iqsharp.magic-ref.azure.submit): Azure 퀀텀 작업 영역에 작업을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-122">[`%azure.submit`](xref:microsoft.quantum.iqsharp.magic-ref.azure.submit): Submits a job to an Azure Quantum workspace.</span></span>
- <span data-ttu-id="65ebd-123">[`%azure.target`](xref:microsoft.quantum.iqsharp.magic-ref.azure.target): Q# Azure 퀀텀 작업 영역에서 작업 제출에 대 한 활성 실행 대상을 설정 하거나 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-123">[`%azure.target`](xref:microsoft.quantum.iqsharp.magic-ref.azure.target): Sets or displays the active run target for Q# job submission in an Azure Quantum workspace.</span></span>

### <a name="chemistry-from-microsoftquantumchemistry-package"></a><span data-ttu-id="65ebd-124">화학 (Microsoft.</span><span class="sxs-lookup"><span data-stu-id="65ebd-124">Chemistry (from Microsoft.Quantum.Chemistry package)</span></span>

- <span data-ttu-id="65ebd-125">[`%chemistry.broombridge`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.broombridge): 지정 된 .yaml 파일에서 Broombridge 전자적 구조 문제 표현을 로드 하 고 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-125">[`%chemistry.broombridge`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.broombridge): Loads and returns Broombridge electronic structure problem representation from a given .yaml file.</span></span>
- <span data-ttu-id="65ebd-126">[`%chemistry.encode`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.encode): Fermion Hamiltonian을에서 사용할 수 있는 형식으로 인코딩합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="65ebd-126">[`%chemistry.encode`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.encode): Encodes a fermion Hamiltonian to a format consumable by Q#.</span></span>
- <span data-ttu-id="65ebd-127">[`%chemistry.fh.add_terms`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.add_terms): Fermion Hamiltonian에 용어를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-127">[`%chemistry.fh.add_terms`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.add_terms): Adds terms to a fermion Hamiltonian.</span></span>
- <span data-ttu-id="65ebd-128">[`%chemistry.fh.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.load): 전자 구조 문제에 대 한 fermion Hamiltonian을 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-128">[`%chemistry.fh.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.load): Loads the fermion Hamiltonian for an electronic structure problem.</span></span> <span data-ttu-id="65ebd-129">문제는 파일에서 로드되거나 인수로 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-129">The problem is loaded from a file or passed as an argument.</span></span>
- <span data-ttu-id="65ebd-130">[`%chemistry.inputstate.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.inputstate.load): Broombridge 전자적 구조 문제를 로드 하 고 선택한 입력 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-130">[`%chemistry.inputstate.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.inputstate.load): Loads Broombridge electronic structure problem and returns selected input state.</span></span>

### <a name="katas-from-microsoftquantumkatas-package"></a><span data-ttu-id="65ebd-131">Katas (Katas 패키지에서)</span><span class="sxs-lookup"><span data-stu-id="65ebd-131">Katas (from Microsoft.Quantum.Katas package)</span></span>

- <span data-ttu-id="65ebd-132">[`%kata`](xref:microsoft.quantum.iqsharp.magic-ref.kata): 단일 테스트를 실행 하 고 테스트 성공 여부를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-132">[`%kata`](xref:microsoft.quantum.iqsharp.magic-ref.kata): Runs a single test, and reports whether the test passed successfully.</span></span>
- <span data-ttu-id="65ebd-133">[`%check_kata`](xref:microsoft.quantum.iqsharp.magic-ref.check_kata): 단일 kata의 테스트에 대 한 참조 구현을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-133">[`%check_kata`](xref:microsoft.quantum.iqsharp.magic-ref.check_kata): Checks the reference implementation for a single kata's test.</span></span>
    <span data-ttu-id="65ebd-134">특히 단일 작업에 대 한 참조 구현을 셀로 대체 하 고 테스트 성공 여부를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ebd-134">Specifically, it substitutes the reference implementation for a single task into the cell, and reports whether the test passed successfully.</span></span>
