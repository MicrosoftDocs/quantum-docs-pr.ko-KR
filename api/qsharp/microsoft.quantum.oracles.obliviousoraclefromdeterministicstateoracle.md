---
uid: Microsoft.Quantum.Oracles.ObliviousOracleFromDeterministicStateOracle
title: ObliviousOracleFromDeterministicStateOracle 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracleFromDeterministicStateOracle
qsharp.summary: Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.
ms.openlocfilehash: c7aa80feda67d68216f318073ee8c6a5eb0653c0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854520"
---
# <a name="obliviousoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="94e71-102">ObliviousOracleFromDeterministicStateOracle 함수</span><span class="sxs-lookup"><span data-stu-id="94e71-102">ObliviousOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="94e71-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="94e71-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="94e71-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="94e71-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="94e71-105">Oracles와를 결합 합니다 `DeterministicStateOracle` `ObliviousOracle` .</span><span class="sxs-lookup"><span data-stu-id="94e71-105">Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.</span></span>

```qsharp
function ObliviousOracleFromDeterministicStateOracle (ancillaOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle) : Microsoft.Quantum.Oracles.ObliviousOracle
```


## <a name="input"></a><span data-ttu-id="94e71-106">입력</span><span class="sxs-lookup"><span data-stu-id="94e71-106">Input</span></span>

### <a name="ancillaoracle--deterministicstateoracle"></a><span data-ttu-id="94e71-107">[DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle) Illaoracle:</span><span class="sxs-lookup"><span data-stu-id="94e71-107">ancillaOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="94e71-108">등록 $a $에서 동작 하는 형식의 상태 준비 oracle $A $ `DeterministicStateOracle` .</span><span class="sxs-lookup"><span data-stu-id="94e71-108">A state preparation oracle $A$ of type `DeterministicStateOracle` acting on register $a$.</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="94e71-109">signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="94e71-109">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="94e71-110">`ObliviousOracle`Register $a, s $에 대해 공동으로 동작 하는 유형의 oracle $U $입니다.</span><span class="sxs-lookup"><span data-stu-id="94e71-110">A oracle $U$ of type `ObliviousOracle` acting jointly on register $a,s$.</span></span>



## <a name="output--obliviousoracle"></a><span data-ttu-id="94e71-111">출력: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="94e71-111">Output : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="94e71-112">유형의 oracle $O = UA $ `ObliviousOracle` 입니다.</span><span class="sxs-lookup"><span data-stu-id="94e71-112">An oracle $O=UA$ of type `ObliviousOracle`.</span></span>

## <a name="see-also"></a><span data-ttu-id="94e71-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="94e71-113">See Also</span></span>

- [<span data-ttu-id="94e71-114">Oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="94e71-114">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="94e71-115">Oracles. ObliviousOracle</span><span class="sxs-lookup"><span data-stu-id="94e71-115">Microsoft.Quantum.Oracles.ObliviousOracle</span></span>](xref:Microsoft.Quantum.Oracles.ObliviousOracle)