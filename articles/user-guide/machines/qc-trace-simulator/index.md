---
title: 양자 컴퓨터 추적 시뮬레이터
description: Microsoft 양자 컴퓨터 추적 시뮬레이터를 사용하여 클래식 코드를 디버그하고 양자 프로그램의 리소스 요구 사항을 예측하는 방법을 알아봅니다.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
ms.openlocfilehash: 4cec688da35951271d87396d9b6a8fed744defc6
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85273774"
---
# <a name="quantum-trace-simulator"></a>양자 추적 시뮬레이터

Microsoft 양자 컴퓨터 추적 시뮬레이터는 실제로 양자 컴퓨터의 상태를 시뮬레이트하지 않고 양자 프로그램을 실행합니다.  이러한 이유로 추적 시뮬레이터는 수천 큐비트를 사용하는 양자 프로그램을 실행할 수 있습니다.  이러한 방식은 다음 두 가지 주요 목적에 유용합니다. 

* 양자 프로그램에 속하는 클래식 코드 디버그 
* 양자 컴퓨터에서 지정된 양자 프로그램 인스턴스를 실행하는 데 필요한 리소스 예측

추적 시뮬레이터는 측정을 수행해야 할 때 사용자가 제공하는 추가 정보에 의존합니다. 이에 대한 자세한 내용은 [측정 결과의 확률 제공](#providing-the-probability-of-measurement-outcomes)을 참조하세요. 

## <a name="providing-the-probability-of-measurement-outcomes"></a>측정 결과의 확률 제공

양자 알고리즘에는 두 가지 종류의 측정값이 표시됩니다. 첫 번째 종류는 사용자가 일반적으로 결과의 확률을 알고 있는 경우에 보조적 역할을 수행합니다. 이 경우 사용자는 이 정보를 나타내기 위해 <xref:microsoft.quantum.intrinsic> 네임스페이스의 <xref:microsoft.quantum.intrinsic.assertprob>을 쓸 수 있습니다. 다음 예제에서는 이에 대해 설명합니다.

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

추적 시뮬레이터가 `AssertProb`를 실행할 때 `source` 및 `q`에 대해 `PauliZ`를 측정하면 확률이 0.5일 때 `Zero` 결과가 제공됩니다. 시뮬레이터는 나중에 `M`을 실행할 경우 기록된 결과 확률 값을 찾을 수 있으며 `M`은 확률이 0.5일 때 `Zero` 또는 `One`을 반환합니다. 양자 상태를 추적하는 동일한 코드를 시뮬레이터에서 실행하는 경우 이러한 시뮬레이터는 `AssertProb`의 제공된 확률이 올바른지 확인합니다.

## <a name="running-your-program-with-the-quantum-computer-trace-simulator"></a>양자 컴퓨터 추적 시뮬레이터를 사용하여 프로그램 실행 

양자 컴퓨터 추적 시뮬레이터는 단지 다른 대상 컴퓨터로 표시될 수 있습니다. 이를 사용하기 위한 C# 드라이버 프로그램은 다른 양자 시뮬레이터용 드라이버 프로그램과 매우 유사합니다. 

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            QCTraceSimulator sim = new QCTraceSimulator();
            var res = MyQuantumProgram.Run(sim).Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

`AssertProb`을 사용하여 주석이 추가되지 않은 측정값이 하나 이상 있는 경우 시뮬레이터는 `Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators` 네임스페이스에서 `UnconstrainedMeasurementException`을 throw합니다. 자세한 내용은 [UnconstrainedMeasurementException](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.UnconstrainedMeasurementException)에 대한 API 설명서를 참조하세요.

추적 시뮬레이터는 양자 프로그램을 실행하는 것 외에도, 프로그램의 버그를 감지하고, 양자 프로그램 리소스 예측을 수행하기 위한 5가지 구성 요소를 제공합니다. 

* [고유 입력 검사기](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs)
* [무효화된 큐비트 사용 검사기](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)
* [기본 연산 카운터](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)
* [회로 깊이 카운터](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)
* [회로 너비 카운터](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)

이러한 각 구성 요소는 `QCTraceSimulatorConfiguration`에서 적절한 플래그를 설정하여 사용하도록 설정할 수 있습니다. 이러한 각 구성 요소를 사용하는 방법에 대한 자세한 내용은 해당 참조 파일에 제공됩니다. 구체적인 세부 정보는 [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration)에 대한 API 설명서를 참조하세요.

## <a name="see-also"></a>참고 항목
양자 컴퓨터 [추적 시뮬레이터](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) C# 참조 

