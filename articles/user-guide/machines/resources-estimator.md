---
title: 퀀텀 리소스 평가기-퀀텀 개발 키트
description: '퀀텀 컴퓨터에서 지정 된 작업 인스턴스를 실행 하는 데 필요한 리소스를 추정 하는 Microsoft QDK resources 평가기에 대해 알아봅니다 Q# .'
author: anpaz-msft
ms.author: anpaz
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: e1ec01d85a141b9c8a7a5ba5589663a0773520e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691868"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a><span data-ttu-id="60322-103">QDK (퀀텀 Development Kit) 리소스 평가기</span><span class="sxs-lookup"><span data-stu-id="60322-103">Quantum Development Kit (QDK) resources estimator</span></span>

<span data-ttu-id="60322-104">이름에서 알 수 있듯이 `ResourcesEstimator` 클래스는 퀀텀 컴퓨터에서 지정 된 작업 인스턴스를 실행 하는 데 필요한 리소스를 추정 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="60322-104">As the name implies, the `ResourcesEstimator` class estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span> <span data-ttu-id="60322-105">퀀텀 컴퓨터의 상태를 실제로 시뮬레이션 하지 않고 퀀텀 작업을 실행 하 여이 작업을 수행 합니다. 따라서 Q# 코드의 클래식 부분이 적절 한 시간 내에 실행 되는 경우 수천 비트를 사용 하는 작업에 대 한 리소스를 추정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60322-105">It accomplishes this by running the quantum operation without actually simulating the state of a quantum computer; for this reason, it estimates resources for Q# operations that use thousands of qubits, provided that the classical part of the code runs in a reasonable time.</span></span>

<span data-ttu-id="60322-106">평가기 리소스는 프로그램을 디버그 하는 데 도움이 되는 다양 한 메트릭 및 도구 집합을 제공 하는 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)를 기반으로 빌드됩니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="60322-106">The resources estimator is built on top of the [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), which provides a richer set of metrics and tools to help debug Q# programs.</span></span>

## <a name="invoking-and-running-the-resources-estimator"></a><span data-ttu-id="60322-107">평가기 리소스 호출 및 실행</span><span class="sxs-lookup"><span data-stu-id="60322-107">Invoking and running the resources estimator</span></span>

<span data-ttu-id="60322-108">평가기 리소스를 사용 하 여 모든 작업을 실행할 수 있습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="60322-108">You can use the resources estimator to run any Q# operation.</span></span> <span data-ttu-id="60322-109">자세한 내용은 [ Q# 프로그램을 실행 하는 방법](xref:microsoft.quantum.guide.host-programs)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="60322-109">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-resources-estimator-from-c"></a><span data-ttu-id="60322-110">C에서 평가기 리소스 호출 #</span><span class="sxs-lookup"><span data-stu-id="60322-110">Invoking the resources estimator from C#</span></span> 

<span data-ttu-id="60322-111">다른 대상 컴퓨터와 마찬가지로 먼저 `ResourceEstimator` 클래스의 인스턴스를 만든 다음, 이를 작업의 `Run` 메서드의 첫 번째 매개 변수로 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="60322-111">As with other target machines, you first create an instance of the `ResourceEstimator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="60322-112">`QuantumSimulator` 클래스와 달리 `ResourceEstimator` 클래스는 <xref:System.IDisposable> 인터페이스를 구현하지 않으므로 `using` 문 내에 묶을 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="60322-112">Note that, unlike the `QuantumSimulator` class, the `ResourceEstimator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            ResourcesEstimator estimator = new ResourcesEstimator();
            MyQuantumProgram.Run(estimator).Wait();
            Console.WriteLine(estimator.ToTSV());
        }
    }
}
```

<span data-ttu-id="60322-113">예제에 나와 있는 것 처럼는 `ResourcesEstimator` `ToTSV()` 탭으로 구분 된 값 (TSV)이 있는 테이블을 생성 하는 메서드를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="60322-113">As the example shows, `ResourcesEstimator` provides the `ToTSV()` method, which generates a table with tab-separated values (TSV).</span></span> <span data-ttu-id="60322-114">테이블을 파일에 저장 하거나 분석을 위해 콘솔에 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60322-114">You can save the table to a file or display it to the console for analysis.</span></span> <span data-ttu-id="60322-115">다음은 이전 프로그램의 샘플 출력입니다.</span><span class="sxs-lookup"><span data-stu-id="60322-115">The following is a sample output from the preceding program:</span></span>

```output
Metric          Sum
CNOT            1000
QubitClifford   1000
R               0
Measure         4002
T               0
Depth           0
Width           2
BorrowedWidth   0
```

> [!NOTE]
> <span data-ttu-id="60322-116">`ResourcesEstimator`인스턴스는 실행 때마다 계산을 다시 설정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60322-116">A `ResourcesEstimator` instance does not reset its calculations on every run.</span></span> <span data-ttu-id="60322-117">동일한 인스턴스를 사용 하 여 다른 작업을 실행 하는 경우 새 결과를 기존 결과로 집계 합니다.</span><span class="sxs-lookup"><span data-stu-id="60322-117">If you use the same instance to run another operation, it aggregates the new results with the existing results.</span></span> <span data-ttu-id="60322-118">실행 간에 계산을 다시 설정 해야 하는 경우 모든 실행에 대해 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60322-118">If you need to reset calculations between runs, create a new instance for every run.</span></span>

### <a name="invoking-the-resources-estimator-from-python"></a><span data-ttu-id="60322-119">Python에서 평가기 리소스 호출</span><span class="sxs-lookup"><span data-stu-id="60322-119">Invoking the resources estimator from Python</span></span>

<span data-ttu-id="60322-120">가져온 작업과 함께 Python 라이브러리의 [estimate_resources ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) 메서드를 사용 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="60322-120">Use the [estimate_resources()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) method from the Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.estimate_resources()
```

### <a name="invoking-the-resources-estimator-from-the-command-line"></a><span data-ttu-id="60322-121">명령줄에서 리소스 평가기 호출</span><span class="sxs-lookup"><span data-stu-id="60322-121">Invoking the resources estimator from the command line</span></span>

<span data-ttu-id="60322-122">명령줄에서 프로그램을 실행 하는 경우 Q# **--시뮬레이터** (또는 **-s** 바로 가기) 매개 변수를 사용 하 여 `ResourcesEstimator` 대상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60322-122">When running a Q# program from the command line, use the **--simulator** (or **-s** shortcut) parameter to specify the `ResourcesEstimator` target machine.</span></span> <span data-ttu-id="60322-123">다음 명령은 평가기 리소스를 사용 하 여 프로그램을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="60322-123">The following command runs a program using the resources estimator:</span></span> 

```dotnetcli
dotnet run -s ResourcesEstimator
```

### <a name="invoking-the-resources-estimator-from-juptyer-notebooks"></a><span data-ttu-id="60322-124">Juptyer 노트북에서 평가기 리소스 호출</span><span class="sxs-lookup"><span data-stu-id="60322-124">Invoking the resources estimator from Juptyer Notebooks</span></span>

<span data-ttu-id="60322-125">Q#작업을 실행 하려면 a 매직 명령 [% 예상 값](xref:microsoft.quantum.iqsharp.magic-ref.simulate) 을 사용 Q# 합니다.</span><span class="sxs-lookup"><span data-stu-id="60322-125">Use the IQ# magic command [%estimate](xref:microsoft.quantum.iqsharp.magic-ref.simulate) to run the Q# operation.</span></span>

```
%estimate myOperation
```

## <a name="programmatically-retrieving-the-estimated-data"></a><span data-ttu-id="60322-126">프로그래밍 방식으로 예상 데이터 검색</span><span class="sxs-lookup"><span data-stu-id="60322-126">Programmatically retrieving the estimated data</span></span>

<span data-ttu-id="60322-127">TSV 테이블 외에도 `Data` 평가기 리소스의 속성을 통해 실행 중에 예상 되는 리소스를 프로그래밍 방식으로 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60322-127">In addition to a TSV table, you can programmatically retrieve the resources estimated during the run via the `Data` property of the resources estimator.</span></span> <span data-ttu-id="60322-128">`Data`속성은 `System.DataTable` 두 개의 열 ( `Metric` 및 `Sum` )이 메트릭의 이름으로 인덱싱되는 인스턴스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="60322-128">The `Data` property provides a `System.DataTable` instance with two columns: `Metric` and `Sum`, indexed by the metrics' names.</span></span>

<span data-ttu-id="60322-129">다음 코드에서는 `QubitClifford` `T` `CNOT` 작업에서 사용 되는 및 작업의 총 수를 검색 하 고 인쇄 하는 방법을 보여 줍니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="60322-129">The following code shows how to retrieve and print the total number of `QubitClifford`, `T` and `CNOT` operations used by a Q# operation:</span></span>

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            ResourcesEstimator estimator = new ResourcesEstimator();
            MyQuantumProgram.Run(estimator).Wait();

            var data = estimator.Data;
            Console.WriteLine($"QubitCliffords: {data.Rows.Find("QubitClifford")["Sum"]}");
            Console.WriteLine($"Ts: {data.Rows.Find("T")["Sum"]}");
            Console.WriteLine($"CNOTs: {data.Rows.Find("CNOT")["Sum"]}");
        }
    }
}
```

## <a name="metrics-reported"></a><span data-ttu-id="60322-130">보고 된 메트릭</span><span class="sxs-lookup"><span data-stu-id="60322-130">Metrics Reported</span></span>

<span data-ttu-id="60322-131">평가기 리소스는 다음 메트릭을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="60322-131">The resources estimator tracks the following metrics:</span></span>

|<span data-ttu-id="60322-132">메트릭</span><span class="sxs-lookup"><span data-stu-id="60322-132">Metric</span></span>|<span data-ttu-id="60322-133">Description</span><span class="sxs-lookup"><span data-stu-id="60322-133">Description</span></span>|
|----|----|
|<span data-ttu-id="60322-134">__CNOT__</span><span class="sxs-lookup"><span data-stu-id="60322-134">__CNOT__</span></span>    |<span data-ttu-id="60322-135">작업의 실행 수 `CNOT` (제어 된 Pauli X 작업이 라고도 함).</span><span class="sxs-lookup"><span data-stu-id="60322-135">The run count of `CNOT` operations (also known as Controlled Pauli X operations).</span></span>|
|<span data-ttu-id="60322-136">__QubitClifford__</span><span class="sxs-lookup"><span data-stu-id="60322-136">__QubitClifford__</span></span> |<span data-ttu-id="60322-137">단일 Clifford 및 Pauli 작업의 실행 수입니다.</span><span class="sxs-lookup"><span data-stu-id="60322-137">The run count of any single qubit Clifford and Pauli operations.</span></span>|
|<span data-ttu-id="60322-138">__측정값__</span><span class="sxs-lookup"><span data-stu-id="60322-138">__Measure__</span></span>    |<span data-ttu-id="60322-139">측정의 실행 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="60322-139">The run count of any measurements.</span></span>  |
|<span data-ttu-id="60322-140">__R__</span><span class="sxs-lookup"><span data-stu-id="60322-140">__R__</span></span>    |<span data-ttu-id="60322-141">Clifford 및 Pauli 작업을 제외한 모든 단일 비트 회전의 실행 횟수입니다 `T` .</span><span class="sxs-lookup"><span data-stu-id="60322-141">The run count of any single-qubit rotations, excluding `T`, Clifford and Pauli operations.</span></span>  |
|<span data-ttu-id="60322-142">__T__</span><span class="sxs-lookup"><span data-stu-id="60322-142">__T__</span></span>    |<span data-ttu-id="60322-143">작업의 실행 수 `T` 및 `T` 작업, T_x = .h 및 T_y = Hy. Hy를 포함 하는 변화 시키고입니다.</span><span class="sxs-lookup"><span data-stu-id="60322-143">The run count of `T` operations and their conjugates, including the `T` operations, T_x = H.T.H, and T_y = Hy.T.Hy.</span></span>  |
|<span data-ttu-id="60322-144">__깊이__</span><span class="sxs-lookup"><span data-stu-id="60322-144">__Depth__</span></span>|<span data-ttu-id="60322-145">작업에 의해 실행 되는 퀀텀 회로의 깊이 Q# 입니다 ( [아래](#depth-width-and-qubitcount)참조).</span><span class="sxs-lookup"><span data-stu-id="60322-145">Depth of the quantum circuit run by the Q# operation (see [below](#depth-width-and-qubitcount)).</span></span> <span data-ttu-id="60322-146">기본적으로 깊이 메트릭은 게이트 수만 계산 `T` 합니다.</span><span class="sxs-lookup"><span data-stu-id="60322-146">By default, the depth metric only counts `T` gates.</span></span> <span data-ttu-id="60322-147">자세한 내용은 [깊이 카운터](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="60322-147">For more details, see [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span></span>   |
|<span data-ttu-id="60322-148">__Width__</span><span class="sxs-lookup"><span data-stu-id="60322-148">__Width__</span></span>|<span data-ttu-id="60322-149">작업에 의해 실행 되는 퀀텀 회로의 너비 Q# 입니다 ( [아래](#depth-width-and-qubitcount)참조).</span><span class="sxs-lookup"><span data-stu-id="60322-149">Width of the quantum circuit run by the Q# operation (see [below](#depth-width-and-qubitcount)).</span></span> <span data-ttu-id="60322-150">기본적으로 깊이 메트릭은 게이트 수만 계산 `T` 합니다.</span><span class="sxs-lookup"><span data-stu-id="60322-150">By default, the depth metric only counts `T` gates.</span></span> <span data-ttu-id="60322-151">자세한 내용은 [깊이 카운터](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="60322-151">For more details, see [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span></span>   |
|<span data-ttu-id="60322-152">__고 비트 수__</span><span class="sxs-lookup"><span data-stu-id="60322-152">__QubitCount__</span></span>    |<span data-ttu-id="60322-153">작업을 실행 하는 동안 할당 된 최대 값 수의 하한값입니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="60322-153">The lower bound for the maximum number of qubits allocated during the run of the Q# operation.</span></span> <span data-ttu-id="60322-154">이 메트릭은 __깊이__ 와 호환 되지 않을 수 있습니다 (아래 참조).</span><span class="sxs-lookup"><span data-stu-id="60322-154">This metric might not be compatible with __Depth__ (see below).</span></span>  |
|<span data-ttu-id="60322-155">__BorrowedWidth__</span><span class="sxs-lookup"><span data-stu-id="60322-155">__BorrowedWidth__</span></span>    |<span data-ttu-id="60322-156">작업 내에서 빌려 온 최대 수입니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="60322-156">The maximum number of qubits borrowed inside the Q# operation.</span></span>  |


## <a name="depth-width-and-qubitcount"></a><span data-ttu-id="60322-157">Depth, Width 및  Bitcount</span><span class="sxs-lookup"><span data-stu-id="60322-157">Depth, Width, and QubitCount</span></span>

<span data-ttu-id="60322-158">보고 된 깊이 및 너비 예상치는 서로 호환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60322-158">Reported Depth and Width estimates are compatible with each other.</span></span>
<span data-ttu-id="60322-159">(이전에는 두 숫자를 모두 달성할 수 있었지만 깊이와 너비를 위해 서로 다른 회로가 필요 합니다.) 현재이 쌍의 두 메트릭은 동시에 동일한 회로를 통해 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60322-159">(Previously both numbers were achievable, but different circuits would be required for Depth and for Width.) Currently both metrics in this pair can be achieved by the same circuit at the same time.</span></span>

<span data-ttu-id="60322-160">보고 되는 메트릭은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="60322-160">The following metrics are reported:</span></span>

<span data-ttu-id="60322-161">__깊이:__ 루트 작업의 경우 특정 게이트 시간을 가정 하 여 실행 하는 데 걸리는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="60322-161">__Depth:__ For the root operation - time it takes to execute it assuming specific gate times.</span></span>
<span data-ttu-id="60322-162">작업의 시작과 끝에서 최신 비트율 비트 가용성 시간 사이의 후속 작업 시간 차이를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="60322-162">For operations called or subsequent operations - time difference between latest qubit availability time at the beginning and the end of the operation.</span></span>

<span data-ttu-id="60322-163">__너비:__ 루트 작업의 경우-이를 실행 하는 데 실제로 사용 되는 작업 (및 호출 하는 작업)의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="60322-163">__Width:__ For the root operation - number of qubits actually used to execute it (and operation it calls).</span></span>
<span data-ttu-id="60322-164">작업을 시작할 때 이미 사용 된 것과 같은 작업의 경우 또는 후속 작업에 사용 된 것 보다 더 많은 이상 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="60322-164">For operations called or subsequent operations - how many more qubits were used in addition to the qubits already used at the beginning of the operation.</span></span>

<span data-ttu-id="60322-165">재사용 된 값은이 숫자에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60322-165">Please note, that reused qubits do not contribute to this number.</span></span>
<span data-ttu-id="60322-166">즉, 작업 A가 시작 되기 전에 몇 개의 몇 가지 기능을 해제 하 고이 작업에서 요구 하는 모든 기능 (및에서 호출 된 작업)이 이전 릴리스를 다시 사용 하 여 충족 된 경우 작업 A의 너비가 0으로 보고 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60322-166">I.e. if a few qubits have been released before operation A starts, and all qubit demanded by this operation A (and operations called from A) were satisfied by reusing previously release qubits, the Width of operation A is reported as 0.</span></span> <span data-ttu-id="60322-167">이 경우에는 너비에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60322-167">Successfully borrowed qubits do not contribute to the Width either.</span></span>

<span data-ttu-id="60322-168">고 __비트 수:__ 루트 작업의 경우-이 작업을 실행 하는 데 충분 하 고 해당 작업에서 호출 되는 작업을 실행 하기에 충분 한 최소 수의 단일 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="60322-168">__QubitCount:__ For the root operation - minimum number of qubits that would be sufficient to execute this operation (and operations called from it).</span></span>
<span data-ttu-id="60322-169">또는 후속 작업에 대해이 작업을 별도로 실행 하기에 충분 한 최소 수의 단일 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="60322-169">For operations called or subsequent operations - minimum number of qubits that would be sufficient to execute this operation separately.</span></span> <span data-ttu-id="60322-170">이 숫자에는 입력 비트 비트가 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60322-170">This number doesn't include input qubits.</span></span> <span data-ttu-id="60322-171">여기에는가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60322-171">It does include borrowed qubits.</span></span>

<span data-ttu-id="60322-172">두 가지 작업 모드가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60322-172">Two modes of operation are supported.</span></span> <span data-ttu-id="60322-173">QCTraceSimulatorConfiguration. OptimizeDepth를 설정 하 여 모드를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="60322-173">Mode is selected by setting QCTraceSimulatorConfiguration.OptimizeDepth.</span></span>

<span data-ttu-id="60322-174">__OptimizeDepth = true:__ 이 경우는 더 이상 사용 하지 않는 것이 좋으며 비트를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="60322-174">__OptimizeDepth=true:__ QubitManager is discouraged from qubit reuse and allocates new qubit every time it is asked for a qubit.</span></span> <span data-ttu-id="60322-175">루트 작업 __깊이__ 는 최소 깊이 (하한값)가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60322-175">For the root operation __Depth__ becomes the minimum depth (lower bound).</span></span> <span data-ttu-id="60322-176">이 깊이에 대해 호환 되는 __너비가__ 보고 됩니다. 둘 다 동시에 달성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60322-176">Compatible __Width__ is reported for this depth (both can be achieved at the same time).</span></span> <span data-ttu-id="60322-177">이 너비는이 깊이에서 최적이 아닐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60322-177">Note, that this width will likely be not optimal given this depth.</span></span> <span data-ttu-id="60322-178">작업을 다시 사용 하는 것으로 가정 하기 때문에 루트 작업의 경우에는 너비 보다 낮을 __수 있습니다.__</span><span class="sxs-lookup"><span data-stu-id="60322-178">__QubitCount__ may be lower than Width for the root operation because it assumes reuse.</span></span>

<span data-ttu-id="60322-179">__OptimizeDepth = false:__ 새 항목을 할당 하기 전에 원하는 비트를 다시 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="60322-179">__OptimizeDepth=false:__ QubitManager is encouraged to reuse qubits and will reuse released qubits before allocating new ones.</span></span> <span data-ttu-id="60322-180">루트 __작업의 경우 너비가 최소__ 너비 (하한값)가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60322-180">For the root operation __Width__ becomes the minimal width (lower bound).</span></span> <span data-ttu-id="60322-181">호환 가능한 __깊이가__ 보고 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60322-181">Compatible __Depth__ is reported on which it can be achieved.</span></span> <span data-ttu-id="60322-182">Borrowing가 없는 것으로 가정 하는 루트 작업의 __너비__ 와 동일한 __것이 있습니다__ .</span><span class="sxs-lookup"><span data-stu-id="60322-182">__QubitCount__ will be the same as __Width__ for the root operation assuming no borrowing.</span></span>

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="60322-183">측정 결과의 확률 제공</span><span class="sxs-lookup"><span data-stu-id="60322-183">Providing the probability of measurement outcomes</span></span>

<span data-ttu-id="60322-184"><xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> <xref:Microsoft.Quantum.Diagnostics> 네임 스페이스에서를 사용 하 여 측정 작업의 예상 확률에 대 한 정보를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60322-184">You can use <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> from the <xref:Microsoft.Quantum.Diagnostics> namespace to provide information about the expected probability of a measurement operation.</span></span> <span data-ttu-id="60322-185">자세한 내용은 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="60322-185">For more information, see [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)</span></span>

## <a name="see-also"></a><span data-ttu-id="60322-186">참고 항목</span><span class="sxs-lookup"><span data-stu-id="60322-186">See also</span></span>

- [<span data-ttu-id="60322-187">퀀텀 추적 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="60322-187">Quantum trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [<span data-ttu-id="60322-188">퀀텀 Toffoli 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="60322-188">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="60322-189">퀀텀 전체 상태 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="60322-189">Quantum full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 
