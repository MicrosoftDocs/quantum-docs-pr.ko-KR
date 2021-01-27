---
title: 퀀텀 리소스 평가기-퀀텀 개발 키트
description: 퀀텀 컴퓨터에서 지정 된 작업 인스턴스를 실행 하는 데 필요한 리소스를 추정 하는 Microsoft QDK resources 평가기에 대해 알아봅니다 Q# .
author: anpaz
ms.author: anpaz
ms.date: 06/26/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.resources-estimator
no-loc:
- Q#
- $$v
ms.openlocfilehash: c3aa94c8b34ad7247fbdeab4bf4dcb96ce746014
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847474"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a>QDK (퀀텀 Development Kit) 리소스 평가기

이름에서 알 수 있듯이 `ResourcesEstimator` 클래스는 퀀텀 컴퓨터에서 지정 된 작업 인스턴스를 실행 하는 데 필요한 리소스를 추정 합니다 Q# . 퀀텀 컴퓨터의 상태를 실제로 시뮬레이션 하지 않고 퀀텀 작업을 실행 하 여이 작업을 수행 합니다. 따라서 Q# 코드의 클래식 부분이 적절 한 시간 내에 실행 되는 경우 수천 비트를 사용 하는 작업에 대 한 리소스를 추정 합니다.

평가기 리소스는 프로그램을 디버그 하는 데 도움이 되는 다양 한 메트릭 및 도구 집합을 제공 하는 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)를 기반으로 빌드됩니다 Q# .

## <a name="invoking-and-running-the-resources-estimator"></a>평가기 리소스 호출 및 실행

평가기 리소스를 사용 하 여 모든 작업을 실행할 수 있습니다 Q# . 자세한 내용은 [ Q# 프로그램을 실행 하는 방법](xref:microsoft.quantum.guide.host-programs)을 참조 하세요.

### <a name="invoking-the-resources-estimator-from-c"></a>C에서 평가기 리소스 호출 # 

다른 대상 컴퓨터와 마찬가지로 먼저 `ResourcesEstimator` 클래스의 인스턴스를 만든 다음, 이를 작업의 `Run` 메서드의 첫 번째 매개 변수로 전달합니다.

`QuantumSimulator` 클래스와 달리 `ResourcesEstimator` 클래스는 <xref:System.IDisposable> 인터페이스를 구현하지 않으므로 `using` 문 내에 묶을 필요가 없습니다.

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
|__깊이__|작업에 의해 실행 되는 퀀텀 회로의 깊이 Q# 입니다 ( [아래](#depth-width-and-qubitcount)참조). 기본적으로 깊이 메트릭은 게이트 수만 계산 `T` 합니다. 자세한 내용은 [깊이 카운터](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)를 참조 하세요.   |
|__Width__|작업에 의해 실행 되는 퀀텀 회로의 너비 Q# 입니다 ( [아래](#depth-width-and-qubitcount)참조). 기본적으로 깊이 메트릭은 게이트 수만 계산 `T` 합니다. 자세한 내용은 [Width 카운터](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)를 참조 하세요.   |
|__고 비트 수__    |작업을 실행 하는 동안 할당 된 최대 값 수의 하한값입니다 Q# . 이 메트릭은 __깊이__ 와 호환 되지 않을 수 있습니다 (아래 참조).  |
|__BorrowedWidth__    |작업 내에서 빌려 온 최대 수입니다 Q# .  |


## <a name="depth-width-and-qubitcount"></a>Depth, Width 및  Bitcount

보고 된 깊이 및 너비 예상치는 서로 호환 됩니다.
(이전에는 두 숫자를 모두 달성할 수 있었지만 깊이와 너비를 위해 서로 다른 회로가 필요 합니다.) 현재이 쌍의 두 메트릭은 동시에 동일한 회로를 통해 구현할 수 있습니다.

보고 되는 메트릭은 다음과 같습니다.

__깊이:__ 루트 작업의 경우, 구성 된 게이트 시간을 가정 하 여 실행 하는 데 걸리는 시간입니다.
작업의 시작 및 끝에서 최신 버전의 시간 차이가 나 후속 작업 시간 차이를 계산 합니다.

__너비:__ 루트 작업의 경우-이를 실행 하는 데 실제로 사용 되는 작업 (및 호출 하는 작업)의 수입니다.
작업을 시작할 때 이미 사용 된 것과 같은 작업의 경우 또는 후속 작업에 사용 된 것 보다 더 많은 이상 비트 수입니다.

재사용 된 값은이 숫자에 영향을 주지 않습니다.
즉, 작업 A가 시작 되기 전에 몇 개의 몇 가지 기능을 해제 하 고이 작업에서 요구 하는 모든 기능 (및에서 호출 된 작업)이 이전 릴리스를 다시 사용 하 여 충족 된 경우 작업 A의 너비가 0으로 보고 됩니다. 이 경우에는 너비에 영향을 주지 않습니다.

고 __비트 수:__ 루트 작업의 경우-이 작업을 실행 하는 데 충분 하 고 해당 작업에서 호출 되는 작업을 실행 하기에 충분 한 최소 수의 단일 비트 수입니다.
또는 후속 작업에 대해이 작업을 별도로 실행 하기에 충분 한 최소 수의 단일 비트 수입니다. 이 숫자에는 입력 비트 비트가 포함 되지 않습니다. 여기에는가 포함 됩니다.

두 가지 작업 모드가 지원 됩니다. QCTraceSimulatorConfiguration. OptimizeDepth를 설정 하 여 모드를 선택 합니다.

__OptimizeDepth = false:__ 이것은 기본 모드입니다. 새 항목을 할당 하기 전에 원하는 비트를 다시 사용 하는 것이 좋습니다. 루트 __작업의 경우 너비가 최소__ 너비 (하한값)가 됩니다. 호환 가능한 __깊이가__ 보고 될 수 있습니다. Borrowing가 없는 것으로 가정 하는 루트 작업의 __너비__ 와 동일한 __것이 있습니다__ .

__OptimizeDepth = true:__ 이 기능을 사용 하는 경우에는이 기능을 사용 하지 않는 것이 좋습니다. 루트 작업 __깊이__ 는 최소 깊이 (하한값)가 됩니다. 이 깊이에 대해 호환 되는 __너비가__ 보고 됩니다. 둘 다 동시에 달성할 수 있습니다. 너비를 최적화 하기 위해 프로그램에서 나중에 발생 한 게이트는 프로그램에서 이전에 발생 한 게이트 이전에 예약 될 수 있지만, 깊이는 최소 수준으로 유지 되는 방식으로 다시 사용 하도록 예약 됩니다. 시간 값을 기반으로 하는 이상 값을 다시 사용 하는 경우에는 게이트 시간을 정수 값으로 구성 하는 것이 좋습니다. __너비가__ 최적이 아닐 수도 있습니다. 추가 정보는 [추적 프로그램의 백서 너비와 깊이](https://github.com/microsoft/qsharp-runtime/tree/main/src/Simulation/Simulators/QCTraceSimulator/Docs)에서 찾을 수 있습니다.

## <a name="providing-the-probability-of-measurement-outcomes"></a>측정 결과의 확률 제공

<xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> <xref:Microsoft.Quantum.Diagnostics> 네임 스페이스에서를 사용 하 여 측정 작업의 예상 확률에 대 한 정보를 제공할 수 있습니다. 자세한 내용은 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 를 참조 하세요.

## <a name="see-also"></a>참고 항목

- [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [퀀텀 Toffoli 시뮬레이터](xref:microsoft.quantum.machines.toffoli-simulator)
- [퀀텀 전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator) 
