---
uid: Microsoft.Quantum.Oracles.ObliviousOracleFromDeterministicStateOracle
title: ObliviousOracleFromDeterministicStateOracle 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracleFromDeterministicStateOracle
qsharp.summary: Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.
ms.openlocfilehash: 9e18776ad4d6adf0068213117c6d1d8ed5c5f126
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722223"
---
# <a name="obliviousoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="28137-102">ObliviousOracleFromDeterministicStateOracle 함수</span><span class="sxs-lookup"><span data-stu-id="28137-102">ObliviousOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="28137-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="28137-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="28137-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="28137-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="28137-105">Oracles와를 결합 합니다 `DeterministicStateOracle` `ObliviousOracle` .</span><span class="sxs-lookup"><span data-stu-id="28137-105">Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.</span></span>

```qsharp
function ObliviousOracleFromDeterministicStateOracle (ancillaOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle) : Microsoft.Quantum.Oracles.ObliviousOracle
```


## <a name="input"></a><span data-ttu-id="28137-106">입력</span><span class="sxs-lookup"><span data-stu-id="28137-106">Input</span></span>

### <a name="ancillaoracle--deterministicstateoracle"></a><span data-ttu-id="28137-107">[DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle) Illaoracle:</span><span class="sxs-lookup"><span data-stu-id="28137-107">ancillaOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="28137-108">등록 $a $에서 동작 하는 형식의 상태 준비 oracle $A $ `DeterministicStateOracle` .</span><span class="sxs-lookup"><span data-stu-id="28137-108">A state preparation oracle $A$ of type `DeterministicStateOracle` acting on register $a$.</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="28137-109">signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="28137-109">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="28137-110">`ObliviousOracle`Register $a, s $에 대해 공동으로 동작 하는 유형의 oracle $U $입니다.</span><span class="sxs-lookup"><span data-stu-id="28137-110">A oracle $U$ of type `ObliviousOracle` acting jointly on register $a,s$.</span></span>



## <a name="output--obliviousoracle"></a><span data-ttu-id="28137-111">출력: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="28137-111">Output : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="28137-112">유형의 oracle $O = UA $ `ObliviousOracle` 입니다.</span><span class="sxs-lookup"><span data-stu-id="28137-112">An oracle $O=UA$ of type `ObliviousOracle`.</span></span>

## <a name="see-also"></a><span data-ttu-id="28137-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="28137-113">See Also</span></span>

- [<span data-ttu-id="28137-114">Oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="28137-114">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="28137-115">Oracles. ObliviousOracle</span><span class="sxs-lookup"><span data-stu-id="28137-115">Microsoft.Quantum.Oracles.ObliviousOracle</span></span>](xref:Microsoft.Quantum.Oracles.ObliviousOracle)