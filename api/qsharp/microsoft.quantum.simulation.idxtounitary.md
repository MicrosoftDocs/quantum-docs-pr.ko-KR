---
uid: Microsoft.Quantum.Simulation.IdxToUnitary
title: IdxToUnitary 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdxToUnitary
qsharp.summary: Used in implementation of `PauliBlockEncoding`
ms.openlocfilehash: a142d8a5af56a43de6341e3c0bdc77f50030f06e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710599"
---
# <a name="idxtounitary-function"></a><span data-ttu-id="e454b-102">IdxToUnitary 함수</span><span class="sxs-lookup"><span data-stu-id="e454b-102">IdxToUnitary function</span></span>

<span data-ttu-id="e454b-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="e454b-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="e454b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e454b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e454b-105">구현에 사용 됨 `PauliBlockEncoding`</span><span class="sxs-lookup"><span data-stu-id="e454b-105">Used in implementation of `PauliBlockEncoding`</span></span>

```qsharp
function IdxToUnitary (idx : Int, genFun : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex), genIdxToUnitary : (Microsoft.Quantum.Simulation.GeneratorIndex -> (Qubit[] => Unit is Adj + Ctl))) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="e454b-106">입력</span><span class="sxs-lookup"><span data-stu-id="e454b-106">Input</span></span>

### <a name="idx--int"></a><span data-ttu-id="e454b-107">idx: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e454b-107">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="genfun--int---generatorindex"></a><span data-ttu-id="e454b-108">genfun: [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="e454b-108">genFun : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>




### <a name="genidxtounitary--generatorindex---qubit--unit-adj--ctl"></a><span data-ttu-id="e454b-109">genidxtounitary: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex) -> [robit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="e454b-109">genIdxToUnitary : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>





## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="e454b-110">출력: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="e454b-110">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>



## <a name="see-also"></a><span data-ttu-id="e454b-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e454b-111">See Also</span></span>

- [<span data-ttu-id="e454b-112">PauliBlockEncoding.</span><span class="sxs-lookup"><span data-stu-id="e454b-112">Microsoft.Quantum.Simulation.PauliBlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.PauliBlockEncoding)