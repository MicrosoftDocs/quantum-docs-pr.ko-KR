---
uid: Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
title: TimeDependentGeneratorSystem 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentGeneratorSystem
qsharp.summary: Represents a time-dependent dynamical generator as a function from time to the value of the dynamical generator at that time.
ms.openlocfilehash: 144a44448c9fda7a038b17ac7c49f63e8cc4dd55
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719876"
---
# <a name="timedependentgeneratorsystem-user-defined-type"></a><span data-ttu-id="bc7c5-102">TimeDependentGeneratorSystem 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="bc7c5-102">TimeDependentGeneratorSystem user defined type</span></span>

<span data-ttu-id="bc7c5-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="bc7c5-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="bc7c5-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bc7c5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bc7c5-105">시간에 따른 동적 생성기를 시간에서 동적 생성기 값 까지의 함수로 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bc7c5-105">Represents a time-dependent dynamical generator as a function from time to the value of the dynamical generator at that time.</span></span>

```qsharp

newtype TimeDependentGeneratorSystem = ((Double -> Microsoft.Quantum.Simulation.GeneratorSystem));
```

