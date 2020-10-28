---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorSystem
title: MultiplyGeneratorSystem 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorSystem
qsharp.summary: Multiplies the coefficient of all terms in a `GeneratorSystem`.
ms.openlocfilehash: 1d28de99dab3f7aca4bf3706fe98f5ef7c5286a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720236"
---
# <a name="multiplygeneratorsystem-function"></a><span data-ttu-id="7c0a9-102">MultiplyGeneratorSystem 함수</span><span class="sxs-lookup"><span data-stu-id="7c0a9-102">MultiplyGeneratorSystem function</span></span>

<span data-ttu-id="7c0a9-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="7c0a9-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="7c0a9-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7c0a9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7c0a9-105">에 있는 모든 용어의 계수를 곱합니다 `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="7c0a9-105">Multiplies the coefficient of all terms in a `GeneratorSystem`.</span></span>

```qsharp
function MultiplyGeneratorSystem (multiplier : Double, generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="7c0a9-106">입력</span><span class="sxs-lookup"><span data-stu-id="7c0a9-106">Input</span></span>

### <a name="multiplier--double"></a><span data-ttu-id="7c0a9-107">승수: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7c0a9-107">multiplier : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7c0a9-108">계수의 승수입니다.</span><span class="sxs-lookup"><span data-stu-id="7c0a9-108">The multiplier on the coefficient.</span></span>


### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="7c0a9-109">generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="7c0a9-109">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="7c0a9-110">곱할 `GeneratorSystem`입니다.</span><span class="sxs-lookup"><span data-stu-id="7c0a9-110">The `GeneratorSystem` to be multiplied.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="7c0a9-111">출력: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="7c0a9-111">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="7c0a9-112">계수 `GeneratorSystem` 가 더 큰 시스템을 나타내는 `multiplier` 입니다.</span><span class="sxs-lookup"><span data-stu-id="7c0a9-112">A `GeneratorSystem` representing a system with coefficients a factor `multiplier` larger.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c0a9-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="7c0a9-113">See Also</span></span>

- [<span data-ttu-id="7c0a9-114">GeneratorSystem.</span><span class="sxs-lookup"><span data-stu-id="7c0a9-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)