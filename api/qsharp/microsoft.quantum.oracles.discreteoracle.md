---
uid: Microsoft.Quantum.Oracles.DiscreteOracle
title: DiscreteOracle 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DiscreteOracle
qsharp.summary: >-
  Represents a discrete-time oracle.

  This is an oracle that implements $U^m$ for a fixed operation $U$ and a non-negative integer $m$.
ms.openlocfilehash: 4b85f58889ef9cc55518009bdd9b59bdb2b5b842
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842566"
---
# <a name="discreteoracle-user-defined-type"></a>DiscreteOracle 사용자 정의 형식

네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


불연속 시간 oracle을 나타냅니다.

이는 고정 된 작업 $U $ 및 음수가 아닌 정수 $m $에 대해 ^ m $ $U를 구현 하는 oracle입니다.

```qsharp

newtype DiscreteOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```

