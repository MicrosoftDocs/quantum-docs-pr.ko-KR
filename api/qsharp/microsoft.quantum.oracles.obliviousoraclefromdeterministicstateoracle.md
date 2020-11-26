---
uid: Microsoft.Quantum.Oracles.ObliviousOracleFromDeterministicStateOracle
title: ObliviousOracleFromDeterministicStateOracle 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracleFromDeterministicStateOracle
qsharp.summary: Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.
ms.openlocfilehash: 8f1fe34e38edefba228fb9d01e1712e4c0916970
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226692"
---
# <a name="obliviousoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="fce16-102">ObliviousOracleFromDeterministicStateOracle 함수</span><span class="sxs-lookup"><span data-stu-id="fce16-102">ObliviousOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="fce16-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="fce16-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="fce16-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fce16-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fce16-105">Oracles와를 결합 합니다 `DeterministicStateOracle` `ObliviousOracle` .</span><span class="sxs-lookup"><span data-stu-id="fce16-105">Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.</span></span>

```qsharp
function ObliviousOracleFromDeterministicStateOracle (ancillaOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle) : Microsoft.Quantum.Oracles.ObliviousOracle
```


## <a name="input"></a><span data-ttu-id="fce16-106">입력</span><span class="sxs-lookup"><span data-stu-id="fce16-106">Input</span></span>

### <a name="ancillaoracle--deterministicstateoracle"></a><span data-ttu-id="fce16-107">[DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle) Illaoracle:</span><span class="sxs-lookup"><span data-stu-id="fce16-107">ancillaOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="fce16-108">등록 $a $에서 동작 하는 형식의 상태 준비 oracle $A $ `DeterministicStateOracle` .</span><span class="sxs-lookup"><span data-stu-id="fce16-108">A state preparation oracle $A$ of type `DeterministicStateOracle` acting on register $a$.</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="fce16-109">signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="fce16-109">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="fce16-110">`ObliviousOracle`Register $a, s $에 대해 공동으로 동작 하는 유형의 oracle $U $입니다.</span><span class="sxs-lookup"><span data-stu-id="fce16-110">A oracle $U$ of type `ObliviousOracle` acting jointly on register $a,s$.</span></span>



## <a name="output--obliviousoracle"></a><span data-ttu-id="fce16-111">출력: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="fce16-111">Output : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="fce16-112">유형의 oracle $O = UA $ `ObliviousOracle` 입니다.</span><span class="sxs-lookup"><span data-stu-id="fce16-112">An oracle $O=UA$ of type `ObliviousOracle`.</span></span>

## <a name="see-also"></a><span data-ttu-id="fce16-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="fce16-113">See Also</span></span>

- [<span data-ttu-id="fce16-114">Oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="fce16-114">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="fce16-115">Oracles. ObliviousOracle</span><span class="sxs-lookup"><span data-stu-id="fce16-115">Microsoft.Quantum.Oracles.ObliviousOracle</span></span>](xref:Microsoft.Quantum.Oracles.ObliviousOracle)