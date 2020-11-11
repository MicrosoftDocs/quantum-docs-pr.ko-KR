---
uid: Microsoft.Quantum.Oracles.StateOracleFromDeterministicStateOracle
title: StateOracleFromDeterministicStateOracle 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracleFromDeterministicStateOracle
qsharp.summary: Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.
ms.openlocfilehash: ccb083dbaaec2f306ba0740ef364ebb22408ed98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724218"
---
# <a name="stateoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="e70a2-102">StateOracleFromDeterministicStateOracle 함수</span><span class="sxs-lookup"><span data-stu-id="e70a2-102">StateOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="e70a2-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="e70a2-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="e70a2-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e70a2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e70a2-105">형식의 oracle `DeterministicStateOracle` 을로 변환 `StateOracle` 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70a2-105">Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.</span></span>

```qsharp
function StateOracleFromDeterministicStateOracle (deterministicStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.StateOracle
```


## <a name="input"></a><span data-ttu-id="e70a2-106">입력</span><span class="sxs-lookup"><span data-stu-id="e70a2-106">Input</span></span>

### <a name="deterministicstateoracle--deterministicstateoracle"></a><span data-ttu-id="e70a2-107">deterministicStateOracle: [deterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="e70a2-107">deterministicStateOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="e70a2-108">형식의 상태 준비 oracle $A `DeterministicStateOracle` 입니다.</span><span class="sxs-lookup"><span data-stu-id="e70a2-108">A state preparation oracle $A$ of type `DeterministicStateOracle`.</span></span>



## <a name="output--stateoracle"></a><span data-ttu-id="e70a2-109">출력: [Stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="e70a2-109">Output : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="e70a2-110">Oracle $A $와 같은 상태를 준비 하지만 이제는 형식 `StateOracle` 입니다.</span><span class="sxs-lookup"><span data-stu-id="e70a2-110">The same state preparation oracle $A$, but now of type `StateOracle`.</span></span> <span data-ttu-id="e70a2-111">이에서 플래그 인덱스는 `StateOracle` 더미 변수 이며 아무런 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e70a2-111">Note that the flag index in this `StateOracle` is a dummy variable and has no effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="e70a2-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e70a2-112">See Also</span></span>

- [<span data-ttu-id="e70a2-113">Oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="e70a2-113">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="e70a2-114">Oracles. StateOracle</span><span class="sxs-lookup"><span data-stu-id="e70a2-114">Microsoft.Quantum.Oracles.StateOracle</span></span>](xref:Microsoft.Quantum.Oracles.StateOracle)