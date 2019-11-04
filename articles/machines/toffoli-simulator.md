---
title: 퀀텀 개발 키트 Toffoli 시뮬레이터 | Microsoft Docs
description: Microsoft의 퀀텀 Development Kit Toffoli 시뮬레이터 개요
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 01/16/2019
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
ms.openlocfilehash: 26940d1a8fe31f1035e2d23a68940cd999517c6b
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442355"
---
# <a name="quantum-development-kit-toffoli-simulator"></a>퀀텀 개발 키트 Toffoli 시뮬레이터

퀀텀 개발 키트는 Toffoli 시뮬레이터를 제공 합니다 .이 시뮬레이터는 X, CNOT 및 다중 제어 된 X 퀀텀 작업으로 제한 되는 퀀텀 알고리즘을 시뮬레이션할 수 있는 특수 한 용도의 시뮬레이터입니다. 모든 기존 논리 및 계산을 사용할 수 있습니다.

Toffoli 시뮬레이터는 [전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator)보다 작업에서 훨씬 더 제한적 이지만 훨씬 더 많은 비트를 시뮬레이션할 수 있습니다.
Toffoli 시뮬레이터는 수백만 개의 다양 한 비트와 함께 사용할 수 있지만 전체 상태 시뮬레이터는 일반적으로 약 30 개로 제한 됩니다.
컴퓨터에서 Q #으로 작성 된 제한 된 퀀텀 알고리즘 집합을 실행 하 고 디버그할 수 있습니다. 예를 들어, 부울 함수를 평가 하는 oracles는 이러한 게이트를 사용 하 여 구현 될 수 있으므로이 시뮬레이터를 사용 하 여 많은 수의 다양 한 수의로 테스트 됩니다.

이 퀀텀 시뮬레이터는 `ToffoliSimulator` 클래스를 통해 노출 됩니다.
시뮬레이터를 사용 하려면이 클래스의 인스턴스를 만들고 나머지 매개 변수와 함께 실행 하려는 퀀텀 작업의 `Run` 메서드에 전달 하면 됩니다.

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

## <a name="other-operations"></a>기타 작업

`ToffoliSimulator`는 `R` 및 `Exp`와 같이 결과 작업이 `X` 또는 id 인 경우 회전을 지원 합니다.

측정 및 어설션이 지원 되지만 Pauli `Z` 기준 으로만 지원 됩니다.
일부 측정의 확률은 항상 0 또는 1입니다. Toffoli 시뮬레이터에는 임의성이 없습니다.

`DumpMachine` 및 `DumpRegister` 지원 됩니다.
두 가지 모두 각 고 비트의 현재 `Z`기반 상태를 선 마다 하나씩 출력 합니다.

## <a name="qubitcount"></a>고 비트 수

기본적으로 `ToffoliSimulator`는 65536의 공간을 할당 합니다.
알고리즘에이 보다 많은 값이 필요한 경우 생성자에 `qubitCount` 매개 변수에 대 한 값을 제공 하 여 원하는 비트 수를 변경할 수 있습니다.
각 추가 비트에는 추가 바이트의 메모리가 필요 하므로 필요한 overestimating의 수를 크게 줄일 수 있습니다.

다음은 그 예입니다.

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```
