---
uid: Microsoft.Quantum.Simulation.Unitary
title: 단일 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: Unitary
qsharp.summary: Represents evolution under a unitary operator.
ms.openlocfilehash: d2bba42e80132d0879f42922f28ad50bef54edf3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725331"
---
# <a name="unitary-user-defined-type"></a><span data-ttu-id="5d9b7-102">단일 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="5d9b7-102">Unitary user defined type</span></span>

<span data-ttu-id="5d9b7-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="5d9b7-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="5d9b7-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5d9b7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5d9b7-105">단일 연산자의 진화를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5d9b7-105">Represents evolution under a unitary operator.</span></span>

```qsharp

newtype Unitary = ((Qubit[] => Unit is Adj + Ctl));
```

