---
uid: Microsoft.Quantum.Oracles.ReflectionOracleFromDeterministicStateOracle
title: ReflectionOracleFromDeterministicStateOracle 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracleFromDeterministicStateOracle
qsharp.summary: Constructs reflection about a given state from an oracle.
ms.openlocfilehash: 09de63d615a4d80e2b59deeddc07567aefe7660e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193831"
---
# <a name="reflectionoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="ca330-102">ReflectionOracleFromDeterministicStateOracle 함수</span><span class="sxs-lookup"><span data-stu-id="ca330-102">ReflectionOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="ca330-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="ca330-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="ca330-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ca330-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ca330-105">Oracle에서 지정 된 상태에 대 한 리플렉션을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca330-105">Constructs reflection about a given state from an oracle.</span></span>

```qsharp
function ReflectionOracleFromDeterministicStateOracle (oracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="description"></a><span data-ttu-id="ca330-106">Description</span><span class="sxs-lookup"><span data-stu-id="ca330-106">Description</span></span>

<span data-ttu-id="ca330-107">단일 행렬 $O $로 표시 되는 결정적 상태 준비를 고려 하 여이 함수의 결과는 oracle $O $에서 준비한 상태 $ \ket{\psi} $에 대 한 반사를 적용 하는 oracle입니다. 즉, $ \ket{\psi} $ 상태를 $O \ket {0} = \ket{\psi} $입니다.</span><span class="sxs-lookup"><span data-stu-id="ca330-107">Given a deterministic state preparation oracle represented by a unitary matrix $O$, the result of this function is an oracle that applies a reflection around the state $\ket{\psi}$ prepared by the oracle $O$; that is, the state $\ket{\psi}$ such that $O\ket{0} = \ket{\psi}$.</span></span>

## <a name="input"></a><span data-ttu-id="ca330-108">입력</span><span class="sxs-lookup"><span data-stu-id="ca330-108">Input</span></span>

### <a name="oracle--deterministicstateoracle"></a><span data-ttu-id="ca330-109">oracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="ca330-109">oracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="ca330-110">$ \Ket{\psi} $ 상태의 복사본을 준비 하는 oracle입니다.</span><span class="sxs-lookup"><span data-stu-id="ca330-110">An oracle that prepares copies of the state $\ket{\psi}$.</span></span>



## <a name="output--reflectionoracle"></a><span data-ttu-id="ca330-111">출력: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="ca330-111">Output : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="ca330-112">$ \Ket{\psi} $ 상태에 대 한 정보를 반영 하는 oracle입니다.</span><span class="sxs-lookup"><span data-stu-id="ca330-112">An oracle that reflects about the state $\ket{\psi}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca330-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ca330-113">See Also</span></span>

- [<span data-ttu-id="ca330-114">Oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="ca330-114">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="ca330-115">Oracles. ReflectionOracle</span><span class="sxs-lookup"><span data-stu-id="ca330-115">Microsoft.Quantum.Oracles.ReflectionOracle</span></span>](xref:Microsoft.Quantum.Oracles.ReflectionOracle)