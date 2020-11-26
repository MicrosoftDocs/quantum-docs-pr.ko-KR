---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: ReflectionOracle 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 7bb0626e7cca9ae0b640699ea57f2e114bda2d06
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226658"
---
# <a name="reflectionoracle-user-defined-type"></a><span data-ttu-id="2308d-102">ReflectionOracle 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="2308d-102">ReflectionOracle user defined type</span></span>

<span data-ttu-id="2308d-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="2308d-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="2308d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2308d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2308d-105">리플렉션 oracle을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2308d-105">Represents a reflection oracle.</span></span>

<span data-ttu-id="2308d-106">리플렉션 oracle $O $에는 입력이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2308d-106">A reflection oracle, $O$, has inputs:</span></span>

- <span data-ttu-id="2308d-107">반사 된 하위 공간을 회전 하는 $ \\? $ 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="2308d-107">The phase $\phi$ by which to rotate the reflected subspace.</span></span>
- <span data-ttu-id="2308d-108">지정 된 리플렉션을 수행할 대상 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="2308d-108">The qubit register on which to perform the given reflection.</span></span>

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="2308d-109">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="2308d-109">Named Items</span></span>

### <a name="applyreflection--doublequbit--unit--is-adj--ctl"></a><span data-ttu-id="2308d-110">ApplyReflection: ([Double](xref:microsoft.quantum.lang-ref.double),[Adj](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  은 + Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="2308d-110">ApplyReflection : ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="2308d-111">설명</span><span class="sxs-lookup"><span data-stu-id="2308d-111">Remarks</span></span>

<span data-ttu-id="2308d-112">이 oracle $O = \boldone-(1-e ^ {i \phi}) \ket{\psi}\bra{\psi} $는 1 단계에서 단일 순수 상태 $ \ket{\psi} $에 대해 부분 반사를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2308d-112">This oracle $O = \boldone - (1 - e^{i \phi}) \ket{\psi}\bra{\psi}$ performs a partial reflection by a phase $\phi$ about a single pure state $\ket{\psi}$.</span></span>