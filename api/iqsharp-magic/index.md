---
title: IQ# 매직 명령
author: rmshaffer
uid: microsoft.quantum.iqsharp.magic-ref.index
ms.author: rmshaffer
ms.date: 09/29/2020
ms.topic: article
ms.openlocfilehash: 934ab18b667797d09d2c8188f727e64b0017e1d5
ms.sourcegitcommit: 685a8ab16d7e6a25e63a168d6e7c385fa6e876cc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/29/2020
ms.locfileid: "91464677"
---
# <a name="iq-magic-commands"></a><span data-ttu-id="717ab-102">IQ# 매직 명령</span><span class="sxs-lookup"><span data-stu-id="717ab-102">IQ# Magic Commands</span></span>
| <span data-ttu-id="717ab-103">매직 명령</span><span class="sxs-lookup"><span data-stu-id="717ab-103">Magic Command</span></span> | <span data-ttu-id="717ab-104">요약</span><span class="sxs-lookup"><span data-stu-id="717ab-104">Summary</span></span> |
|---------------|---------|
| [`%azure.connect`](xref:microsoft.quantum.iqsharp.magic-ref.azure.connect) | <span data-ttu-id="717ab-105">Azure Quantum 작업 영역에 연결하거나 현재 연결 상태를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-105">Connects to an Azure Quantum workspace or displays current connection status.</span></span> |
| [`%azure.execute`](xref:microsoft.quantum.iqsharp.magic-ref.azure.execute) | <span data-ttu-id="717ab-106">Azure Quantum 작업 영역에서 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-106">Executes a job in an Azure Quantum workspace.</span></span> |
| [`%azure.jobs`](xref:microsoft.quantum.iqsharp.magic-ref.azure.jobs) | <span data-ttu-id="717ab-107">현재 Azure Quantum 작업 영역의 작업 목록을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-107">Displays a list of jobs in the current Azure Quantum workspace.</span></span> |
| [`%azure.output`](xref:microsoft.quantum.iqsharp.magic-ref.azure.output) | <span data-ttu-id="717ab-108">현재 Azure Quantum 작업 영역의 작업 결과를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-108">Displays results for a job in the current Azure Quantum workspace.</span></span> |
| [`%azure.status`](xref:microsoft.quantum.iqsharp.magic-ref.azure.status) | <span data-ttu-id="717ab-109">현재 Azure Quantum 작업 영역의 작업 상태를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-109">Displays status for a job in the current Azure Quantum workspace.</span></span> |
| [`%azure.submit`](xref:microsoft.quantum.iqsharp.magic-ref.azure.submit) | <span data-ttu-id="717ab-110">Azure Quantum 작업 영역에 작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-110">Submits a job to an Azure Quantum workspace.</span></span> |
| [`%azure.target`](xref:microsoft.quantum.iqsharp.magic-ref.azure.target) | <span data-ttu-id="717ab-111">Azure Quantum 작업 영역의 Q# 작업 제출에 대한 활성 실행 대상을 설정하거나 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-111">Sets or displays the active execution target for Q# job submission in an Azure Quantum workspace.</span></span> |
| [`%check_kata`](xref:microsoft.quantum.iqsharp.magic-ref.check_kata) | <span data-ttu-id="717ab-112">단일 kata의 테스트에 대한 참조 구현을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-112">Checks the reference implementation for a single kata's test.</span></span> |
| [`%chemistry.broombridge`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.broombridge) | <span data-ttu-id="717ab-113">지정된 .yaml 파일에서 Broombridge 전자 구조 문제 표현을 로드하고 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-113">Loads and returns Broombridge electronic structure problem representation from a given .yaml file.</span></span> |
| [`%chemistry.encode`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.encode) | <span data-ttu-id="717ab-114">페르미온 해밀토니언을 Q#으로 사용할 수 있는 형식으로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-114">Encodes a fermion Hamiltonian to a format consumable by Q#.</span></span> |
| [`%chemistry.fh.add_terms`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.add_terms) | <span data-ttu-id="717ab-115">페르미온 해밀토니언에 항을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-115">Adds terms to a fermion Hamiltonian.</span></span> |
| [`%chemistry.fh.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.load) | <span data-ttu-id="717ab-116">전자 구조 문제에 대한 페르미온 해밀토니언을 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-116">Loads the fermion Hamiltonian for an electronic structure problem.</span></span> <span data-ttu-id="717ab-117">문제는 파일에서 로드되거나 인수로 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-117">The problem is loaded from a file or passed as an argument.</span></span> |
| [`%chemistry.inputstate.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.inputstate.load) | <span data-ttu-id="717ab-118">Broombridge 전자 구조 문제를 로드하고 선택한 입력 상태를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-118">Loads Broombridge electronic structure problem and returns selected input state.</span></span> |
| [`%config`](xref:microsoft.quantum.iqsharp.magic-ref.config) | <span data-ttu-id="717ab-119">구성 옵션을 설정하거나 쿼리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-119">Allows setting or querying configuration options.</span></span> |
| [`%estimate`](xref:microsoft.quantum.iqsharp.magic-ref.estimate) | <span data-ttu-id="717ab-120">ResourcesEstimator 대상 머신에서 지정된 함수나 연산을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-120">Runs a given function or operation on the ResourcesEstimator target machine.</span></span> |
| [`%kata`](xref:microsoft.quantum.iqsharp.magic-ref.kata) | <span data-ttu-id="717ab-121">단일 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-121">Executes a single test.</span></span> |
| [`%lsmagic`](xref:microsoft.quantum.iqsharp.magic-ref.lsmagic) | <span data-ttu-id="717ab-122">현재 사용할 수 있는 모든 매직 명령 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-122">Returns a list of all currently available magic commands.</span></span> |
| [`%lsopen`](xref:microsoft.quantum.iqsharp.magic-ref.lsopen) | <span data-ttu-id="717ab-123">현재 열려 있는 네임스페이스 및 해당 별칭을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-123">Lists currently opened namespaces and their aliases.</span></span> |
| [`%package`](xref:microsoft.quantum.iqsharp.magic-ref.package) | <span data-ttu-id="717ab-124">NuGet 패키지를 로드하는 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-124">Provides the ability to load a NuGet package.</span></span> |
| [`%performance`](xref:microsoft.quantum.iqsharp.magic-ref.performance) | <span data-ttu-id="717ab-125">이 커널에 대한 현재 성능 메트릭을 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-125">Reports current performance metrics for this kernel.</span></span> |
| [`%project`](xref:microsoft.quantum.iqsharp.magic-ref.project) | <span data-ttu-id="717ab-126">Q# 프로젝트 참조를 보거나 추가하는 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-126">Provides the ability to view or add Q# project references.</span></span> |
| [`%simulate`](xref:microsoft.quantum.iqsharp.magic-ref.simulate) | <span data-ttu-id="717ab-127">QuantumSimulator 대상 컴퓨터에서 지정된 함수나 연산을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-127">Runs a given function or operation on the QuantumSimulator target machine.</span></span> |
| [`%toffoli`](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) | <span data-ttu-id="717ab-128">ToffoliSimulator 대상 컴퓨터에서 지정된 함수나 연산을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-128">Runs a given function or operation on the ToffoliSimulator target machine.</span></span> |
| [`%trace`](xref:microsoft.quantum.iqsharp.magic-ref.trace) | <span data-ttu-id="717ab-129">지정된 작업의 실행 경로를 시각화합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-129">Visualizes the execution path of the given operation.</span></span> |
| [`%who`](xref:microsoft.quantum.iqsharp.magic-ref.who) | <span data-ttu-id="717ab-130">현재 세션에서 사용할 수 있는 Q# 작업을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-130">Lists the Q# operations available in the current session.</span></span> |
| [`%workspace`](xref:microsoft.quantum.iqsharp.magic-ref.workspace) | <span data-ttu-id="717ab-131">현재 작업 영역과 관련된 작업을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="717ab-131">Provides actions related to the current workspace.</span></span> |
