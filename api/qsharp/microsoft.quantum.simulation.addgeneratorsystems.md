---
uid: Microsoft.Quantum.Simulation.AddGeneratorSystems
title: AddGeneratorSystems 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: AddGeneratorSystems
qsharp.summary: Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.
ms.openlocfilehash: 494037aa7635cccf25978bea9339ecc7aee75142
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710641"
---
# <a name="addgeneratorsystems-function"></a><span data-ttu-id="23fc0-102">AddGeneratorSystems 함수</span><span class="sxs-lookup"><span data-stu-id="23fc0-102">AddGeneratorSystems function</span></span>

<span data-ttu-id="23fc0-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="23fc0-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="23fc0-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="23fc0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="23fc0-105">새를 `GeneratorSystem` 만드는 두 개의를 추가 `GeneratorSystem` 합니다.</span><span class="sxs-lookup"><span data-stu-id="23fc0-105">Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.</span></span>

```qsharp
function AddGeneratorSystems (generatorSystemA : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemB : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="23fc0-106">입력</span><span class="sxs-lookup"><span data-stu-id="23fc0-106">Input</span></span>

### <a name="generatorsystema--generatorsystem"></a><span data-ttu-id="23fc0-107">generatorSystemA: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="23fc0-107">generatorSystemA : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="23fc0-108">첫 번째 `GeneratorSystem`입니다.</span><span class="sxs-lookup"><span data-stu-id="23fc0-108">The first `GeneratorSystem`.</span></span>


### <a name="generatorsystemb--generatorsystem"></a><span data-ttu-id="23fc0-109">generatorSystemB: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="23fc0-109">generatorSystemB : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="23fc0-110">두 번째 `GeneratorSystem`입니다.</span><span class="sxs-lookup"><span data-stu-id="23fc0-110">The second `GeneratorSystem`.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="23fc0-111">출력: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="23fc0-111">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="23fc0-112">`GeneratorSystem`입력 생성기 시스템의 합계인 시스템을 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="23fc0-112">A `GeneratorSystem` representing a system that is the sum of the input generator systems.</span></span>

## <a name="see-also"></a><span data-ttu-id="23fc0-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="23fc0-113">See Also</span></span>

- [<span data-ttu-id="23fc0-114">GeneratorSystem.</span><span class="sxs-lookup"><span data-stu-id="23fc0-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)