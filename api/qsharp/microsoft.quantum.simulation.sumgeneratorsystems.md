---
uid: Microsoft.Quantum.Simulation.SumGeneratorSystems
title: SumGeneratorSystems 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SumGeneratorSystems
qsharp.summary: Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.
ms.openlocfilehash: 0e64d2b599c55c19711208670030fd01e09aff7e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851011"
---
# <a name="sumgeneratorsystems-function"></a><span data-ttu-id="befcb-102">SumGeneratorSystems 함수</span><span class="sxs-lookup"><span data-stu-id="befcb-102">SumGeneratorSystems function</span></span>

<span data-ttu-id="befcb-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="befcb-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="befcb-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="befcb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="befcb-105">`GeneratorSystem`새 GeneratorSystem을 만들려면를 여러 개 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="befcb-105">Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.</span></span>

```qsharp
function SumGeneratorSystems (generatorSystems : Microsoft.Quantum.Simulation.GeneratorSystem[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="befcb-106">입력</span><span class="sxs-lookup"><span data-stu-id="befcb-106">Input</span></span>

### <a name="generatorsystems--generatorsystem"></a><span data-ttu-id="befcb-107">generatorSystems: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)[]</span><span class="sxs-lookup"><span data-stu-id="befcb-107">generatorSystems : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)[]</span></span>

<span data-ttu-id="befcb-108">`GeneratorSystem[]` 형식의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="befcb-108">An array of type `GeneratorSystem[]`.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="befcb-109">출력: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="befcb-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="befcb-110">`GeneratorSystem`입력 생성기 시스템의 합계인 시스템을 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="befcb-110">A `GeneratorSystem` representing a system that is the sum of the input generator systems.</span></span>

## <a name="see-also"></a><span data-ttu-id="befcb-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="befcb-111">See Also</span></span>

- [<span data-ttu-id="befcb-112">GeneratorSystem.</span><span class="sxs-lookup"><span data-stu-id="befcb-112">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)