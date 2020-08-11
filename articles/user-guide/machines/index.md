---
title: 퀀텀 시뮬레이터 및 Q# 프로그램
description: Q# 프로그램의 대상 컴퓨터로 사용할 수 있는 퀀텀 시뮬레이터에 대해 설명합니다.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 6/17/2020
ms.topic: article
uid: microsoft.quantum.machines
no-loc:
- Q#
- $$v
ms.openlocfilehash: 77401ca3642b89d708f338f852dc60bf7346b87b
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868307"
---
# <a name="quantum-simulators"></a>퀀텀 시뮬레이터

퀀텀 시뮬레이터는 클래식 컴퓨터에서 실행되고 Q# 프로그램을 위한 *대상 컴퓨터* 역할을 하는 소프트웨어 프로그램으로, 큐비트가 다른 작업에 반응하는 방식을 예측하는 환경에서 퀀텀 프로그램을 실행하고 테스트할 수 있습니다. 이 문서에서는 QDK(Quantum Development Kit)에 포함된 퀀텀 시뮬레이터와 명령줄을 통하거나 기존 언어로 작성된 드라이버 코드를 사용하여 Q# 프로그램을 퀀텀 시뮬레이터에 전달할 수 있는 다양한 방법에 대해 설명합니다.  



## <a name="the-quantum-development-kit-qdk-quantum-simulators"></a>QDK(Quantum Development Kit) 퀀텀 시뮬레이터

퀀텀 시뮬레이터는 알고리즘을 위한 퀀텀 기본 형식을 구현합니다. 여기에는 `H`, `CNOT` 및 `Measure`와 같은 기본 작업뿐만 아니라, 큐비트 관리와 추적도 포함됩니다. QDK에는 동일한 퀀텀 알고리즘에 대해 여러 실행 모델을 나타내는 여러 클래스의 퀀텀 시뮬레이터가 있습니다. 


각 유형의 퀀텀 시뮬레이터는 이러한 기본 형식의 다른 구현을 제공할 수 있습니다. 예를 들어, [전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator)는 [퀀텀 상태 벡터](xref:microsoft.quantum.glossary#quantum-state)를 완전히 시뮬레이션하여 퀀텀 알고리즘을 실행하는 반면 [양자 컴퓨터 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)는 실제 퀀텀 상태를 전혀 고려하지 않습니다. 대신 알고리즘에 대한 게이트, 큐비트 및 기타 리소스 사용을 추적합니다.

### <a name="quantum-machine-classes"></a>양자 컴퓨터 클래스

향후, QDK는 다른 유형의 시뮬레이션을 지원하고 퀀텀 하드웨어에서 실행할 수 있도록 지원하는 추가 양자 컴퓨터 클래스를 정의할 예정입니다. 기본 컴퓨터 구현을 변경하면서 알고리즘은 일정하게 유지하면 시뮬레이션에서 알고리즘을 쉽게 테스트하고 디버그한 다음, 알고리즘이 변경되지 않았다는 확신을 가지고 실제 하드웨어에서 실행할 수 있습니다.

QDK에는 `Microsoft.Quantum.Simulation.Simulators` 네임스페이스에 모두 정의된 여러 양자 컴퓨터 클래스가 있습니다.

|시뮬레이터 |클래스|Description|
|-----|------|---|
|[전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator)| `QuantumSimulator` | 퀀텀 알고리즘을 실행 및 디버그하고 약 30큐비트로 제한됩니다. |
|[단순 리소스 예측 도구](xref:microsoft.quantum.machines.resources-estimator)| `ResourcesEstimator` | 퀀텀 알고리즘을 실행하는 데 필요한 리소스를 최상위 수준에서 분석하고 수천 큐비트를 지원합니다.|
|[추적 기반 리소스 예측 도구](xref:microsoft.quantum.machines.qc-trace-simulator.intro)|  `QCTraceSimulator` |알고리즘의 전체 호출 그래프에 대해 리소스 사용량을 자세히 분석하고 수천 큐비트를 지원합니다.|
|[Toffoli 시뮬레이터](xref:microsoft.quantum.machines.toffoli-simulator)| `ToffoliSimulator` |`X`, `CNOT` 및 다중 제어 `X` 퀀텀 작업으로 제한되는 퀀텀 알고리즘을 시뮬레이션하고 수백만 큐비트를 지원합니다. |

## <a name="invoking-the-quantum-simulator"></a>퀀텀 시뮬레이터 호출

[Q# 프로그램을 실행하는 방법](xref:microsoft.quantum.guide.host-programs)에서는 Q# 코드를 퀀텀 시뮬레이터에 전달하는 세 가지 방법을 보여줍니다. 

* 명령줄 사용
* Python 호스트 프로그램 사용
* C# 호스트 프로그램 사용

양자 컴퓨터는 일반적인 .NET 클래스의 인스턴스로, .NET 클래스와 마찬가지로 해당 생성자를 호출하여 생성됩니다. 이 작업을 수행하는 방법은 Q# 프로그램을 실행하는 방법에 따라 달라집니다.

## <a name="next-steps"></a>다음 단계

* 서로 다른 환경에서 Q# 프로그램에 대한 대상 컴퓨터를 호출하는 방법에 대한 자세한 내용은 [Q# 프로그램을 실행하는 방법](xref:microsoft.quantum.guide.host-programs)을 참조하세요.
