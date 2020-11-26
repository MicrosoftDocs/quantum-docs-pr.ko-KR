---
uid: Microsoft.Quantum.Oracles.DiscreteOracle
title: DiscreteOracle 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DiscreteOracle
qsharp.summary: >-
  Represents a discrete-time oracle.

  This is an oracle that implements $U^m$ for a fixed operation $U$ and a non-negative integer $m$.
ms.openlocfilehash: accbd7b88cc2f6522da20ec1959492310ff0e743
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193899"
---
# <a name="discreteoracle-user-defined-type"></a><span data-ttu-id="49427-102">DiscreteOracle 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="49427-102">DiscreteOracle user defined type</span></span>

<span data-ttu-id="49427-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="49427-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="49427-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="49427-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="49427-105">불연속 시간 oracle을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="49427-105">Represents a discrete-time oracle.</span></span>

<span data-ttu-id="49427-106">이는 고정 된 작업 $U $ 및 음수가 아닌 정수 $m $에 대해 ^ m $ $U를 구현 하는 oracle입니다.</span><span class="sxs-lookup"><span data-stu-id="49427-106">This is an oracle that implements $U^m$ for a fixed operation $U$ and a non-negative integer $m$.</span></span>

```qsharp

newtype DiscreteOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```

