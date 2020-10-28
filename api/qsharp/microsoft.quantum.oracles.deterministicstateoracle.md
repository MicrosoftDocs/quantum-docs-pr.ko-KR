---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracle
title: DeterministicStateOracle 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracle
qsharp.summary: >-
  Represents an oracle for deterministic state preparation.

  The input to the oracle $O$ is:

  - The register that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: f02267d48cf42fb5b02782dc6b667ac7b60a05dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724295"
---
# <a name="deterministicstateoracle-user-defined-type"></a><span data-ttu-id="d13b0-102">DeterministicStateOracle 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="d13b0-102">DeterministicStateOracle user defined type</span></span>

<span data-ttu-id="d13b0-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="d13b0-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="d13b0-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d13b0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d13b0-105">결정적 상태 준비를 위한 oracle을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d13b0-105">Represents an oracle for deterministic state preparation.</span></span>

<span data-ttu-id="d13b0-106">Oracle $O $에 대 한 입력은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d13b0-106">The input to the oracle $O$ is:</span></span>

- <span data-ttu-id="d13b0-107">원하는 퀀텀 상태 $ \ket{\psi} s $를 저장할 레지스터입니다 \_ .</span><span class="sxs-lookup"><span data-stu-id="d13b0-107">The register that will store the desired quantum state $\ket{\psi}\_s$.</span></span>

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="d13b0-108">설명</span><span class="sxs-lookup"><span data-stu-id="d13b0-108">Remarks</span></span>

<span data-ttu-id="d13b0-109">$O \ket = \ket{\psi} $에서 정의한이 oracle {0} 은 {0} 상태 $ \ket{\psi} $를 만들기 위해 계산 기준 상태 $ \ket $에 대해 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="d13b0-109">This oracle defined by $O\ket{0}=\ket{\psi}$ acts on the on computational basis state $\ket{0}$ to create the state $\ket{\psi}$.</span></span>
<span data-ttu-id="d13b0-110">첫 번째 매개 변수는 $ \ket{\psi} $의 기본 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="d13b0-110">The first parameter is the qubit register of $\ket{\psi}$.</span></span>