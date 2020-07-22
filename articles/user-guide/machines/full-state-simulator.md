---
title: 전체 상태 퀀텀 시뮬레이터-퀀텀 개발 키트
description: 'Microsoft Quantum Development Kit 전체 상태 시뮬레이터에서 Q # 프로그램을 실행 하는 방법에 대해 알아봅니다.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: 563fdbd2a45461d112e4c46651eddd75c6fc3db2
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871181"
---
# <a name="quantum-development-kit-qdk-full-state-simulator"></a>QDK (퀀텀 Development Kit) 전체 상태 시뮬레이터

QDK은 로컬 컴퓨터의 퀀텀 컴퓨터를 시뮬레이트하는 전체 상태 시뮬레이터를 제공 합니다. 전체 상태 시뮬레이터를 사용 하 여 Q #으로 작성 된 퀀텀 알고리즘을 실행 하 고 디버그할 수 있습니다. 여기에는 최대 30 개의 이상 비트가 사용 됩니다. 전체 상태 시뮬레이터는 Microsoft Research의 [Liq $ Ui | \rangle $](http://stationq.github.io/Liquid/) 플랫폼에서 사용 되는 퀀텀 시뮬레이터와 비슷합니다.

## <a name="invoking-and-running-the-full-state-simulator"></a>전체 상태 시뮬레이터 호출 및 실행

클래스를 통해 전체 상태 시뮬레이터를 노출 합니다 `QuantumSimulator` . 자세한 내용은 [Q # 프로그램을 실행 하는 방법](xref:microsoft.quantum.guide.host-programs)을 참조 하세요.

### <a name="invoking-the-simulator-from-c"></a>C에서 시뮬레이터 호출 #

클래스의 인스턴스를 만든 `QuantumSimulator` 다음 `Run` 추가 매개 변수와 함께 퀀텀 작업의 메서드로 전달 합니다.
```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

`QuantumSimulator`클래스가 인터페이스를 구현 하므로 <xref:System.IDisposable> `Dispose` 시뮬레이터의 인스턴스가 더 이상 필요 하지 않은 경우 메서드를 호출 해야 합니다. 이 작업을 수행 하는 가장 좋은 방법은 메서드를 자동으로 호출 하는 [using](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/using-statement) 문 내에서 시뮬레이터 선언과 작업을 래핑하는 것입니다 `Dispose` .

### <a name="invoking-the-simulator-from-python"></a>Python에서 시뮬레이터 호출

가져온 Q # 작업으로 Q # Python 라이브러리의 [시뮬레이트 ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) 메서드를 사용 합니다.

```python
qubit_result = myOperation.simulate()
```

### <a name="invoking-the-simulator-from-the-command-line"></a>명령줄에서 시뮬레이터 호출

명령줄에서 Q # 프로그램을 실행 하는 경우 전체 상태 시뮬레이터가 기본 대상 컴퓨터입니다. 필요에 따라 **--시뮬레이터** (또는 **-s** 바로 가기) 매개 변수를 사용 하 여 원하는 대상 컴퓨터를 지정할 수 있습니다. 다음 명령은 모두 전체 상태 시뮬레이터를 사용 하 여 프로그램을 실행 합니다. 

```dotnetcli
dotnet run
dotnet run -s QuantumSimulator
```

### <a name="invoking-the-simulator-from-juptyer-notebooks"></a>Juptyer 노트북에서 시뮬레이터 호출

IQ # magic 명령 [% 시뮬레이트](xref:microsoft.quantum.iqsharp.magic-ref.simulate) 를 사용 하 여 Q # 작업을 실행 합니다.

```
%simulate myOperation
```
## <a name="seeding-the-simulator"></a>시뮬레이터 시드

기본적으로 전체 상태 시뮬레이터는 난수 생성기를 사용 하 여 퀀텀 임의성을 시뮬레이션 합니다. 테스트를 위해 결정적 결과를 사용 하는 것이 유용한 경우도 있습니다. C # 프로그램에서 `QuantumSimulator` 매개 변수를 통해 생성자에 난수 생성기의 초기값을 제공 하 여이를 수행할 수 있습니다 `randomNumberGeneratorSeed` .

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="configuring-threads"></a>스레드 구성

전체 상태 시뮬레이터는 [OpenMP](http://www.openmp.org/) 를 사용 하 여 필요한 선형 대 수을 병렬화 합니다. 기본적으로 OpenMP는 사용 가능한 모든 하드웨어 스레드를 사용 합니다. 즉, 실제 작업을 dwarfs는 데 필요한 조정이 필요한 경우에 따라 적은 수의 수의 수를 포함 하는 프로그램이 느리게 실행 되는 경우가 많습니다. 환경 변수를 작은 숫자로 설정 하면이 문제를 해결할 수 있습니다 `OMP_NUM_THREADS` . 이에 대 한 규칙은 최대 4 개의 최대 4 개의 스레드를 구성한 다음 추가 스레드 하나를 추가 하는 것입니다. 알고리즘에 따라 변수를 조정 해야 할 수 있습니다.

## <a name="see-also"></a>참고 항목

- [평가기 퀀텀 리소스](xref:microsoft.quantum.machines.resources-estimator)
- [퀀텀 Toffoli 시뮬레이터](xref:microsoft.quantum.machines.toffoli-simulator)
- [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)