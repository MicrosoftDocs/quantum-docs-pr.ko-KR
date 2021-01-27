---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: DeterministicStateOracleFromStateOracle 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: af545a7d6e82e654ee36ab3ba77c8f8be3384b96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854550"
---
# <a name="deterministicstateoraclefromstateoracle-function"></a><span data-ttu-id="6dad7-102">DeterministicStateOracleFromStateOracle 함수</span><span class="sxs-lookup"><span data-stu-id="6dad7-102">DeterministicStateOracleFromStateOracle function</span></span>

<span data-ttu-id="6dad7-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="6dad7-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="6dad7-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6dad7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6dad7-105">형식의 oracle `StateOracle` 을로 변환 `DeterministicStateOracle` 합니다.</span><span class="sxs-lookup"><span data-stu-id="6dad7-105">Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.</span></span>

```qsharp
function DeterministicStateOracleFromStateOracle (idxFlagQubit : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle) : Microsoft.Quantum.Oracles.DeterministicStateOracle
```


## <a name="input"></a><span data-ttu-id="6dad7-106">입력</span><span class="sxs-lookup"><span data-stu-id="6dad7-106">Input</span></span>

### <a name="idxflagqubit--int"></a><span data-ttu-id="6dad7-107">Idx플래그 [](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6dad7-107">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6dad7-108">`stateOracle`두 레지스터에 대해 명시적으로 동작 하는 $A $의 플래그의 인덱스입니다. 플래그 $f $와 system $s $ (예: $A \ket {0} \_ f\ket {\ psi} \_ s $)입니다.</span><span class="sxs-lookup"><span data-stu-id="6dad7-108">The index to the flag qubit of the `stateOracle` $A$, which explicitly acts on two registers: the flag $f$ and the system $s$, e.g. $A\ket{0}\_f\ket{\psi}\_s$.</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="6dad7-109">stateOracle: [Stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="6dad7-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="6dad7-110">형식의 상태 준비 oracle $A `StateOracle` 입니다.</span><span class="sxs-lookup"><span data-stu-id="6dad7-110">A state preparation oracle $A$ of type `StateOracle`.</span></span>



## <a name="output--deterministicstateoracle"></a><span data-ttu-id="6dad7-111">출력: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="6dad7-111">Output : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="6dad7-112">Oracle $A $와 같은 상태를 준비 하지만, 이제는 `DeterministicStateOracle` $a, s $는 더 이상 명시적으로 구분 되지 않습니다. 예를 들어  $A \ket{0\psi} \_ {as} $입니다.</span><span class="sxs-lookup"><span data-stu-id="6dad7-112">The same state preparation oracle $A$, but now of type `DeterministicStateOracle`, so it acts on a register where $a,s$ no longer explicitly separate, e.g.  $A\ket{0\psi}\_{as}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="6dad7-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6dad7-113">See Also</span></span>

- [<span data-ttu-id="6dad7-114">Oracles. StateOracle</span><span class="sxs-lookup"><span data-stu-id="6dad7-114">Microsoft.Quantum.Oracles.StateOracle</span></span>](xref:Microsoft.Quantum.Oracles.StateOracle)
- [<span data-ttu-id="6dad7-115">Oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="6dad7-115">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)