---
uid: Microsoft.Quantum.Simulation.AddGeneratorSystems
title: AddGeneratorSystems 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: AddGeneratorSystems
qsharp.summary: Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.
ms.openlocfilehash: d6e8f7085cf0558960d055dbeeb08740c3fab049
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229667"
---
# <a name="addgeneratorsystems-function"></a><span data-ttu-id="f0ee1-102">AddGeneratorSystems 함수</span><span class="sxs-lookup"><span data-stu-id="f0ee1-102">AddGeneratorSystems function</span></span>

<span data-ttu-id="f0ee1-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="f0ee1-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="f0ee1-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f0ee1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f0ee1-105">새를 `GeneratorSystem` 만드는 두 개의를 추가 `GeneratorSystem` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0ee1-105">Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.</span></span>

```qsharp
function AddGeneratorSystems (generatorSystemA : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemB : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="f0ee1-106">입력</span><span class="sxs-lookup"><span data-stu-id="f0ee1-106">Input</span></span>

### <a name="generatorsystema--generatorsystem"></a><span data-ttu-id="f0ee1-107">generatorSystemA: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="f0ee1-107">generatorSystemA : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="f0ee1-108">첫 번째 `GeneratorSystem`입니다.</span><span class="sxs-lookup"><span data-stu-id="f0ee1-108">The first `GeneratorSystem`.</span></span>


### <a name="generatorsystemb--generatorsystem"></a><span data-ttu-id="f0ee1-109">generatorSystemB: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="f0ee1-109">generatorSystemB : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="f0ee1-110">두 번째 `GeneratorSystem`입니다.</span><span class="sxs-lookup"><span data-stu-id="f0ee1-110">The second `GeneratorSystem`.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="f0ee1-111">출력: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="f0ee1-111">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="f0ee1-112">`GeneratorSystem`입력 생성기 시스템의 합계인 시스템을 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="f0ee1-112">A `GeneratorSystem` representing a system that is the sum of the input generator systems.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0ee1-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f0ee1-113">See Also</span></span>

- [<span data-ttu-id="f0ee1-114">GeneratorSystem.</span><span class="sxs-lookup"><span data-stu-id="f0ee1-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)