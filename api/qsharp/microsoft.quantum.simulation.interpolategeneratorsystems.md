---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystems
title: InterpolateGeneratorSystems 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystems
qsharp.summary: Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.
ms.openlocfilehash: ee47637996313fe1b77c76f00b08417dac956247
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230585"
---
# <a name="interpolategeneratorsystems-function"></a><span data-ttu-id="97c17-102">InterpolateGeneratorSystems 함수</span><span class="sxs-lookup"><span data-stu-id="97c17-102">InterpolateGeneratorSystems function</span></span>

<span data-ttu-id="97c17-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="97c17-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="97c17-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="97c17-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="97c17-105">`TimeDependentGeneratorSystem`두의 선형 보간을 나타내는을 반환 합니다 `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="97c17-105">Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.</span></span>

```qsharp
function InterpolateGeneratorSystems (generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
```


## <a name="input"></a><span data-ttu-id="97c17-106">입력</span><span class="sxs-lookup"><span data-stu-id="97c17-106">Input</span></span>

### <a name="generatorsystemstart--generatorsystem"></a><span data-ttu-id="97c17-107">generatorSystemStart: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="97c17-107">generatorSystemStart : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="97c17-108">시작 `GeneratorSystem` 입니다.</span><span class="sxs-lookup"><span data-stu-id="97c17-108">The start `GeneratorSystem`.</span></span>


### <a name="generatorsystemend--generatorsystem"></a><span data-ttu-id="97c17-109">generatorSystemEnd: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="97c17-109">generatorSystemEnd : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="97c17-110">끝 `GeneratorSystem` 입니다.</span><span class="sxs-lookup"><span data-stu-id="97c17-110">The end `GeneratorSystem`.</span></span>



## <a name="output--timedependentgeneratorsystem"></a><span data-ttu-id="97c17-111">출력: [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="97c17-111">Output : [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span></span>

<span data-ttu-id="97c17-112">`TimeDependentGeneratorSystem`가중치 $ (1-s) $ on `generatorSystemStart` 과 가중치 $s $ on으로 입력 생성기 시스템의 합계인 시스템을 나타내는 `generatorSystemEnd` 입니다.</span><span class="sxs-lookup"><span data-stu-id="97c17-112">A `TimeDependentGeneratorSystem` representing a system that is the sum of the input generator systems, with weight $(1-s)$ on `generatorSystemStart` and weight $s$ on `generatorSystemEnd`.</span></span>

## <a name="see-also"></a><span data-ttu-id="97c17-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="97c17-113">See Also</span></span>

- [<span data-ttu-id="97c17-114">GeneratorSystem.</span><span class="sxs-lookup"><span data-stu-id="97c17-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
- [<span data-ttu-id="97c17-115">TimeDependentGeneratorSystem.</span><span class="sxs-lookup"><span data-stu-id="97c17-115">Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)