---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: DeterministicStateOracleFromStateOracle 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: 183b1108ead6239e26bb0b38144cb9374e7bf285
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226760"
---
# <a name="deterministicstateoraclefromstateoracle-function"></a><span data-ttu-id="540cc-102">DeterministicStateOracleFromStateOracle 함수</span><span class="sxs-lookup"><span data-stu-id="540cc-102">DeterministicStateOracleFromStateOracle function</span></span>

<span data-ttu-id="540cc-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="540cc-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="540cc-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="540cc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="540cc-105">형식의 oracle `StateOracle` 을로 변환 `DeterministicStateOracle` 합니다.</span><span class="sxs-lookup"><span data-stu-id="540cc-105">Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.</span></span>

```qsharp
function DeterministicStateOracleFromStateOracle (idxFlagQubit : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle) : Microsoft.Quantum.Oracles.DeterministicStateOracle
```


## <a name="input"></a><span data-ttu-id="540cc-106">입력</span><span class="sxs-lookup"><span data-stu-id="540cc-106">Input</span></span>

### <a name="idxflagqubit--int"></a><span data-ttu-id="540cc-107">Idx플래그 [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="540cc-107">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="540cc-108">`stateOracle`두 레지스터에 대해 명시적으로 동작 하는 $A $의 플래그의 인덱스입니다. 플래그 $f $와 system $s $ (예: $A \ket {0} \_ f\ket {\ psi} \_ s $)입니다.</span><span class="sxs-lookup"><span data-stu-id="540cc-108">The index to the flag qubit of the `stateOracle` $A$, which explicitly acts on two registers: the flag $f$ and the system $s$, e.g. $A\ket{0}\_f\ket{\psi}\_s$.</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="540cc-109">stateOracle: [Stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="540cc-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="540cc-110">형식의 상태 준비 oracle $A `StateOracle` 입니다.</span><span class="sxs-lookup"><span data-stu-id="540cc-110">A state preparation oracle $A$ of type `StateOracle`.</span></span>



## <a name="output--deterministicstateoracle"></a><span data-ttu-id="540cc-111">출력: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="540cc-111">Output : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="540cc-112">Oracle $A $와 같은 상태를 준비 하지만, 이제는 `DeterministicStateOracle` $a, s $는 더 이상 명시적으로 구분 되지 않습니다. 예를 들어  $A \ket{0\psi} \_ {as} $입니다.</span><span class="sxs-lookup"><span data-stu-id="540cc-112">The same state preparation oracle $A$, but now of type `DeterministicStateOracle`, so it acts on a register where $a,s$ no longer explicitly separate, e.g.  $A\ket{0\psi}\_{as}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="540cc-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="540cc-113">See Also</span></span>

- [<span data-ttu-id="540cc-114">Oracles. StateOracle</span><span class="sxs-lookup"><span data-stu-id="540cc-114">Microsoft.Quantum.Oracles.StateOracle</span></span>](xref:Microsoft.Quantum.Oracles.StateOracle)
- [<span data-ttu-id="540cc-115">Oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="540cc-115">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)