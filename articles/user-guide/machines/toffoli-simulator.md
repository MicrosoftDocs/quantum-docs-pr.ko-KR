---
title: 퀀텀 Toffoli 시뮬레이터-퀀텀 개발 키트
description: 수백만 개의 다양 한 비트와 함께 사용할 수 있는 특별 한 용도의 퀀텀 시뮬레이터 인 Microsoft QDK Toffoli 시뮬레이터에 대해 알아봅니다.
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 6/25/2020
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
no-loc:
- Q#
- $$v
ms.openlocfilehash: 8a981645703423856e667be7c3dccf5270a5885f
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868103"
---
# <a name="quantum-development-kit-qdk-toffoli-simulator"></a><span data-ttu-id="ea1a1-103">QDK (퀀텀 Development Kit) Toffoli 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="ea1a1-103">Quantum Development Kit (QDK) Toffoli simulator</span></span>

<span data-ttu-id="ea1a1-104">QDK Toffoli 시뮬레이터는 제한 된 범위의 특수 한 용도의 시뮬레이터로 `X` , `CNOT` 및 다중 제어 된 `X` 퀀텀 작업만 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-104">The QDK Toffoli simulator is a special-purpose simulator with a limited scope and only supports `X`, `CNOT`, and multi-controlled `X` quantum operations.</span></span> <span data-ttu-id="ea1a1-105">모든 기존 논리 및 계산을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-105">All classical logic and computations are available.</span></span>

<span data-ttu-id="ea1a1-106">Toffoli 시뮬레이터는 [전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator)보다 기능이 더 제한적 이지만 훨씬 더 많은 기능을 시뮬레이션할 수 있다는 이점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-106">While the Toffoli simulator is more restricted in functionality than the [full state simulator](xref:microsoft.quantum.machines.full-state-simulator), it has the advantage of being able to simulate far more qubits.</span></span> <span data-ttu-id="ea1a1-107">Toffoli 시뮬레이터는 수백만의 비트와 함께 사용할 수 있지만 전체 상태 시뮬레이터는 약 30 개 이상으로 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-107">The Toffoli simulator can be used with millions of qubits, while the full state simulator is limited to about 30 qubits.</span></span> <span data-ttu-id="ea1a1-108">이는 부울 함수를 평가 하는 oracles와 함께 사용 하는 것이 유용 합니다. 지원 되는 알고리즘 집합을 사용 하 여 구현 하 고 많은 수의 다양 한 기능을 통해 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-108">This is useful, for example, with oracles that evaluate Boolean functions - they can be implemented using the limited set of supported algorithms and tested on a large number of qubits.</span></span>

## <a name="invoking-the-toffoli-simulator"></a><span data-ttu-id="ea1a1-109">Toffoli 시뮬레이터 호출</span><span class="sxs-lookup"><span data-stu-id="ea1a1-109">Invoking the Toffoli simulator</span></span>

<span data-ttu-id="ea1a1-110">클래스를 통해 Toffoli 시뮬레이터를 노출 합니다 `ToffoliSimulator` .</span><span class="sxs-lookup"><span data-stu-id="ea1a1-110">You expose the Toffoli simulator via the `ToffoliSimulator` class.</span></span> <span data-ttu-id="ea1a1-111">자세한 내용은 [ Q# 프로그램을 실행 하는 방법](xref:microsoft.quantum.guide.host-programs)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-111">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-toffoli-simulator-from-c"></a><span data-ttu-id="ea1a1-112">C에서 Toffoli 시뮬레이터 호출 #</span><span class="sxs-lookup"><span data-stu-id="ea1a1-112">Invoking the Toffoli simulator from C#</span></span>

<span data-ttu-id="ea1a1-113">다른 대상 컴퓨터와 마찬가지로 먼저 `ToffoliSimulator` 클래스의 인스턴스를 만든 다음, 이를 작업의 `Run` 메서드의 첫 번째 매개 변수로 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-113">As with other target machines, you first create an instance of the `ToffoliSimulator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="ea1a1-114">`QuantumSimulator` 클래스와 달리 `ToffoliSimulator` 클래스는 <xref:System.IDisposable> 인터페이스를 구현하지 않으므로 `using` 문 내에 묶을 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-114">Note that, unlike the `QuantumSimulator` class, the `ToffoliSimulator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

### <a name="invoking-the-toffoli-simulator-from-python"></a><span data-ttu-id="ea1a1-115">Python에서 Toffoli 시뮬레이터 호출</span><span class="sxs-lookup"><span data-stu-id="ea1a1-115">Invoking the Toffoli simulator from Python</span></span>

<span data-ttu-id="ea1a1-116">가져온 작업과 함께 Python 라이브러리의 [toffoli_simulate ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) 메서드를 사용 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="ea1a1-116">Use the [toffoli_simulate()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) method from the Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.toffoli_simulate()
```

### <a name="invoking-the-toffoli-simulator-from-the-command-line"></a><span data-ttu-id="ea1a1-117">명령줄에서 Toffoli 시뮬레이터 호출</span><span class="sxs-lookup"><span data-stu-id="ea1a1-117">Invoking the Toffoli simulator from the command line</span></span>

<span data-ttu-id="ea1a1-118">명령줄에서 프로그램을 실행 하는 경우 Q# **--시뮬레이터** (또는 **-s** 바로 가기) 매개 변수를 사용 하 여 Toffoli 시뮬레이터 대상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-118">When running a Q# program from the command line, use the **--simulator** (or **-s** shortcut) parameter to specify the Toffoli simulator target machine.</span></span> <span data-ttu-id="ea1a1-119">다음 명령은 평가기 리소스를 사용 하 여 프로그램을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-119">The following command runs a program using the resources estimator:</span></span> 

```dotnetcli
dotnet run -s ToffoliSimulator
```

### <a name="invoking-the-toffoli-simulator-from-juptyer-notebooks"></a><span data-ttu-id="ea1a1-120">Juptyer 노트북에서 Toffoli 시뮬레이터 호출</span><span class="sxs-lookup"><span data-stu-id="ea1a1-120">Invoking the Toffoli simulator from Juptyer Notebooks</span></span>

<span data-ttu-id="ea1a1-121">Q#-매직 명령 [% toffoli을 (](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) 를) 사용 하 여 작업을 실행 Q# 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-121">Use the IQ# magic command [%toffoli](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) to run the Q# operation.</span></span>

```
%toffoli myOperation
```

## <a name="supported-operations"></a><span data-ttu-id="ea1a1-122">지원되는 작업</span><span class="sxs-lookup"><span data-stu-id="ea1a1-122">Supported operations</span></span>

<span data-ttu-id="ea1a1-123">Toffoli 시뮬레이터는 다음을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-123">The Toffoli simulator supports:</span></span>

* <span data-ttu-id="ea1a1-124">회전 및 지수화 Paulis는 `R` `Exp` 결과 작업이 같거나 항등 매트릭스가 될 때 및 등입니다 `X` .</span><span class="sxs-lookup"><span data-stu-id="ea1a1-124">Rotations and exponentiated Paulis, such as `R` and `Exp`, when the resulting operation equals `X` or the identity matrix.</span></span>
* <span data-ttu-id="ea1a1-125">측정 및 [어설션](xref:microsoft.quantum.diagnostics.assertmeasurement) 작업 뿐만 아니라 Pauli에만 해당 `Z` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-125">Measurement and [assert](xref:microsoft.quantum.diagnostics.assertmeasurement) operations, but only in the Pauli `Z` basis.</span></span> <span data-ttu-id="ea1a1-126">측정 연산의 확률은 항상 **0** 또는 **1**입니다. Toffoli 시뮬레이터에는 임의성이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-126">Note that a measurement operation's probability is always either **0** or **1**; there is no randomness in the Toffoli simulator.</span></span>
* <span data-ttu-id="ea1a1-127">`DumpMachine`및 `DumpRegister` 함수</span><span class="sxs-lookup"><span data-stu-id="ea1a1-127">`DumpMachine` and `DumpRegister` functions.</span></span>
<span data-ttu-id="ea1a1-128">두 함수는 `Z` 각 비트의 현재 기본 상태를 한 줄에 하나씩 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-128">Both functions output the current `Z`-basis state of each qubit, one qubit per line.</span></span>

## <a name="specifying-the-number-of-qubits"></a><span data-ttu-id="ea1a1-129">비트 수 지정</span><span class="sxs-lookup"><span data-stu-id="ea1a1-129">Specifying the number of qubits</span></span>

<span data-ttu-id="ea1a1-130">기본적으로 인스턴스는 `ToffoliSimulator` 65536의 공간을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-130">By default, a `ToffoliSimulator` instance allocates space for 65,536 qubits.</span></span>
<span data-ttu-id="ea1a1-131">알고리즘이이 보다 더 많은 비트를 필요로 하는 경우 매개 변수의 값을 생성자에 제공 하 여 원하는 비트 수를 지정할 수 있습니다 `qubitCount` .</span><span class="sxs-lookup"><span data-stu-id="ea1a1-131">If your algorithm requires more qubits than this, you can specify the qubit count by providing a value for the `qubitCount` parameter to the constructor.</span></span>
<span data-ttu-id="ea1a1-132">각 추가 비트에는 1 바이트의 메모리만 필요 하므로 필요한 overestimating의 수를 크게 줄일 수 있는 비용은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ea1a1-132">Each additional qubit requires only one byte of memory, so there is no significant cost to overestimating the number of qubits you'll need.</span></span>

<span data-ttu-id="ea1a1-133">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="ea1a1-133">For example:</span></span>

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```

## <a name="see-also"></a><span data-ttu-id="ea1a1-134">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ea1a1-134">See also</span></span>

- [<span data-ttu-id="ea1a1-135">평가기 퀀텀 리소스</span><span class="sxs-lookup"><span data-stu-id="ea1a1-135">Quantum Resources Estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)
- [<span data-ttu-id="ea1a1-136">퀀텀 추적 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="ea1a1-136">Quantum Trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [<span data-ttu-id="ea1a1-137">퀀텀 전체 상태 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="ea1a1-137">Quantum Full State simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 