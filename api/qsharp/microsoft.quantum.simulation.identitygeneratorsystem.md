---
uid: Microsoft.Quantum.Simulation.IdentityGeneratorSystem
title: IdentityGeneratorSystem 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityGeneratorSystem
qsharp.summary: Returns a generator system consistent with the zero Hamiltonian `H = 0`, which corresponds to the identity evolution operation.
ms.openlocfilehash: 6602087cf7fa173a28fc5894f39ec02a67802427
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858130"
---
# <a name="identitygeneratorsystem-function"></a><span data-ttu-id="c2527-102">IdentityGeneratorSystem 함수</span><span class="sxs-lookup"><span data-stu-id="c2527-102">IdentityGeneratorSystem function</span></span>

<span data-ttu-id="c2527-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="c2527-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="c2527-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c2527-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c2527-105">Id 진화 작업에 해당 하는 0 Hamiltonian 일치 하는 생성기 시스템을 반환 합니다 `H = 0` .</span><span class="sxs-lookup"><span data-stu-id="c2527-105">Returns a generator system consistent with the zero Hamiltonian `H = 0`, which corresponds to the identity evolution operation.</span></span>

```qsharp
function IdentityGeneratorSystem () : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="output--generatorsystem"></a><span data-ttu-id="c2527-106">출력: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="c2527-106">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="c2527-107">Hamiltonian $H = $0의 진화를 나타내는 생성기 시스템입니다.</span><span class="sxs-lookup"><span data-stu-id="c2527-107">A generator system representing evolution under the Hamiltonian $H = 0$.</span></span>