---
uid: Microsoft.Quantum.Oracles.ContinuousOracle
title: ContinuousOracle 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ContinuousOracle
qsharp.summary: >-
  Represents a continuous-time oracle.

  This is an oracle that implements $U(\delta t) : \ket{\psi(t)} \mapsto \ket{\psi(t + \delta t)}$ for all times $t$, where $U$ is a fixed operation, and where $\delta t$ is a non-negative real number.
ms.openlocfilehash: ac254b7556878550216d5c0c9222620fdc5c5702
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855926"
---
# <a name="continuousoracle-user-defined-type"></a><span data-ttu-id="6ed79-102">ContinuousOracle 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="6ed79-102">ContinuousOracle user defined type</span></span>

<span data-ttu-id="6ed79-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="6ed79-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="6ed79-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6ed79-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6ed79-105">연속 시간 oracle을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6ed79-105">Represents a continuous-time oracle.</span></span>

<span data-ttu-id="6ed79-106">이는 $U (\delta t)를 구현 하는 oracle입니다. 모든 시간에 대 한 \ket{\psi (t)} \maps\ket{\psi (t + \delta t)} $ $t $, 여기서 $U $은 고정 연산이 며 $ \delta t $는 음수가 아닌 실수입니다.</span><span class="sxs-lookup"><span data-stu-id="6ed79-106">This is an oracle that implements $U(\delta t) : \ket{\psi(t)} \mapsto \ket{\psi(t + \delta t)}$ for all times $t$, where $U$ is a fixed operation, and where $\delta t$ is a non-negative real number.</span></span>

```qsharp

newtype ContinuousOracle = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

