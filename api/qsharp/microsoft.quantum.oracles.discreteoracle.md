---
uid: Microsoft.Quantum.Oracles.DiscreteOracle
title: DiscreteOracle 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DiscreteOracle
qsharp.summary: >-
  Represents a discrete-time oracle.

  This is an oracle that implements $U^m$ for a fixed operation $U$ and a non-negative integer $m$.
ms.openlocfilehash: ccbcc92d4b6f1c800b576ad54739d26665e6d6d5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724925"
---
# <a name="discreteoracle-user-defined-type"></a><span data-ttu-id="282a6-102">DiscreteOracle 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="282a6-102">DiscreteOracle user defined type</span></span>

<span data-ttu-id="282a6-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="282a6-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="282a6-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="282a6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="282a6-105">불연속 시간 oracle을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="282a6-105">Represents a discrete-time oracle.</span></span>

<span data-ttu-id="282a6-106">이는 고정 된 작업 $U $ 및 음수가 아닌 정수 $m $에 대해 ^ m $ $U를 구현 하는 oracle입니다.</span><span class="sxs-lookup"><span data-stu-id="282a6-106">This is an oracle that implements $U^m$ for a fixed operation $U$ and a non-negative integer $m$.</span></span>

```qsharp

newtype DiscreteOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```

