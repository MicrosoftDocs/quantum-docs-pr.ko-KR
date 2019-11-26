---
title: 평가기 퀀텀 개발 키트 리소스 | Microsoft Docs
description: Microsoft의 퀀텀 개발 키트 리소스 개요 평가기
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 1/22/2019
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: 591e306b3001934bd81342a533e3f6ca25129781
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184987"
---
# <a name="the-resourcesestimator-target-machine"></a><span data-ttu-id="20aa9-103">ResourcesEstimator 대상 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="20aa9-103">The ResourcesEstimator Target Machine</span></span>

<span data-ttu-id="20aa9-104">이름에서 알 수 있듯이 `ResourcesEstimator`는 퀀텀 컴퓨터에서 지정 된 Q # 작업 인스턴스를 실행 하는 데 필요한 리소스를 추정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-104">As the name implies, the `ResourcesEstimator` estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>
<span data-ttu-id="20aa9-105">퀀텀 컴퓨터의 상태를 실제로 시뮬레이션 하지 않고 퀀텀 작업을 실행 하 여이 작업을 수행 합니다. 따라서 수천 비트를 사용 하는 Q # 작업에 대 한 리소스를 예상할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-105">It accomplishes this by executing the quantum operation without actually simulating the state of a quantum computer; for this reason, it can estimate resources for Q# operations that use thousands of qubits.</span></span>

## <a name="usage"></a><span data-ttu-id="20aa9-106">사용량</span><span class="sxs-lookup"><span data-stu-id="20aa9-106">Usage</span></span>

<span data-ttu-id="20aa9-107">`ResourcesEstimator`은 다른 유형의 대상 컴퓨터 일 뿐 이므로 모든 Q # 작업을 실행 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-107">The `ResourcesEstimator` is just another type of target machine, thus it can be used to run any Q# operation.</span></span> 

<span data-ttu-id="20aa9-108">다른 대상 컴퓨터와 같이 C# 호스트 프로그램에서 사용 하려면 인스턴스를 만들고 작업의 `Run` 메서드에 대 한 첫 번째 매개 변수로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-108">As other target machines, to use it on a C# host program create an instance and pass it as the first parameter of the operation's `Run` method:</span></span>

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

<span data-ttu-id="20aa9-109">예제에서 볼 수 있듯이 `ResourcesEstimator`은 파일에 저장 하거나 분석을 위해 콘솔에 기록할 수 있는 탭으로 구분 된 값 (TSV)이 있는 테이블을 생성 하는 `ToTSV()` 메서드를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-109">As the example shows, the `ResourcesEstimator` provides a `ToTSV()` method to generate a table with tab-seperated-values (TSV) that can be saved into a file or written to the console for analysis.</span></span> <span data-ttu-id="20aa9-110">위의 프로그램의 출력은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-110">The output of the above program should look something like this:</span></span>

```Output
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
> <span data-ttu-id="20aa9-111">`ResourcesEstimator`는 모든 실행에 대해 계산을 다시 설정 하지 않습니다. 동일한 인스턴스가 다른 작업을 실행 하는 데 사용 되는 경우 기존 결과의 맨 위에 집계 수가 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-111">The `ResourcesEstimator` does not reset its calculations on every run, if the same instance is used to execute another operation it will keep aggregating counts on top of existing results.</span></span>
> <span data-ttu-id="20aa9-112">실행 간에 계산을 다시 설정 해야 하는 경우 모든 실행에 대해 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-112">If you need to reset calculations between runs, create a new instance for every execution.</span></span>


## <a name="programmatically-retrieving-the-estimated-data"></a><span data-ttu-id="20aa9-113">프로그래밍 방식으로 예상 데이터 검색</span><span class="sxs-lookup"><span data-stu-id="20aa9-113">Programmatically Retrieving the Estimated Data</span></span>

<span data-ttu-id="20aa9-114">TSV 테이블 외에도 `ResourcesEstimator`의 `Data` 속성을 통해 예상 리소스를 프로그래밍 방식으로 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-114">In addition to a TSV table, the resources estimated can be retrieved programmatically via the `ResourcesEstimator`'s `Data` property.</span></span> <span data-ttu-id="20aa9-115">`Data`는 두 개의 열이 있는 `System.DataTable` 인스턴스를 제공 합니다. `Metric` 및 `Sum`는 메트릭 이름으로 인덱싱됩니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-115">`Data` provides a `System.DataTable` instance with two columns: `Metric` and `Sum`, indexed by the metrics names.</span></span>

<span data-ttu-id="20aa9-116">다음 코드는 Q # 작업에서 사용 하는 `QubitClifford`, `T` 및 `CNOT` 게이트의 총 수를 검색 하 고 인쇄 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-116">The following code shows how to retrieve and print the total number of `QubitClifford`, `T` and `CNOT` gates used by a Q# operation:</span></span>

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

## <a name="metrics-reported"></a><span data-ttu-id="20aa9-117">보고 된 메트릭</span><span class="sxs-lookup"><span data-stu-id="20aa9-117">Metrics Reported</span></span>

<span data-ttu-id="20aa9-118">다음은 `ResourcesEstimator`에서 예상 하는 메트릭 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-118">The following is the list of metrics estimated by the `ResourcesEstimator`:</span></span>

* <span data-ttu-id="20aa9-119">__Cnot__: cnot (제어 된 Pauli X 게이트 라고도 함) 게이트를 실행 했습니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-119">__CNOT__: The count of CNOT (also known as the Controlled Pauli X gate) gates executed.</span></span>
* <span data-ttu-id="20aa9-120">__QubitClifford__: 실행 된 단일 Clifford 및 Pauli 게이트의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-120">__QubitClifford__: The count of any single qubit Clifford and Pauli gates executed.</span></span>
* <span data-ttu-id="20aa9-121">__Measure__: 실행 된 측정값의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-121">__Measure__:  The count of any measurements executed.</span></span>
* <span data-ttu-id="20aa9-122">__R__: T, Clifford 및 Pauli 게이트를 제외 하 고 실행 된 단일 비트 회전의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-122">__R__: The count of any single qubit rotations executed, excluding T, Clifford and Pauli gates.</span></span>
* <span data-ttu-id="20aa9-123">__T__: t 게이트, T_x = .H 및 T_y = Hy를 포함 하 여 t 게이트 및 해당 변화 시키고의 수를 실행 했습니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-123">__T__: The count of T gates and their conjugates, including the T gate, T_x = H.T.H, and T_y = Hy.T.Hy, executed.</span></span>
* <span data-ttu-id="20aa9-124">__Depth__: Q # 작업에 의해 실행 되는 퀀텀 회로의 깊이입니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-124">__Depth__: Depth of the quantum circuit executed by the Q# operation.</span></span> <span data-ttu-id="20aa9-125">기본적으로 T 게이트만 깊이에서 계산 됩니다. 자세한 내용은 [깊이 카운터](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="20aa9-125">By default, only T gates are counted in the depth, see [depth counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) for details.</span></span>
* <span data-ttu-id="20aa9-126">__Width__: Q # 작업을 실행 하는 동안 할당 된 최고 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-126">__Width__: Maximum number of qubits allocated during the execution of the Q# operation.</span></span>
* <span data-ttu-id="20aa9-127">__BorrowedWidth__: Q # 작업 내에서 빌려 온 최대 수 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-127">__BorrowedWidth__: Maximum number of qubits borrowed inside the Q# operation.</span></span>


## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="20aa9-128">측정 결과의 확률 제공</span><span class="sxs-lookup"><span data-stu-id="20aa9-128">Providing the Probability of Measurement Outcomes</span></span>

<span data-ttu-id="20aa9-129"><xref:microsoft.quantum.primitive> 네임 스페이스의 <xref:microsoft.quantum.primitive.assertprob>를 사용 하 여 Q # 프로그램의 실행을 구동 하는 데 도움이 되는 예상 측정 확률에 대 한 정보를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-129"><xref:microsoft.quantum.primitive.assertprob> from the <xref:microsoft.quantum.primitive> namespace can be used to provide information about the expected probability of a measurement to help drive the execution of the Q# program.</span></span> <span data-ttu-id="20aa9-130">다음 예제에서는 이에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-130">The following example illustrates this:</span></span>

```qsharp
operation Teleportation (source : Qubit, target : Qubit) : Unit {

    using (ancilla = Qubit()) {

        H(ancilla);
        CNOT(ancilla, target);

        CNOT(source, ancilla);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [ancilla], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(ancilla) == One) { X(target); X(ancilla); }
    }
}
```

<span data-ttu-id="20aa9-131">`ResourcesEstimator`에서 `AssertProb` 발생 하면 `source`에 대 한 `PauliZ` 측정을 기록 하 고 확률 0.5에 `ancilla` 결과를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-131">When the `ResourcesEstimator` encounters `AssertProb` it will record that measuring `PauliZ` on `source` and `ancilla` should be given an outcome of `Zero` with probability 0.5.</span></span> <span data-ttu-id="20aa9-132">나중에 `M` 실행 되는 경우 결과 확률의 기록 된 값을 찾아 `M` 확률 0.5에 `Zero` 또는 `One`을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-132">When it executes `M` later, it will find the recorded values of the outcome probabilities and `M` will return `Zero` or `One` with probability 0.5.</span></span>


## <a name="see-also"></a><span data-ttu-id="20aa9-133">참고 항목</span><span class="sxs-lookup"><span data-stu-id="20aa9-133">See also</span></span>

<span data-ttu-id="20aa9-134">`ResourcesEstimator`은 다양 한 메트릭 집합, 전체 호출 그래프에서 메트릭을 보고 하는 기능, 질문 # 프로그램에서 버그를 찾는 데 도움이 되는 [고유한 입력 검사기](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) 와 같은 기능을 제공 하는 퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)를 기반으로 빌드됩니다.</span><span class="sxs-lookup"><span data-stu-id="20aa9-134">The `ResourcesEstimator` is built on top of the quantum computer [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), which provides a richer set of metrics, the ability to report metrics on the full call-graph, and features like [distinct inputs checker](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) to help find bugs on Q# programs.</span></span> <span data-ttu-id="20aa9-135">자세한 내용은 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="20aa9-135">Please refer to the [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) documentation for more information.</span></span>
