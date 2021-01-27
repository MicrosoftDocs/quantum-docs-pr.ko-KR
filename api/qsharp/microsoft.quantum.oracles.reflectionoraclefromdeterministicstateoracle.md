---
uid: Microsoft.Quantum.Oracles.ReflectionOracleFromDeterministicStateOracle
title: ReflectionOracleFromDeterministicStateOracle 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracleFromDeterministicStateOracle
qsharp.summary: Constructs reflection about a given state from an oracle.
ms.openlocfilehash: c260bdbcdb2ce53ad602bf84e0d31ef4fec24a79
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842518"
---
# <a name="reflectionoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="15c42-102">ReflectionOracleFromDeterministicStateOracle 함수</span><span class="sxs-lookup"><span data-stu-id="15c42-102">ReflectionOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="15c42-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="15c42-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="15c42-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="15c42-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="15c42-105">Oracle에서 지정 된 상태에 대 한 리플렉션을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15c42-105">Constructs reflection about a given state from an oracle.</span></span>

```qsharp
function ReflectionOracleFromDeterministicStateOracle (oracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="description"></a><span data-ttu-id="15c42-106">설명</span><span class="sxs-lookup"><span data-stu-id="15c42-106">Description</span></span>

<span data-ttu-id="15c42-107">단일 행렬 $O $로 표시 되는 결정적 상태 준비를 고려 하 여이 함수의 결과는 oracle $O $에서 준비한 상태 $ \ket{\psi} $에 대 한 반사를 적용 하는 oracle입니다. 즉, $ \ket{\psi} $ 상태를 $O \ket {0} = \ket{\psi} $입니다.</span><span class="sxs-lookup"><span data-stu-id="15c42-107">Given a deterministic state preparation oracle represented by a unitary matrix $O$, the result of this function is an oracle that applies a reflection around the state $\ket{\psi}$ prepared by the oracle $O$; that is, the state $\ket{\psi}$ such that $O\ket{0} = \ket{\psi}$.</span></span>

## <a name="input"></a><span data-ttu-id="15c42-108">입력</span><span class="sxs-lookup"><span data-stu-id="15c42-108">Input</span></span>

### <a name="oracle--deterministicstateoracle"></a><span data-ttu-id="15c42-109">oracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="15c42-109">oracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="15c42-110">$ \Ket{\psi} $ 상태의 복사본을 준비 하는 oracle입니다.</span><span class="sxs-lookup"><span data-stu-id="15c42-110">An oracle that prepares copies of the state $\ket{\psi}$.</span></span>



## <a name="output--reflectionoracle"></a><span data-ttu-id="15c42-111">출력: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="15c42-111">Output : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="15c42-112">$ \Ket{\psi} $ 상태에 대 한 정보를 반영 하는 oracle입니다.</span><span class="sxs-lookup"><span data-stu-id="15c42-112">An oracle that reflects about the state $\ket{\psi}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="15c42-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="15c42-113">See Also</span></span>

- [<span data-ttu-id="15c42-114">Oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="15c42-114">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="15c42-115">Oracles. ReflectionOracle</span><span class="sxs-lookup"><span data-stu-id="15c42-115">Microsoft.Quantum.Oracles.ReflectionOracle</span></span>](xref:Microsoft.Quantum.Oracles.ReflectionOracle)