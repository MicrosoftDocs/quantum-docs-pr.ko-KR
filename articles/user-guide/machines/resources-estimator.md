---
title: 퀀텀 리소스 평가기-퀀텀 개발 키트
description: 퀀텀 컴퓨터에서 지정 된 작업 인스턴스를 실행 하는 데 필요한 리소스를 추정 하는 Microsoft QDK resources 평가기에 대해 알아봅니다 Q# .
author: anpaz-msft
ms.author: anpaz
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
no-loc:
- Q#
- $$v
ms.openlocfilehash: 6138c098a4efe2797c7d7360573ddcb9cb70a6c1
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835930"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a>QDK (퀀텀 Development Kit) 리소스 평가기

이름에서 알 수 있듯이 `ResourcesEstimator` 클래스는 퀀텀 컴퓨터에서 지정 된 작업 인스턴스를 실행 하는 데 필요한 리소스를 추정 합니다 Q# . 퀀텀 컴퓨터의 상태를 실제로 시뮬레이션 하지 않고 퀀텀 작업을 실행 하 여이 작업을 수행 합니다. 따라서 Q# 코드의 클래식 부분이 적절 한 시간 내에 실행 되는 경우 수천 비트를 사용 하는 작업에 대 한 리소스를 추정 합니다.

평가기 리소스는 프로그램을 디버그 하는 데 도움이 되는 다양 한 메트릭 및 도구 집합을 제공 하는 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)를 기반으로 빌드됩니다 Q# .

## <a name="invoking-and-running-the-resources-estimator"></a>평가기 리소스 호출 및 실행

평가기 리소스를 사용 하 여 모든 작업을 실행할 수 있습니다 Q# . 자세한 내용은 [ Q# 프로그램을 실행 하는 방법](xref:microsoft.quantum.guide.host-programs)을 참조 하세요.

### <a name="invoking-the-resources-estimator-from-c"></a>C에서 평가기 리소스 호출 # 

다른 대상 컴퓨터와 마찬가지로 먼저 `ResourceEstimator` 클래스의 인스턴스를 만든 다음, 이를 작업의 `Run` 메서드의 첫 번째 매개 변수로 전달합니다.

`QuantumSimulator` 클래스와 달리 `ResourceEstimator` 클래스는 <xref:System.IDisposable> 인터페이스를 구현하지 않으므로 `using` 문 내에 묶을 필요가 없습니다.

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

예제에 나와 있는 것 처럼는 `ResourcesEstimator` `ToTSV()` 탭으로 구분 된 값 (TSV)이 있는 테이블을 생성 하는 메서드를 제공 합니다. 테이블을 파일에 저장 하거나 분석을 위해 콘솔에 표시할 수 있습니다. 다음은 이전 프로그램의 샘플 출력입니다.

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
> `ResourcesEstimator`인스턴스는 실행 때마다 계산을 다시 설정 하지 않습니다. 동일한 인스턴스를 사용 하 여 다른 작업을 실행 하는 경우 새 결과를 기존 결과로 집계 합니다. 실행 간에 계산을 다시 설정 해야 하는 경우 모든 실행에 대해 새 인스턴스를 만듭니다.

### <a name="invoking-the-resources-estimator-from-python"></a>Python에서 평가기 리소스 호출

가져온 작업과 함께 Python 라이브러리의 [estimate_resources ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) 메서드를 사용 합니다 Q# .

```python
qubit_result = myOperation.estimate_resources()
```

### <a name="invoking-the-resources-estimator-from-the-command-line"></a>명령줄에서 리소스 평가기 호출

명령줄에서 프로그램을 실행 하는 경우 Q# **--시뮬레이터** (또는 **-s** 바로 가기) 매개 변수를 사용 하 여 `ResourcesEstimator` 대상 컴퓨터를 지정 합니다. 다음 명령은 평가기 리소스를 사용 하 여 프로그램을 실행 합니다. 

```dotnetcli
dotnet run -s ResourcesEstimator
```

### <a name="invoking-the-resources-estimator-from-juptyer-notebooks"></a>Juptyer 노트북에서 평가기 리소스 호출

Q#작업을 실행 하려면 a 매직 명령 [% 예상 값](xref:microsoft.quantum.iqsharp.magic-ref.simulate) 을 사용 Q# 합니다.

```
%estimate myOperation
```

## <a name="programmatically-retrieving-the-estimated-data"></a>프로그래밍 방식으로 예상 데이터 검색

TSV 테이블 외에도 `Data` 평가기 리소스의 속성을 통해 실행 중에 예상 되는 리소스를 프로그래밍 방식으로 검색할 수 있습니다. `Data`속성은 `System.DataTable` 두 개의 열 ( `Metric` 및 `Sum` )이 메트릭의 이름으로 인덱싱되는 인스턴스를 제공 합니다.

다음 코드에서는 `QubitClifford` `T` `CNOT` 작업에서 사용 되는 및 작업의 총 수를 검색 하 고 인쇄 하는 방법을 보여 줍니다 Q# .

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

## <a name="metrics-reported"></a>보고 된 메트릭

평가기 리소스는 다음 메트릭을 추적 합니다.

|메트릭|설명|
|----|----|
|__CNOT__    |작업의 실행 수 `CNOT` (제어 된 Pauli X 작업이 라고도 함).|
|__QubitClifford__ |단일 Clifford 및 Pauli 작업의 실행 수입니다.|
|__측정값__    |측정의 실행 횟수입니다.  |
|__R__    |Clifford 및 Pauli 작업을 제외한 모든 단일 비트 회전의 실행 횟수입니다 `T` .  |
|__T__    |작업의 실행 수 `T` 및 `T` 작업, T_x = .h 및 T_y = Hy. Hy를 포함 하는 변화 시키고입니다.  |
|__Depth__|작업에 의해 실행 되는 퀀텀 회로 깊이의 하 한입니다 Q# . 기본적으로 깊이 메트릭은 게이트 수만 계산 `T` 합니다. 자세한 내용은 [깊이 카운터](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)를 참조 하세요.   |
|__Width__    |작업을 실행 하는 동안 할당 된 최대 값 수의 하한값입니다 Q# . __깊이__ 와 __너비__ 의 하한값을 동시에 실현 하지 못할 수도 있습니다.  |
|__BorrowedWidth__    |작업 내에서 빌려 온 최대 수입니다 Q# .  |

## <a name="providing-the-probability-of-measurement-outcomes"></a>측정 결과의 확률 제공

<xref:microsoft.quantum.diagnostics.assertmeasurementprobability> <xref:microsoft.quantum.diagnostics> 네임 스페이스에서를 사용 하 여 측정 작업의 예상 확률에 대 한 정보를 제공할 수 있습니다. 자세한 내용은 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 를 참조 하세요.

## <a name="see-also"></a>참고 항목

- [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [퀀텀 Toffoli 시뮬레이터](xref:microsoft.quantum.machines.toffoli-simulator)
- [퀀텀 전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator) 