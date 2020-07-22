---
title: 퀀텀 리소스 평가기-퀀텀 개발 키트
description: '퀀텀 컴퓨터에서 지정 된 Q # 작업 인스턴스를 실행 하는 데 필요한 리소스를 추정 하는 Microsoft QDK resources 평가기에 대해 알아봅니다.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: 0909a050e89d6295664e54ab63cfda5d407a8f12
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/21/2020
ms.locfileid: "86870546"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a><span data-ttu-id="968a2-103">QDK (퀀텀 Development Kit) 리소스 평가기</span><span class="sxs-lookup"><span data-stu-id="968a2-103">Quantum Development Kit (QDK) resources estimator</span></span>

<span data-ttu-id="968a2-104">이름에서 알 수 있듯이 `ResourcesEstimator` 클래스는 퀀텀 컴퓨터에서 지정 된 Q # 작업 인스턴스를 실행 하는 데 필요한 리소스를 추정 합니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-104">As the name implies, the `ResourcesEstimator` class estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span> <span data-ttu-id="968a2-105">퀀텀 컴퓨터의 상태를 실제로 시뮬레이션 하지 않고 퀀텀 작업을 실행 하 여이 작업을 수행 합니다. 따라서 코드의 클래식 부분이 적절 한 시간 내에 실행 되는 경우 수천 비트를 사용 하는 Q # 작업에 대 한 리소스를 예측 합니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-105">It accomplishes this by executing the quantum operation without actually simulating the state of a quantum computer; for this reason, it estimates resources for Q# operations that use thousands of qubits, provided that the classical part of the code runs in a reasonable time.</span></span>

<span data-ttu-id="968a2-106">평가기 리소스는 Q # 프로그램을 디버그 하는 데 도움이 되는 다양 한 메트릭 및 도구 집합을 제공 하는 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)를 기반으로 빌드됩니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-106">The resources estimator is built on top of the [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), which provides a richer set of metrics and tools to help debug Q# programs.</span></span>

## <a name="invoking-and-running-the-resources-estimator"></a><span data-ttu-id="968a2-107">평가기 리소스 호출 및 실행</span><span class="sxs-lookup"><span data-stu-id="968a2-107">Invoking and running the resources estimator</span></span>

<span data-ttu-id="968a2-108">평가기 리소스를 사용 하 여 Q # 작업을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-108">You can use the resources estimator to run any Q# operation.</span></span> <span data-ttu-id="968a2-109">자세한 내용은 [Q # 프로그램을 실행 하는 방법](xref:microsoft.quantum.guide.host-programs)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="968a2-109">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-resources-estimator-from-c"></a><span data-ttu-id="968a2-110">C에서 평가기 리소스 호출 #</span><span class="sxs-lookup"><span data-stu-id="968a2-110">Invoking the resources estimator from C#</span></span> 

<span data-ttu-id="968a2-111">다른 대상 컴퓨터와 마찬가지로 먼저 클래스의 인스턴스를 만든 `ResourceEstimator` 다음 작업 메서드의 첫 번째 매개 변수로 전달 `Run` 합니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-111">As with other target machines, you first create an instance of the `ResourceEstimator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="968a2-112">클래스와 달리 `QuantumSimulator` `ResourceEstimator` 클래스는 인터페이스를 구현 하지 않으므로 <xref:System.IDisposable> 문 내에 묶을 필요가 없습니다 `using` .</span><span class="sxs-lookup"><span data-stu-id="968a2-112">Note that, unlike the `QuantumSimulator` class, the `ResourceEstimator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

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

<span data-ttu-id="968a2-113">예제에 나와 있는 것 처럼는 `ResourcesEstimator` `ToTSV()` 탭으로 구분 된 값 (TSV)이 있는 테이블을 생성 하는 메서드를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-113">As the example shows, `ResourcesEstimator` provides the `ToTSV()` method, which generates a table with tab-separated values (TSV).</span></span> <span data-ttu-id="968a2-114">테이블을 파일에 저장 하거나 분석을 위해 콘솔에 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-114">You can save the table to a file or display it to the console for analysis.</span></span> <span data-ttu-id="968a2-115">다음은 이전 프로그램의 샘플 출력입니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-115">The following is a sample output from the preceding program:</span></span>

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
> <span data-ttu-id="968a2-116">`ResourcesEstimator`인스턴스는 실행 때마다 계산을 다시 설정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-116">A `ResourcesEstimator` instance does not reset its calculations on every run.</span></span> <span data-ttu-id="968a2-117">동일한 인스턴스를 사용 하 여 다른 작업을 실행 하는 경우 새 결과를 기존 결과로 집계 합니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-117">If you use the same instance to run another operation, it aggregates the new results with the existing results.</span></span> <span data-ttu-id="968a2-118">실행 간에 계산을 다시 설정 해야 하는 경우 모든 실행에 대해 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-118">If you need to reset calculations between runs, create a new instance for every run.</span></span>

### <a name="invoking-the-resources-estimator-from-python"></a><span data-ttu-id="968a2-119">Python에서 평가기 리소스 호출</span><span class="sxs-lookup"><span data-stu-id="968a2-119">Invoking the resources estimator from Python</span></span>

<span data-ttu-id="968a2-120">가져온 Q # 작업을 사용 하 여 Python 라이브러리의 [estimate_resources ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) 메서드를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-120">Use the [estimate_resources()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) method from the Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.estimate_resources()
```

### <a name="invoking-the-resources-estimator-from-the-command-line"></a><span data-ttu-id="968a2-121">명령줄에서 리소스 평가기 호출</span><span class="sxs-lookup"><span data-stu-id="968a2-121">Invoking the resources estimator from the command line</span></span>

<span data-ttu-id="968a2-122">명령줄에서 Q # 프로그램을 실행 하는 경우 **--시뮬레이터** (또는 **-s** 바로 가기) 매개 변수를 사용 하 여 `ResourcesEstimator` 대상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-122">When running a Q# program from the command line, use the **--simulator** (or **-s** shortcut) parameter to specify the `ResourcesEstimator` target machine.</span></span> <span data-ttu-id="968a2-123">다음 명령은 평가기 리소스를 사용 하 여 프로그램을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-123">The following command runs a program using the resources estimator:</span></span> 

```dotnetcli
dotnet run -s ResourcesEstimator
```

### <a name="invoking-the-resources-estimator-from-juptyer-notebooks"></a><span data-ttu-id="968a2-124">Juptyer 노트북에서 평가기 리소스 호출</span><span class="sxs-lookup"><span data-stu-id="968a2-124">Invoking the resources estimator from Juptyer Notebooks</span></span>

<span data-ttu-id="968a2-125">Q # 작업을 실행 하려면 IQ # 매직 명령 [% 예상 값](xref:microsoft.quantum.iqsharp.magic-ref.simulate) 을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-125">Use the IQ# magic command [%estimate](xref:microsoft.quantum.iqsharp.magic-ref.simulate) to run the Q# operation.</span></span>

```
%estimate myOperation
```

## <a name="programmatically-retrieving-the-estimated-data"></a><span data-ttu-id="968a2-126">프로그래밍 방식으로 예상 데이터 검색</span><span class="sxs-lookup"><span data-stu-id="968a2-126">Programmatically retrieving the estimated data</span></span>

<span data-ttu-id="968a2-127">TSV 테이블 외에도 `Data` 평가기 리소스의 속성을 통해 실행 중에 예상 되는 리소스를 프로그래밍 방식으로 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-127">In addition to a TSV table, you can programmatically retrieve the resources estimated during the run via the `Data` property of the resources estimator.</span></span> <span data-ttu-id="968a2-128">`Data`속성은 `System.DataTable` 두 개의 열 ( `Metric` 및 `Sum` )이 메트릭의 이름으로 인덱싱되는 인스턴스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-128">The `Data` property provides a `System.DataTable` instance with two columns: `Metric` and `Sum`, indexed by the metrics' names.</span></span>

<span data-ttu-id="968a2-129">다음 코드에서는 `QubitClifford` `T` `CNOT` Q # 작업에서 사용 되는 및 작업의 총 수를 검색 하 고 인쇄 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-129">The following code shows how to retrieve and print the total number of `QubitClifford`, `T` and `CNOT` operations used by a Q# operation:</span></span>

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

## <a name="metrics-reported"></a><span data-ttu-id="968a2-130">보고 된 메트릭</span><span class="sxs-lookup"><span data-stu-id="968a2-130">Metrics Reported</span></span>

<span data-ttu-id="968a2-131">평가기 리소스는 다음 메트릭을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-131">The resources estimator tracks the following metrics:</span></span>

|<span data-ttu-id="968a2-132">메트릭</span><span class="sxs-lookup"><span data-stu-id="968a2-132">Metric</span></span>|<span data-ttu-id="968a2-133">Description</span><span class="sxs-lookup"><span data-stu-id="968a2-133">Description</span></span>|
|----|----|
|<span data-ttu-id="968a2-134">__CNOT__</span><span class="sxs-lookup"><span data-stu-id="968a2-134">__CNOT__</span></span>    |<span data-ttu-id="968a2-135">작업의 실행 수 `CNOT` (제어 된 Pauli X 작업이 라고도 함).</span><span class="sxs-lookup"><span data-stu-id="968a2-135">The run count of `CNOT` operations (also known as Controlled Pauli X operations).</span></span>|
|<span data-ttu-id="968a2-136">__QubitClifford__</span><span class="sxs-lookup"><span data-stu-id="968a2-136">__QubitClifford__</span></span> |<span data-ttu-id="968a2-137">단일 Clifford 및 Pauli 작업의 실행 수입니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-137">The run count of any single qubit Clifford and Pauli operations.</span></span>|
|<span data-ttu-id="968a2-138">__Measure__(측정값)</span><span class="sxs-lookup"><span data-stu-id="968a2-138">__Measure__</span></span>    |<span data-ttu-id="968a2-139">측정의 실행 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-139">The run count of any measurements.</span></span>  |
|<span data-ttu-id="968a2-140">__R__</span><span class="sxs-lookup"><span data-stu-id="968a2-140">__R__</span></span>    |<span data-ttu-id="968a2-141">Clifford 및 Pauli 작업을 제외한 모든 단일 비트 회전의 실행 횟수입니다 `T` .</span><span class="sxs-lookup"><span data-stu-id="968a2-141">The run count of any single-qubit rotations, excluding `T`, Clifford and Pauli operations.</span></span>  |
|<span data-ttu-id="968a2-142">__T__</span><span class="sxs-lookup"><span data-stu-id="968a2-142">__T__</span></span>    |<span data-ttu-id="968a2-143">작업의 실행 수 `T` 및 `T` 작업, T_x = .h 및 T_y = Hy. Hy를 포함 하는 변화 시키고입니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-143">The run count of `T` operations and their conjugates, including the `T` operations, T_x = H.T.H, and T_y = Hy.T.Hy.</span></span>  |
|<span data-ttu-id="968a2-144">__Depth__</span><span class="sxs-lookup"><span data-stu-id="968a2-144">__Depth__</span></span>|<span data-ttu-id="968a2-145">Q # 작업에 의해 실행 되는 퀀텀 회로 깊이의 하 한입니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-145">The lower bound for the depth of the quantum circuit run by the Q# operation.</span></span> <span data-ttu-id="968a2-146">기본적으로 깊이 메트릭은 게이트 수만 계산 `T` 합니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-146">By default, the depth metric only counts `T` gates.</span></span> <span data-ttu-id="968a2-147">자세한 내용은 [깊이 카운터](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="968a2-147">For more details, see [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span></span>   |
|<span data-ttu-id="968a2-148">__Width__</span><span class="sxs-lookup"><span data-stu-id="968a2-148">__Width__</span></span>    |<span data-ttu-id="968a2-149">Q # 작업을 실행 하는 동안 할당 된 최대 수의 수에 대 한 하 한입니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-149">The lower bound for the maximum number of qubits allocated during the run of the Q# operation.</span></span> <span data-ttu-id="968a2-150">__깊이__ 와 __너비__ 의 하한값을 동시에 실현 하지 못할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-150">It might not be possible to achieve both __Depth__ and __Width__ lower bounds simultaneously.</span></span>  |
|<span data-ttu-id="968a2-151">__BorrowedWidth__</span><span class="sxs-lookup"><span data-stu-id="968a2-151">__BorrowedWidth__</span></span>    |<span data-ttu-id="968a2-152">Q # 작업 내에서 빌려 온 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-152">The maximum number of qubits borrowed inside the Q# operation.</span></span>  |

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="968a2-153">측정 결과의 확률 제공</span><span class="sxs-lookup"><span data-stu-id="968a2-153">Providing the probability of measurement outcomes</span></span>

<span data-ttu-id="968a2-154"><xref:microsoft.quantum.diagnostics.assertmeasurementprobability> <xref:microsoft.quantum.diagnostics> 네임 스페이스에서를 사용 하 여 측정 작업의 예상 확률에 대 한 정보를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="968a2-154">You can use <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> from the <xref:microsoft.quantum.diagnostics> namespace to provide information about the expected probability of a measurement operation.</span></span> <span data-ttu-id="968a2-155">자세한 내용은 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="968a2-155">For more information, see [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)</span></span>

## <a name="see-also"></a><span data-ttu-id="968a2-156">참고 항목</span><span class="sxs-lookup"><span data-stu-id="968a2-156">See also</span></span>

- [<span data-ttu-id="968a2-157">퀀텀 추적 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="968a2-157">Quantum trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [<span data-ttu-id="968a2-158">퀀텀 Toffoli 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="968a2-158">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="968a2-159">퀀텀 전체 상태 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="968a2-159">Quantum full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 