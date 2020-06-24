---
title: 리소스 개수 가져오기
description: 퀀텀 추적 시뮬레이터를 사용 하 여 리소스 예상치를 얻는 방법에 대해 알아봅니다.
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.resourcecounts
ms.openlocfilehash: 14d0a703a20a801dcee9678a113a33404859a1a9
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275888"
---
# <a name="obtaining-resource-counts"></a>리소스 개수 가져오기

기존 컴퓨터에서 $ 이상 비트 $n 시뮬레이트하는 비용은 $n $로 확대 됩니다. 이는 전체 상태 시뮬레이터로 수행할 수 있는 퀀텀 화학 시뮬레이션의 크기를 크게 제한 합니다. 대량 화학 인스턴스의 경우에도 유용한 정보를 얻을 수 있습니다. 여기서는 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)를 사용 하 여 자동화 된 방식으로 연금술 시뮬레이션에 대 한 T 게이트 또는 cnot 게이트 수와 같은 리소스 비용을 얻을 수 있는 방법을 살펴봅니다. 이러한 정보는 퀀텀 컴퓨터가 이러한 퀀텀 화학 알고리즘을 실행 하기에 충분히 큰 경우에 대해 알립니다. 참조는 제공 된 샘플을 참조 하세요 `GetGateCount` .

`FermionHamiltonian` [파일 로드](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) 예제에서 설명한 것 처럼 Broombridge 스키마에서 로드 된 인스턴스가 이미 있다고 가정 하겠습니다. 

```csharp
    // Filename of Hamiltonian to be loaded.
    var filename = "...";

    // This deserializes Broombridge.
    var problem = Broombridge.Deserializers.DeserializeBroombridge(filename).ProblemDescriptions.First();

    // This is a data structure representing the Jordan-Wigner encoding 
    // of the Hamiltonian that we may pass to a Q# algorithm.
    var qSharpData = problem.ToQSharpFormat();
```

리소스 예상치를 얻기 위한 구문은 전체 상태 시뮬레이터에서 알고리즘을 실행 하는 것과 거의 동일 합니다. 다른 대상 컴퓨터를 선택 하기만 하면 됩니다. 리소스 추정치의 목적을 위해이는 단일 Trotter 단계의 비용 또는 접미사 기술을 통해 만든 퀀텀 워크를 평가 하는 데 사용 됩니다. 이러한 알고리즘을 호출 하는 상용구는 다음과 같습니다.

```qsharp
//////////////////////////////////////////////////////////////////////////
// Using Trotterization //////////////////////////////////////////////////
//////////////////////////////////////////////////////////////////////////

/// # Summary
/// This allocates qubits and applies a single Trotter step.
operation RunTrotterStep (qSharpData: JordanWignerEncodingData) : Unit {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    // We use a Product formula, also known as `Trotterization` to
    // simulate the Hamiltonian.
    // The integrator step size does not affect the gate cost of a single step.
    let trotterStepSize = 1.0;
    
    // Order of integrator
    let trotterOrder = 1;
    let (nQubits, (rescaleFactor, oracle)) = TrotterStepOracle(qSharpData, trotterStepSize, trotterOrder);
    
    // We not allocate qubits an run a single step.
    using (qubits = Qubit[nQubits]) {
        oracle(qubits);
        ResetAll(qubits);
    }
}


//////////////////////////////////////////////////////////////////////////
// Using Qubitization ////////////////////////////////////////////////////
//////////////////////////////////////////////////////////////////////////

/// # Summary
/// This allocates qubits and applies a single qubitization step.
operation RunQubitizationStep (qSharpData: JordanWignerEncodingData) : Double {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    let (nQubits, (l1Norm, oracle)) = QubitizationOracle(qSharpData);
    
    // We now allocate qubits and run a single step.
    using (qubits = Qubit[nQubits]) {
        oracle(qubits);
        ResetAll(qubits);
    }
    
    return l1Norm;
}
```

이제 원하는 리소스를 추적 하도록 추적 시뮬레이터를 구성 합니다. 이 경우 플래그를로 설정 하 여 기본 퀀텀 작업의 수를 계산 `usePrimitiveOperationsCounter` `true` 합니다. `throwOnUnconstraintMeasurement` `false` Q # 코드가 측정 결과의 확률 (있는 경우)을 올바르게 어설션 하지 않는 경우 예외를 방지 하려면 기술 세부 정보를로 설정 합니다.

```csharp
private static QCTraceSimulator CreateAndConfigureTraceSim()
{
    // Create and configure Trace Simulator
    var config = new QCTraceSimulatorConfiguration()
    {
        usePrimitiveOperationsCounter = true,
        throwOnUnconstraintMeasurement = false
    };

    return new QCTraceSimulator(config);
}
```

이제 다음과 같이 드라이버 프로그램에서 퀀텀 알고리즘을 실행 합니다.

```csharp
// Instantiate a trace simulator instance
QCTraceSimulator sim = CreateAndConfigureTraceSim();

// Run the quantum algorithm on the trace simulator.
RunQubitizationStep.Run(sim, qSharpData);

// Print all resource counts to file.
var gateStats = sim.ToCSV();
foreach (var x in gateStats)
{
    System.IO.File.WriteAllLines($"QubitizationGateCountEstimates.{x.Key}.csv", new string[] { x.Value });
}
```