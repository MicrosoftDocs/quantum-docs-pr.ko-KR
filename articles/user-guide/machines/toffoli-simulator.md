---
title: 퀀텀 Toffoli 시뮬레이터-퀀텀 개발 키트
description: 수백만 개의 다양 한 비트와 함께 사용할 수 있는 특별 한 용도의 퀀텀 시뮬레이터 인 Microsoft QDK Toffoli 시뮬레이터에 대해 알아봅니다.
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 6/25/2020
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
ms.openlocfilehash: a6ceee592e628215511ec83475d9e25bf54674f7
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/21/2020
ms.locfileid: "86870620"
---
# <a name="quantum-development-kit-qdk-toffoli-simulator"></a>QDK (퀀텀 Development Kit) Toffoli 시뮬레이터

QDK Toffoli 시뮬레이터는 제한 된 범위의 특수 한 용도의 시뮬레이터로 `X` , `CNOT` 및 다중 제어 된 `X` 퀀텀 작업만 지원 합니다. 모든 기존 논리 및 계산을 사용할 수 있습니다.

Toffoli 시뮬레이터는 [전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator)보다 기능이 더 제한적 이지만 훨씬 더 많은 기능을 시뮬레이션할 수 있다는 이점이 있습니다. Toffoli 시뮬레이터는 수백만의 비트와 함께 사용할 수 있지만 전체 상태 시뮬레이터는 약 30 개 이상으로 제한 됩니다. 이는 부울 함수를 평가 하는 oracles와 함께 사용 하는 것이 유용 합니다. 지원 되는 알고리즘 집합을 사용 하 여 구현 하 고 많은 수의 다양 한 기능을 통해 테스트할 수 있습니다.

## <a name="invoking-the-toffoli-simulator"></a>Toffoli 시뮬레이터 호출

클래스를 통해 Toffoli 시뮬레이터를 노출 합니다 `ToffoliSimulator` . 자세한 내용은 [Q # 프로그램을 실행 하는 방법](xref:microsoft.quantum.guide.host-programs)을 참조 하세요.

### <a name="invoking-the-toffoli-simulator-from-c"></a>C에서 Toffoli 시뮬레이터 호출 #

다른 대상 컴퓨터와 마찬가지로 먼저 클래스의 인스턴스를 만든 `ToffoliSimulator` 다음 작업 메서드의 첫 번째 매개 변수로 전달 `Run` 합니다.

클래스와 달리 `QuantumSimulator` `ToffoliSimulator` 클래스는 인터페이스를 구현 하지 않으므로 <xref:System.IDisposable> 문 내에 묶을 필요가 없습니다 `using` .

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

### <a name="invoking-the-toffoli-simulator-from-python"></a>Python에서 Toffoli 시뮬레이터 호출

가져온 Q # 작업을 사용 하 여 Python 라이브러리의 [toffoli_simulate ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) 메서드를 사용 합니다.

```python
qubit_result = myOperation.toffoli_simulate()
```

### <a name="invoking-the-toffoli-simulator-from-the-command-line"></a>명령줄에서 Toffoli 시뮬레이터 호출

명령줄에서 Q # 프로그램을 실행 하는 경우 **--시뮬레이터** (또는 **-s** 바로 가기) 매개 변수를 사용 하 여 Toffoli 시뮬레이터 대상 컴퓨터를 지정 합니다. 다음 명령은 평가기 리소스를 사용 하 여 프로그램을 실행 합니다. 

```dotnetcli
dotnet run -s ToffoliSimulator
```

### <a name="invoking-the-toffoli-simulator-from-juptyer-notebooks"></a>Juptyer 노트북에서 Toffoli 시뮬레이터 호출

IQ # magic 명령 [% toffoli을 (](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) 를) 사용 하 여 Q # 작업을 실행 합니다.

```
%toffoli myOperation
```

## <a name="supported-operations"></a>지원되는 작업

Toffoli 시뮬레이터는 다음을 지원 합니다.

* 회전 및 지수화 Paulis는 `R` `Exp` 결과 작업이 같거나 항등 매트릭스가 될 때 및 등입니다 `X` .
* 측정 및 [어설션](xref:microsoft.quantum.diagnostics.assertmeasurement) 작업 뿐만 아니라 Pauli에만 해당 `Z` 됩니다. 측정 연산의 확률은 항상 **0** 또는 **1**입니다. Toffoli 시뮬레이터에는 임의성이 없습니다.
* `DumpMachine`및 `DumpRegister` 함수
두 함수는 `Z` 각 비트의 현재 기본 상태를 한 줄에 하나씩 출력 합니다.

## <a name="specifying-the-number-of-qubits"></a>비트 수 지정

기본적으로 인스턴스는 `ToffoliSimulator` 65536의 공간을 할당 합니다.
알고리즘이이 보다 더 많은 비트를 필요로 하는 경우 매개 변수의 값을 생성자에 제공 하 여 원하는 비트 수를 지정할 수 있습니다 `qubitCount` .
각 추가 비트에는 1 바이트의 메모리만 필요 하므로 필요한 overestimating의 수를 크게 줄일 수 있는 비용은 없습니다.

예를 들면 다음과 같습니다.

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```

## <a name="see-also"></a>참고 항목

- [평가기 퀀텀 리소스](xref:microsoft.quantum.machines.resources-estimator)
- [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [퀀텀 전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator) 