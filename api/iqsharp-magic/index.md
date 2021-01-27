---
title: IQ# 매직 명령
description: IQ# Jupyter 커널에서 사용할 수 있는 매직 명령을 나열합니다.
author: rmshaffer
uid: microsoft.quantum.iqsharp.magic-ref.index
ms.author: ryansha
ms.date: 01/24/2021
ms.topic: article
ms.openlocfilehash: 00b0e0b806c0034d222d286bac5388bd14326a60
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844094"
---
# <a name="iq-magic-commands"></a><span data-ttu-id="dca67-103">IQ# 매직 명령</span><span class="sxs-lookup"><span data-stu-id="dca67-103">IQ# Magic Commands</span></span>
| <span data-ttu-id="dca67-104">매직 명령</span><span class="sxs-lookup"><span data-stu-id="dca67-104">Magic Command</span></span> | <span data-ttu-id="dca67-105">요약</span><span class="sxs-lookup"><span data-stu-id="dca67-105">Summary</span></span> |
|---------------|---------|
| [`%azure.connect`](xref:microsoft.quantum.iqsharp.magic-ref.azure.connect) | <span data-ttu-id="dca67-106">Azure Quantum 작업 영역에 연결하거나 현재 연결 상태를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-106">Connects to an Azure Quantum workspace or displays current connection status.</span></span> |
| [`%azure.execute`](xref:microsoft.quantum.iqsharp.magic-ref.azure.execute) | <span data-ttu-id="dca67-107">Azure Quantum 작업 영역에 작업을 제출하고 완료될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-107">Submits a job to an Azure Quantum workspace and waits for completion.</span></span> |
| [`%azure.jobs`](xref:microsoft.quantum.iqsharp.magic-ref.azure.jobs) | <span data-ttu-id="dca67-108">현재 Azure Quantum 작업 영역의 작업 목록을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-108">Displays a list of jobs in the current Azure Quantum workspace.</span></span> |
| [`%azure.output`](xref:microsoft.quantum.iqsharp.magic-ref.azure.output) | <span data-ttu-id="dca67-109">현재 Azure Quantum 작업 영역의 작업 결과를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-109">Displays results for a job in the current Azure Quantum workspace.</span></span> |
| [`%azure.status`](xref:microsoft.quantum.iqsharp.magic-ref.azure.status) | <span data-ttu-id="dca67-110">현재 Azure Quantum 작업 영역의 작업 상태를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-110">Displays status for a job in the current Azure Quantum workspace.</span></span> |
| [`%azure.submit`](xref:microsoft.quantum.iqsharp.magic-ref.azure.submit) | <span data-ttu-id="dca67-111">Azure Quantum 작업 영역에 작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-111">Submits a job to an Azure Quantum workspace.</span></span> |
| [`%azure.target`](xref:microsoft.quantum.iqsharp.magic-ref.azure.target) | <span data-ttu-id="dca67-112">Azure Quantum 작업 영역의 Q# 작업 제출에 대한 활성 실행 대상을 설정하거나 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-112">Sets or displays the active execution target for Q# job submission in an Azure Quantum workspace.</span></span> |
| [`%check_kata`](xref:microsoft.quantum.iqsharp.magic-ref.check_kata) | <span data-ttu-id="dca67-113">단일 kata의 테스트에 대한 참조 구현을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-113">Checks the reference implementation for a single kata's test.</span></span> |
| [`%chemistry.broombridge`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.broombridge) | <span data-ttu-id="dca67-114">지정된 .yaml 파일에서 Broombridge 전자 구조 문제 표현을 로드하고 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-114">Loads and returns Broombridge electronic structure problem representation from a given .yaml file.</span></span> |
| [`%chemistry.encode`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.encode) | <span data-ttu-id="dca67-115">페르미온 해밀토니언을 Q#으로 사용할 수 있는 형식으로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-115">Encodes a fermion Hamiltonian to a format consumable by Q#.</span></span> |
| [`%chemistry.fh.add_terms`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.add_terms) | <span data-ttu-id="dca67-116">페르미온 해밀토니언에 항을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-116">Adds terms to a fermion Hamiltonian.</span></span> |
| [`%chemistry.fh.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.load) | <span data-ttu-id="dca67-117">전자 구조 문제에 대한 페르미온 해밀토니언을 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-117">Loads the fermion Hamiltonian for an electronic structure problem.</span></span> <span data-ttu-id="dca67-118">문제는 파일에서 로드되거나 인수로 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-118">The problem is loaded from a file or passed as an argument.</span></span> |
| [`%chemistry.inputstate.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.inputstate.load) | <span data-ttu-id="dca67-119">Broombridge 전자 구조 문제를 로드하고 선택한 입력 상태를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-119">Loads Broombridge electronic structure problem and returns selected input state.</span></span> |
| [`%config`](xref:microsoft.quantum.iqsharp.magic-ref.config) | <span data-ttu-id="dca67-120">구성 옵션을 설정하거나 쿼리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-120">Allows setting or querying configuration options.</span></span> |
| [`%debug`](xref:microsoft.quantum.iqsharp.magic-ref.debug) | <span data-ttu-id="dca67-121">지정된 Q# 작업 또는 함수를 단계별로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-121">Steps through the execution of a given Q# operation or function.</span></span> |
| [`%estimate`](xref:microsoft.quantum.iqsharp.magic-ref.estimate) | <span data-ttu-id="dca67-122">ResourcesEstimator 대상 머신에서 지정된 함수나 연산을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-122">Runs a given function or operation on the ResourcesEstimator target machine.</span></span> |
| [`%kata`](xref:microsoft.quantum.iqsharp.magic-ref.kata) | <span data-ttu-id="dca67-123">단일 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-123">Executes a single test.</span></span> |
| [`%lsmagic`](xref:microsoft.quantum.iqsharp.magic-ref.lsmagic) | <span data-ttu-id="dca67-124">현재 사용할 수 있는 모든 매직 명령 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-124">Returns a list of all currently available magic commands.</span></span> |
| [`%lsopen`](xref:microsoft.quantum.iqsharp.magic-ref.lsopen) | <span data-ttu-id="dca67-125">현재 열려 있는 네임스페이스 및 해당 별칭을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-125">Lists currently opened namespaces and their aliases.</span></span> |
| [`%package`](xref:microsoft.quantum.iqsharp.magic-ref.package) | <span data-ttu-id="dca67-126">NuGet 패키지를 로드하는 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-126">Provides the ability to load a NuGet package.</span></span> |
| [`%performance`](xref:microsoft.quantum.iqsharp.magic-ref.performance) | <span data-ttu-id="dca67-127">이 커널에 대한 현재 성능 메트릭을 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-127">Reports current performance metrics for this kernel.</span></span> |
| [`%project`](xref:microsoft.quantum.iqsharp.magic-ref.project) | <span data-ttu-id="dca67-128">Q# 프로젝트 참조를 보거나 추가하는 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-128">Provides the ability to view or add Q# project references.</span></span> |
| [`%simulate`](xref:microsoft.quantum.iqsharp.magic-ref.simulate) | <span data-ttu-id="dca67-129">QuantumSimulator 대상 컴퓨터에서 지정된 함수나 연산을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-129">Runs a given function or operation on the QuantumSimulator target machine.</span></span> |
| [`%toffoli`](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) | <span data-ttu-id="dca67-130">ToffoliSimulator 대상 컴퓨터에서 지정된 함수나 연산을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-130">Runs a given function or operation on the ToffoliSimulator target machine.</span></span> |
| [`%trace`](xref:microsoft.quantum.iqsharp.magic-ref.trace) | <span data-ttu-id="dca67-131">지정된 작업의 실행 경로를 시각화합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-131">Visualizes the execution path of the given operation.</span></span> |
| [`%who`](xref:microsoft.quantum.iqsharp.magic-ref.who) | <span data-ttu-id="dca67-132">현재 세션에서 사용할 수 있는 Q# 작업을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-132">Lists the Q# operations available in the current session.</span></span> |
| [`%workspace`](xref:microsoft.quantum.iqsharp.magic-ref.workspace) | <span data-ttu-id="dca67-133">현재 작업 영역과 관련된 작업을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="dca67-133">Provides actions related to the current workspace.</span></span> |
