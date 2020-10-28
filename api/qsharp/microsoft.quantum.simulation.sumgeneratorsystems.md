---
uid: Microsoft.Quantum.Simulation.SumGeneratorSystems
title: SumGeneratorSystems 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SumGeneratorSystems
qsharp.summary: Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.
ms.openlocfilehash: b667a6af313b5bb8950a34a6d0406976bde49311
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719881"
---
# <a name="sumgeneratorsystems-function"></a><span data-ttu-id="92114-102">SumGeneratorSystems 함수</span><span class="sxs-lookup"><span data-stu-id="92114-102">SumGeneratorSystems function</span></span>

<span data-ttu-id="92114-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="92114-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="92114-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="92114-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="92114-105">`GeneratorSystem`새 GeneratorSystem을 만들려면를 여러 개 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="92114-105">Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.</span></span>

```qsharp
function SumGeneratorSystems (generatorSystems : Microsoft.Quantum.Simulation.GeneratorSystem[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="92114-106">입력</span><span class="sxs-lookup"><span data-stu-id="92114-106">Input</span></span>

### <a name="generatorsystems--generatorsystem"></a><span data-ttu-id="92114-107">generatorSystems: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)[]</span><span class="sxs-lookup"><span data-stu-id="92114-107">generatorSystems : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)[]</span></span>

<span data-ttu-id="92114-108">`GeneratorSystem[]` 형식의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="92114-108">An array of type `GeneratorSystem[]`.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="92114-109">출력: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="92114-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="92114-110">`GeneratorSystem`입력 생성기 시스템의 합계인 시스템을 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="92114-110">A `GeneratorSystem` representing a system that is the sum of the input generator systems.</span></span>

## <a name="see-also"></a><span data-ttu-id="92114-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="92114-111">See Also</span></span>

- [<span data-ttu-id="92114-112">GeneratorSystem.</span><span class="sxs-lookup"><span data-stu-id="92114-112">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)