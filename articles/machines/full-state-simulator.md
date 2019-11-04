---
title: 퀀텀 개발 키트 전체 상태 시뮬레이터 | Microsoft Docs
description: Microsoft의 퀀텀 개발 키트 전체 상태 시뮬레이터 개요
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 12/7/2017
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: ab0e65765d27e301a59948d7c02105a523022e68
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184681"
---
# <a name="quantum-development-kit-full-state-simulator"></a><span data-ttu-id="e8908-103">퀀텀 개발 키트 전체 상태 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="e8908-103">Quantum Development Kit Full State Simulator</span></span>

<span data-ttu-id="e8908-104">퀀텀 개발 키트는 Microsoft Research의 [Liq $ Ui | \rangle $](http://stationq.github.io/Liquid/) 와 유사한 전체 상태 퀀텀 시뮬레이터를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8908-104">The Quantum Development Kit provides a full state quantum simulator similar to [LIQ$Ui|\rangle$](http://stationq.github.io/Liquid/) from Microsoft Research.</span></span>
<span data-ttu-id="e8908-105">이 시뮬레이터는 컴퓨터에서 Q #으로 작성 된 퀀텀 알고리즘을 실행 하 고 디버그 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8908-105">This simulator can be used to execute and debug quantum algorithms written in Q# on your computer.</span></span>

<span data-ttu-id="e8908-106">이 퀀텀 시뮬레이터는 `QuantumSimulator` 클래스를 통해 노출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8908-106">This quantum simulator is exposed via the `QuantumSimulator` class.</span></span> <span data-ttu-id="e8908-107">시뮬레이터를 사용 하려면이 클래스의 인스턴스를 만들고 나머지 매개 변수와 함께 실행 하려는 퀀텀 작업의 `Run` 메서드에 전달 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8908-107">To use the simulator, simply create an instance of this class and pass it to the `Run` method of the quantum operation you want to execute along with the rest of the parameters:</span></span>

```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

## <a name="idisposable"></a><span data-ttu-id="e8908-108">IDisposable</span><span class="sxs-lookup"><span data-stu-id="e8908-108">IDisposable</span></span>

<span data-ttu-id="e8908-109">`QuantumSimulator` 클래스는 <xref:System.IDisposable>를 구현 하므로 시뮬레이터 인스턴스가 더 이상 사용 되지 않으면 `Dispose` 메서드를 호출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8908-109">The `QuantumSimulator` class implements <xref:System.IDisposable>, thus the `Dispose` method should be called once the instance of the simulator is not used anymore.</span></span> <span data-ttu-id="e8908-110">이 작업을 수행 하는 가장 좋은 방법은 위의 예제와 같이 `using` 문 내에서 시뮬레이터를 래핑하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e8908-110">The best way to do this is to wrap the simulator within a `using` statement, as in the example above.</span></span>

## <a name="seed"></a><span data-ttu-id="e8908-111">시드는</span><span class="sxs-lookup"><span data-stu-id="e8908-111">Seed</span></span>

<span data-ttu-id="e8908-112">`QuantumSimulator` 난수 생성기를 사용 하 여 퀀텀 임의성을 시뮬레이션 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8908-112">The `QuantumSimulator` uses a random number generator to simulate quantum randomness.</span></span> <span data-ttu-id="e8908-113">테스트를 위해 결정적 결과를 사용 하는 것이 유용한 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8908-113">For testing purposes, it is sometimes useful to have deterministic results.</span></span> <span data-ttu-id="e8908-114">이 작업을 수행 하려면 `randomNumberGeneratorSeed` 매개 변수를 통해 `QuantumSimulator`의 생성자에 난수 생성기의 초기값을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8908-114">This can be accomplished by providing a seed for the random number generator in the `QuantumSimulator`'s constructor via the `randomNumberGeneratorSeed` parameter:</span></span>

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="threads"></a><span data-ttu-id="e8908-115">스레드</span><span class="sxs-lookup"><span data-stu-id="e8908-115">Threads</span></span>

<span data-ttu-id="e8908-116">`QuantumSimulator`는 [OpenMP](http://www.openmp.org/) 를 사용 하 여 필요한 선형 대 수을 병렬화 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8908-116">The `QuantumSimulator` uses [OpenMP](http://www.openmp.org/) to parallelize the linear algebra required.</span></span> <span data-ttu-id="e8908-117">기본적으로 OpenMP는 사용 가능한 모든 하드웨어 스레드를 사용 합니다. 즉, 필요한 조정이 실제 작업을 dwarf 하기 때문에 적은 수의 비트를 포함 하는 프로그램이 느리게 실행 되는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="e8908-117">By default OpenMP uses all available hardware threads, which means that programs with small numbers of qubits will often run slowly because the coordination required will dwarf the actual work.</span></span> <span data-ttu-id="e8908-118">환경 변수 `OMP_NUM_THREADS`을 작은 숫자로 설정 하면이 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8908-118">This can be fixed by setting the environment variable `OMP_NUM_THREADS` to a small number.</span></span> <span data-ttu-id="e8908-119">매우 대략적인 규칙으로, 스레드 1 개는 최대 약 4 개의 highbit에 적합 한 다음, 추가 스레드는 알고리즘에 따라 달라 지지만 좋은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e8908-119">As a very rough rule of thumb, 1 thread is good for up to about 4 qubits, and then an additional thread per qubit is good, although this is highly dependent on your algorithm.</span></span>

