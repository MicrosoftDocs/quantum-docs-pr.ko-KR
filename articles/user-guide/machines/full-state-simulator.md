---
title: 전체 상태 퀀텀 시뮬레이터-퀀텀 개발 키트
description: Q#Microsoft Quantum Development Kit 전체 상태 시뮬레이터에서 프로그램을 실행 하는 방법에 대해 알아봅니다.
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
no-loc:
- Q#
- $$v
ms.openlocfilehash: b15af66123dadae09815cde1966c69b3ce2e9e64
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868341"
---
# <a name="quantum-development-kit-qdk-full-state-simulator"></a><span data-ttu-id="ad565-103">QDK (퀀텀 Development Kit) 전체 상태 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="ad565-103">Quantum Development Kit (QDK) full state simulator</span></span>

<span data-ttu-id="ad565-104">QDK은 로컬 컴퓨터의 퀀텀 컴퓨터를 시뮬레이트하는 전체 상태 시뮬레이터를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad565-104">The QDK provides a full state simulator that simulates a quantum machine on your local computer.</span></span> <span data-ttu-id="ad565-105">전체 상태 시뮬레이터를 사용 하 여 Q# 최대 30 개의 이상으로 작성 된 퀀텀 알고리즘을 실행 하 고 디버그할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad565-105">You can use the full state simulator to run and debug quantum algorithms written in Q#, utilizing up to 30 qubits.</span></span> <span data-ttu-id="ad565-106">전체 상태 시뮬레이터는 Microsoft Research의 [Liq $ Ui | \rangle $](http://stationq.github.io/Liquid/) 플랫폼에서 사용 되는 퀀텀 시뮬레이터와 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="ad565-106">The full state simulator is similar to the quantum simulator used in the  [LIQ$Ui|\rangle$](http://stationq.github.io/Liquid/) platform from Microsoft Research.</span></span>

## <a name="invoking-and-running-the-full-state-simulator"></a><span data-ttu-id="ad565-107">전체 상태 시뮬레이터 호출 및 실행</span><span class="sxs-lookup"><span data-stu-id="ad565-107">Invoking and running the full state simulator</span></span>

<span data-ttu-id="ad565-108">클래스를 통해 전체 상태 시뮬레이터를 노출 합니다 `QuantumSimulator` .</span><span class="sxs-lookup"><span data-stu-id="ad565-108">You expose the full state simulator via the `QuantumSimulator` class.</span></span> <span data-ttu-id="ad565-109">자세한 내용은 [ Q# 프로그램을 실행 하는 방법](xref:microsoft.quantum.guide.host-programs)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ad565-109">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-simulator-from-c"></a><span data-ttu-id="ad565-110">C에서 시뮬레이터 호출 #</span><span class="sxs-lookup"><span data-stu-id="ad565-110">Invoking the simulator from C#</span></span>

<span data-ttu-id="ad565-111">클래스의 인스턴스를 만든 `QuantumSimulator` 다음 `Run` 추가 매개 변수와 함께 퀀텀 작업의 메서드로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad565-111">Create an instance of the `QuantumSimulator` class and then pass it to the `Run` method of a quantum operation, along with any additional parameters.</span></span>
```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

<span data-ttu-id="ad565-112">`QuantumSimulator`클래스가 인터페이스를 구현 하므로 <xref:System.IDisposable> `Dispose` 시뮬레이터의 인스턴스가 더 이상 필요 하지 않은 경우 메서드를 호출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad565-112">Because the `QuantumSimulator` class implements the <xref:System.IDisposable> interface, you must call the `Dispose` method once you do not need the instance of the simulator anymore.</span></span> <span data-ttu-id="ad565-113">이 작업을 수행 하는 가장 좋은 방법은 메서드를 자동으로 호출 하는 [using](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/using-statement) 문 내에서 시뮬레이터 선언과 작업을 래핑하는 것입니다 `Dispose` .</span><span class="sxs-lookup"><span data-stu-id="ad565-113">The best way to do this is to wrap the simulator declaration and operations within a [using](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/using-statement) statement, which automatically calls the `Dispose` method.</span></span>

### <a name="invoking-the-simulator-from-python"></a><span data-ttu-id="ad565-114">Python에서 시뮬레이터 호출</span><span class="sxs-lookup"><span data-stu-id="ad565-114">Invoking the simulator from Python</span></span>

<span data-ttu-id="ad565-115">가져온 작업과 함께 Python 라이브러리의 [시뮬레이트 ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) 메서드를 사용 합니다 Q# Q# .</span><span class="sxs-lookup"><span data-stu-id="ad565-115">Use the [simulate()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) method from the Q# Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.simulate()
```

### <a name="invoking-the-simulator-from-the-command-line"></a><span data-ttu-id="ad565-116">명령줄에서 시뮬레이터 호출</span><span class="sxs-lookup"><span data-stu-id="ad565-116">Invoking the simulator from the command line</span></span>

<span data-ttu-id="ad565-117">Q#명령줄에서 프로그램을 실행 하는 경우 전체 상태 시뮬레이터가 기본 대상 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="ad565-117">When running a Q# program from the command line, the full state simulator is the default target machine.</span></span> <span data-ttu-id="ad565-118">필요에 따라 **--시뮬레이터** (또는 **-s** 바로 가기) 매개 변수를 사용 하 여 원하는 대상 컴퓨터를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad565-118">Optionally, you can use the **--simulator** (or **-s** shortcut) parameter to specify the desired target machine.</span></span> <span data-ttu-id="ad565-119">다음 명령은 모두 전체 상태 시뮬레이터를 사용 하 여 프로그램을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad565-119">Both of the following commands run a program using the full state simulator.</span></span> 

```dotnetcli
dotnet run
dotnet run -s QuantumSimulator
```

### <a name="invoking-the-simulator-from-juptyer-notebooks"></a><span data-ttu-id="ad565-120">Juptyer 노트북에서 시뮬레이터 호출</span><span class="sxs-lookup"><span data-stu-id="ad565-120">Invoking the simulator from Juptyer Notebooks</span></span>

<span data-ttu-id="ad565-121">Q#-매직 명령 [% 시뮬레이트](xref:microsoft.quantum.iqsharp.magic-ref.simulate) 를 사용 하 여 작업을 실행 Q# 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad565-121">Use the IQ# magic command [%simulate](xref:microsoft.quantum.iqsharp.magic-ref.simulate) to run the Q# operation.</span></span>

```
%simulate myOperation
```
## <a name="seeding-the-simulator"></a><span data-ttu-id="ad565-122">시뮬레이터 시드</span><span class="sxs-lookup"><span data-stu-id="ad565-122">Seeding the simulator</span></span>

<span data-ttu-id="ad565-123">기본적으로 전체 상태 시뮬레이터는 난수 생성기를 사용 하 여 퀀텀 임의성을 시뮬레이션 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad565-123">By default, the full state simulator uses a random number generator to simulate quantum randomness.</span></span> <span data-ttu-id="ad565-124">테스트를 위해 결정적 결과를 사용 하는 것이 유용한 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad565-124">For testing purposes, it is sometimes useful to have deterministic results.</span></span> <span data-ttu-id="ad565-125">C # 프로그램에서 `QuantumSimulator` 매개 변수를 통해 생성자에 난수 생성기의 초기값을 제공 하 여이를 수행할 수 있습니다 `randomNumberGeneratorSeed` .</span><span class="sxs-lookup"><span data-stu-id="ad565-125">In a C# program, you can accomplish this by providing a seed for the random number generator in the `QuantumSimulator` constructor via the `randomNumberGeneratorSeed` parameter.</span></span>

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="configuring-threads"></a><span data-ttu-id="ad565-126">스레드 구성</span><span class="sxs-lookup"><span data-stu-id="ad565-126">Configuring threads</span></span>

<span data-ttu-id="ad565-127">전체 상태 시뮬레이터는 [OpenMP](http://www.openmp.org/) 를 사용 하 여 필요한 선형 대 수을 병렬화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad565-127">The full state simulator uses [OpenMP](http://www.openmp.org/) to parallelize the linear algebra required.</span></span> <span data-ttu-id="ad565-128">기본적으로 OpenMP는 사용 가능한 모든 하드웨어 스레드를 사용 합니다. 즉, 실제 작업을 dwarfs는 데 필요한 조정이 필요한 경우에 따라 적은 수의 수의 수를 포함 하는 프로그램이 느리게 실행 되는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="ad565-128">By default, OpenMP uses all available hardware threads, which means that programs with small numbers of qubits often runs slowly because the coordination that is required dwarfs the actual work.</span></span> <span data-ttu-id="ad565-129">환경 변수를 작은 숫자로 설정 하면이 문제를 해결할 수 있습니다 `OMP_NUM_THREADS` .</span><span class="sxs-lookup"><span data-stu-id="ad565-129">You can fix this by setting the environment variable `OMP_NUM_THREADS` to a small number.</span></span> <span data-ttu-id="ad565-130">이에 대 한 규칙은 최대 4 개의 최대 4 개의 스레드를 구성한 다음 추가 스레드 하나를 추가 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ad565-130">As a rule of thumb, configure one thread for up to four qubits, and then one additional thread per qubit.</span></span> <span data-ttu-id="ad565-131">알고리즘에 따라 변수를 조정 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad565-131">You might need to adjust the variable depending on your algorithm.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad565-132">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ad565-132">See also</span></span>

- [<span data-ttu-id="ad565-133">퀀텀 리소스 예측 도구</span><span class="sxs-lookup"><span data-stu-id="ad565-133">Quantum resources estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)
- [<span data-ttu-id="ad565-134">퀀텀 Toffoli 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="ad565-134">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="ad565-135">퀀텀 추적 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="ad565-135">Quantum trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)