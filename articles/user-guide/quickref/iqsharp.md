---
title: IQ# 매직 명령
description: 'R c 2를 사용 하 여 IQ # 매직 명령에 대 한 빠른 참조 페이지 Q # Jupyter 노트북'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
uid: microsoft.quantum.guide.quickref.iqsharp
ms.openlocfilehash: 0cd1a2289132e2760a21fd9d4f4083696353e271
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431022"
---
# <a name="iq-magic-commands"></a><span data-ttu-id="ba320-103">IQ# 매직 명령</span><span class="sxs-lookup"><span data-stu-id="ba320-103">IQ# Magic Commands</span></span>

### <a name="general"></a><span data-ttu-id="ba320-104">일반</span><span class="sxs-lookup"><span data-stu-id="ba320-104">General</span></span>

- <span data-ttu-id="ba320-105">`%config`: 구성 기본 설정을 설정 하거나 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-105">`%config`: Sets or gets configuration preferences.</span></span>
- <span data-ttu-id="ba320-106">`%estimate`: QuantumSimulator 대상 컴퓨터에서 지정 된 함수 또는 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-106">`%estimate`: Runs a given function or operation on the QuantumSimulator target machine.</span></span>
- <span data-ttu-id="ba320-107">`%lsmagic`: 현재 사용할 수 있는 모든 매직 명령의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-107">`%lsmagic`: Returns a list of all currently available magic commands.</span></span>
- <span data-ttu-id="ba320-108">`%package`: Nuget 패키지를 로드 하는 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-108">`%package`: Provides the ability to load a Nuget package.</span></span>
- <span data-ttu-id="ba320-109">`%performance`:이 커널에 대 한 현재 성능 메트릭을 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-109">`%performance`: Reports current performance metrics for this kernel.</span></span>
- <span data-ttu-id="ba320-110">`%simulate`: QuantumSimulator 대상 컴퓨터에서 지정 된 함수 또는 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-110">`%simulate`: Runs a given function or operation on the QuantumSimulator target machine.</span></span>
- <span data-ttu-id="ba320-111">`%toffoli`: ToffoliSimulator 시뮬레이터 대상 컴퓨터에서 지정 된 함수 또는 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-111">`%toffoli`: Runs a given function or operation on the ToffoliSimulator simulator target machine.</span></span>
- <span data-ttu-id="ba320-112">`%who`: 현재 작업 영역과 관련 된 작업을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-112">`%who`: Provides actions related to the current workspace.</span></span>
- <span data-ttu-id="ba320-113">`%workspace`: 현재 세션에 정의 된 모든 작업 및 함수 목록을 대화형으로 반환 하거나 현재 작업 영역에서 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-113">`%workspace`: Returns a list of all operations and functions defined in the current session, either interactively or loaded from the current workspace.</span></span>

### <a name="chemistry"></a><span data-ttu-id="ba320-114">화학</span><span class="sxs-lookup"><span data-stu-id="ba320-114">Chemistry</span></span>

- <span data-ttu-id="ba320-115">`%chemistry.broombridge`: 지정 된 .yaml 파일에서 Broombridge 전자적 구조 문제 표현을 로드 하 고 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-115">`%chemistry.broombridge`: Loads and returns Broombridge electronic structure problem representation from a given .yaml file.</span></span>
- <span data-ttu-id="ba320-116">`%chemistry.encode`: Fermion Hamiltonian를 Q #에서 사용할 수 있는 형식으로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-116">`%chemistry.encode`: Encodes a fermion Hamiltonian to a format consumable by Q#.</span></span>
- <span data-ttu-id="ba320-117">`%chemistry.fh.add_terms`: Fermion Hamiltonian에 용어를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-117">`%chemistry.fh.add_terms`: Adds terms to a fermion Hamiltonian.</span></span>
- <span data-ttu-id="ba320-118">`%chemistry.fh.load`: 전자 구조 문제에 대 한 fermion Hamiltonian을 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-118">`%chemistry.fh.load`: Loads the fermion Hamiltonian for an electronic structure problem.</span></span> <span data-ttu-id="ba320-119">문제는 파일에서 로드되거나 인수로 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-119">The problem is loaded from a file or passed as an argument.</span></span>
- <span data-ttu-id="ba320-120">`%chemistry.inputstate.load`: Broombridge 전자적 구조 문제를 로드 하 고 선택한 입력 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-120">`%chemistry.inputstate.load`: Loads Broombridge electronic structure problem and returns selected input state.</span></span>

### <a name="from-microsoftquantumkatas-package"></a><span data-ttu-id="ba320-121">Katas 패키지에서</span><span class="sxs-lookup"><span data-stu-id="ba320-121">From Microsoft.Quantum.Katas package</span></span>

- <span data-ttu-id="ba320-122">`%kata`: 단일 테스트를 실행 하 고 테스트 성공 여부를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-122">`%kata`: Executes a single test, and reports whether the test passed successfully.</span></span>
- <span data-ttu-id="ba320-123">`%check_kata`: 단일 kata의 테스트에 대 한 참조 구현을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-123">`%check_kata`: Checks the reference implementation for a single kata's test.</span></span>
    <span data-ttu-id="ba320-124">특히 단일 작업에 대 한 참조 구현을 셀로 대체 하 고 테스트 성공 여부를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba320-124">Specifically, it substitutes the reference implementation for a single task into the cell, and reports whether the test passed successfully.</span></span>
