---
uid: Microsoft.Quantum.Simulation.GetGeneratorSystemFunction
title: GetGeneratorSystemFunction 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GetGeneratorSystemFunction
qsharp.summary: Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.
ms.openlocfilehash: 28e3c12d0ae0b08fc368c25eeb6f38d2834ca912
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229310"
---
# <a name="getgeneratorsystemfunction-function"></a><span data-ttu-id="780cc-102">GetGeneratorSystemFunction 함수</span><span class="sxs-lookup"><span data-stu-id="780cc-102">GetGeneratorSystemFunction function</span></span>

<span data-ttu-id="780cc-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="780cc-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="780cc-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="780cc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="780cc-105">`GeneratorIndex`에서 함수를 검색 `GeneratorSystem` 합니다.</span><span class="sxs-lookup"><span data-stu-id="780cc-105">Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.</span></span>

```qsharp
function GetGeneratorSystemFunction (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)
```


## <a name="input"></a><span data-ttu-id="780cc-106">입력</span><span class="sxs-lookup"><span data-stu-id="780cc-106">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="780cc-107">generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="780cc-107">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="780cc-108">해당 `GeneratorSystem`입니다.</span><span class="sxs-lookup"><span data-stu-id="780cc-108">The `GeneratorSystem` of interest.</span></span>



## <a name="output--int---generatorindex"></a><span data-ttu-id="780cc-109">출력: [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="780cc-109">Output : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="780cc-110">Hamiltonian의 각 용어를 인덱싱하는 함수입니다 `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="780cc-110">An function that indexes each `GeneratorIndex` term in a Hamiltonian.</span></span>

## <a name="see-also"></a><span data-ttu-id="780cc-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="780cc-111">See Also</span></span>

- [<span data-ttu-id="780cc-112">GeneratorIndex.</span><span class="sxs-lookup"><span data-stu-id="780cc-112">Microsoft.Quantum.Simulation.GeneratorIndex</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorIndex)
- [<span data-ttu-id="780cc-113">GeneratorSystem.</span><span class="sxs-lookup"><span data-stu-id="780cc-113">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)