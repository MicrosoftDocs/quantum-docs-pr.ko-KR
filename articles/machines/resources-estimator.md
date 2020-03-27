---
title: 평가기 퀀텀 개발 키트 리소스
description: '퀀텀 컴퓨터에서 지정 된 Q # 작업 인스턴스를 실행 하는 데 필요한 리소스를 예측 하는 평가기 리소스에 대해 알아봅니다.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 1/22/2019
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: 51186134e9279727fec212cdce84f69493aaa656
ms.sourcegitcommit: a0e50c5f07841b99204c068cf5b5ec8ed087ffea
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/26/2020
ms.locfileid: "80320819"
---
# <a name="the-resourcesestimator-target-machine"></a>ResourcesEstimator 대상 컴퓨터

이름에서 알 수 있듯이 `ResourcesEstimator`는 퀀텀 컴퓨터에서 지정 된 Q # 작업 인스턴스를 실행 하는 데 필요한 리소스를 추정 합니다.
퀀텀 컴퓨터의 상태를 실제로 시뮬레이션 하지 않고 퀀텀 작업을 실행 하 여이 작업을 수행 합니다. 따라서 코드의 고전적인 부분이 적절 한 시간 내에 실행 될 수 있는 경우 수천 비트를 사용 하는 Q # 작업에 대 한 리소스를 예상할 수 있습니다.

## <a name="usage"></a>사용

`ResourcesEstimator`은 다른 유형의 대상 컴퓨터 일 뿐 이므로 모든 Q # 작업을 실행 하는 데 사용할 수 있습니다. 

다른 대상 컴퓨터와 같이 C# 호스트 프로그램에서 사용 하려면 인스턴스를 만들고 작업의 `Run` 메서드에 대 한 첫 번째 매개 변수로 전달 합니다.

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

예제에서 볼 수 있듯이 `ResourcesEstimator`은 파일에 저장 하거나 분석을 위해 콘솔에 기록할 수 있는 탭으로 구분 된 값 (TSV)이 있는 테이블을 생성 하는 `ToTSV()` 메서드를 제공 합니다. 위의 프로그램의 출력은 다음과 같습니다.

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
> `ResourcesEstimator`는 모든 실행에 대해 계산을 다시 설정 하지 않습니다. 동일한 인스턴스가 다른 작업을 실행 하는 데 사용 되는 경우 기존 결과의 맨 위에 집계 수가 유지 됩니다.
> 실행 간에 계산을 다시 설정 해야 하는 경우 모든 실행에 대해 새 인스턴스를 만듭니다.


## <a name="programmatically-retrieving-the-estimated-data"></a>프로그래밍 방식으로 예상 데이터 검색

TSV 테이블 외에도 `ResourcesEstimator`의 `Data` 속성을 통해 예상 리소스를 프로그래밍 방식으로 검색할 수 있습니다. `Data`는 두 개의 열이 있는 `System.DataTable` 인스턴스를 제공 합니다. `Metric` 및 `Sum`는 메트릭 이름으로 인덱싱됩니다.

다음 코드는 Q # 작업에서 사용 하는 `QubitClifford`, `T` 및 `CNOT` 게이트의 총 수를 검색 하 고 인쇄 하는 방법을 보여 줍니다.

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

다음은 `ResourcesEstimator`에서 예상 하는 메트릭 목록입니다.

* __Cnot__: cnot (제어 된 Pauli X 게이트 라고도 함) 게이트를 실행 했습니다.
* __QubitClifford__: 실행 된 단일 Clifford 및 Pauli 게이트의 수입니다.
* __Measure__: 실행 된 측정값의 수입니다.
* __R__: T, Clifford 및 Pauli 게이트를 제외 하 고 실행 된 단일 비트 회전의 수입니다.
* __T__: t 게이트, T_x = .h 및 T_y = Hy)를 포함 한 t 게이트 및 해당 변화 시키고의 수를 실행 합니다.
* __Depth__: Q # 작업에 의해 실행 되는 퀀텀 회로의 깊이입니다. 기본적으로 T 게이트만 깊이에서 계산 됩니다. 자세한 내용은 [깊이 카운터](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) 를 참조 하세요.
* __Width__: Q # 작업을 실행 하는 동안 할당 된 최고 비트 수입니다.
* __BorrowedWidth__: Q # 작업 내에서 빌려 온 최대 수 비트 수입니다.


## <a name="providing-the-probability-of-measurement-outcomes"></a>측정 결과의 확률 제공

<xref:microsoft.quantum.intrinsic> 네임 스페이스의 <xref:microsoft.quantum.intrinsic.assertprob>를 사용 하 여 Q # 프로그램의 실행을 구동 하는 데 도움이 되는 예상 측정 확률에 대 한 정보를 제공할 수 있습니다. 다음 예제에서는 이에 대해 설명합니다.

```qsharp
operation Teleport(source : Qubit, target : Qubit) : Unit {

    using (qubit = Qubit()) {

        H(q);
        CNOT(qubit, target);

        CNOT(source, qubit);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [qubit], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(qubit) == One) { X(target); X(qubit); }
    }
}
```

`ResourcesEstimator`에서 `AssertProb` 발생 하면 `source`에 대 한 `PauliZ` 측정을 기록 하 고 확률 0.5에 `q` 결과를 제공 해야 합니다.`Zero` 나중에 `M` 실행 되는 경우 결과 확률의 기록 된 값을 찾아 `M` 확률 0.5에 `Zero` 또는 `One`을 반환 합니다.


## <a name="see-also"></a>참고 항목

`ResourcesEstimator`은 다양 한 메트릭 집합, 전체 호출 그래프에서 메트릭을 보고 하는 기능, 질문 # 프로그램에서 버그를 찾는 데 도움이 되는 [고유한 입력 검사기](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) 와 같은 기능을 제공 하는 퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)를 기반으로 빌드됩니다. 자세한 내용은 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 설명서를 참조 하세요.

