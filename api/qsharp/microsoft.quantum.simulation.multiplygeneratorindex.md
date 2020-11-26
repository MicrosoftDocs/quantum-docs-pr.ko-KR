---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorIndex
title: MultiplyGeneratorIndex 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorIndex
qsharp.summary: Multiplies the coefficient in a `GeneratorIndex`.
ms.openlocfilehash: dc2bd02c40b53eca726f70578e3c5918add8f1bb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230449"
---
# <a name="multiplygeneratorindex-function"></a><span data-ttu-id="c4458-102">MultiplyGeneratorIndex 함수</span><span class="sxs-lookup"><span data-stu-id="c4458-102">MultiplyGeneratorIndex function</span></span>

<span data-ttu-id="c4458-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="c4458-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="c4458-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c4458-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c4458-105">에 계수를 곱합니다 `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="c4458-105">Multiplies the coefficient in a `GeneratorIndex`.</span></span>

```qsharp
function MultiplyGeneratorIndex (multiplier : Double, generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="c4458-106">입력</span><span class="sxs-lookup"><span data-stu-id="c4458-106">Input</span></span>

### <a name="multiplier--double"></a><span data-ttu-id="c4458-107">승수: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c4458-107">multiplier : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c4458-108">계수의 승수입니다.</span><span class="sxs-lookup"><span data-stu-id="c4458-108">The multiplier on the coefficient.</span></span>


### <a name="generatorindex--generatorindex"></a><span data-ttu-id="c4458-109">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="c4458-109">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="c4458-110">곱할 `GeneratorIndex`입니다.</span><span class="sxs-lookup"><span data-stu-id="c4458-110">The `GeneratorIndex` to be multiplied.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="c4458-111">출력: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="c4458-111">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="c4458-112">`GeneratorIndex`계수가 계수 보다 큰 용어를 나타내는 `multiplier` 입니다.</span><span class="sxs-lookup"><span data-stu-id="c4458-112">A `GeneratorIndex` representing a term with coefficient a factor `multiplier` larger.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4458-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c4458-113">See Also</span></span>

- [<span data-ttu-id="c4458-114">GeneratorIndex.</span><span class="sxs-lookup"><span data-stu-id="c4458-114">Microsoft.Quantum.Simulation.GeneratorIndex</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorIndex)