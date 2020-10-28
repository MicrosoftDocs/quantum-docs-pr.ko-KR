---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystems
title: InterpolateGeneratorSystems 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystems
qsharp.summary: Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.
ms.openlocfilehash: 9881c27577023dafff0bfc6d961877db44fec0eb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710564"
---
# <a name="interpolategeneratorsystems-function"></a><span data-ttu-id="8de12-102">InterpolateGeneratorSystems 함수</span><span class="sxs-lookup"><span data-stu-id="8de12-102">InterpolateGeneratorSystems function</span></span>

<span data-ttu-id="8de12-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="8de12-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="8de12-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8de12-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8de12-105">`TimeDependentGeneratorSystem`두의 선형 보간을 나타내는을 반환 합니다 `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="8de12-105">Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.</span></span>

```qsharp
function InterpolateGeneratorSystems (generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
```


## <a name="input"></a><span data-ttu-id="8de12-106">입력</span><span class="sxs-lookup"><span data-stu-id="8de12-106">Input</span></span>

### <a name="generatorsystemstart--generatorsystem"></a><span data-ttu-id="8de12-107">generatorSystemStart: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="8de12-107">generatorSystemStart : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="8de12-108">시작 `GeneratorSystem` 입니다.</span><span class="sxs-lookup"><span data-stu-id="8de12-108">The start `GeneratorSystem`.</span></span>


### <a name="generatorsystemend--generatorsystem"></a><span data-ttu-id="8de12-109">generatorSystemEnd: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="8de12-109">generatorSystemEnd : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="8de12-110">끝 `GeneratorSystem` 입니다.</span><span class="sxs-lookup"><span data-stu-id="8de12-110">The end `GeneratorSystem`.</span></span>



## <a name="output--timedependentgeneratorsystem"></a><span data-ttu-id="8de12-111">출력: [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="8de12-111">Output : [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span></span>

<span data-ttu-id="8de12-112">`TimeDependentGeneratorSystem`가중치 $ (1-s) $ on `generatorSystemStart` 과 가중치 $s $ on으로 입력 생성기 시스템의 합계인 시스템을 나타내는 `generatorSystemEnd` 입니다.</span><span class="sxs-lookup"><span data-stu-id="8de12-112">A `TimeDependentGeneratorSystem` representing a system that is the sum of the input generator systems, with weight $(1-s)$ on `generatorSystemStart` and weight $s$ on `generatorSystemEnd`.</span></span>

## <a name="see-also"></a><span data-ttu-id="8de12-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="8de12-113">See Also</span></span>

- [<span data-ttu-id="8de12-114">GeneratorSystem.</span><span class="sxs-lookup"><span data-stu-id="8de12-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
- [<span data-ttu-id="8de12-115">TimeDependentGeneratorSystem.</span><span class="sxs-lookup"><span data-stu-id="8de12-115">Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)