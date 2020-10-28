---
uid: Microsoft.Quantum.Characterization.ContinuousPhaseEstimationIteration
title: ContinuousPhaseEstimationIteration 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ContinuousPhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.
ms.openlocfilehash: a3914a4b19e3b898b6de8808699da09d386f487a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715079"
---
# <a name="continuousphaseestimationiteration-operation"></a><span data-ttu-id="d7243-102">ContinuousPhaseEstimationIteration 작업</span><span class="sxs-lookup"><span data-stu-id="d7243-102">ContinuousPhaseEstimationIteration operation</span></span>

<span data-ttu-id="d7243-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="d7243-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="d7243-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d7243-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d7243-105">단일 oracle의 임의의 실제 성능을 사용 하 여 반복적인 (일반적으로 제어) 단계 추정 알고리즘의 단일 반복을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7243-105">Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.</span></span>

```qsharp
operation ContinuousPhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.ContinuousOracle, time : Double, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="d7243-106">입력</span><span class="sxs-lookup"><span data-stu-id="d7243-106">Input</span></span>

### <a name="oracle--continuousoracle"></a><span data-ttu-id="d7243-107">oracle: [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span><span class="sxs-lookup"><span data-stu-id="d7243-107">oracle : [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span></span>

<span data-ttu-id="d7243-108">$U ^ t $가 지정 된 레지스터에 적용 되는 작업 (예: "^ t $")이 지정 된 레지스터에 적용 되는 $t 작업입니다. 여기서 $U $은 단계가 예상 되는 단일이 고, $t 여기서 $는 oracle에 지정 된 정수 거듭제곱입니다.</span><span class="sxs-lookup"><span data-stu-id="d7243-108">Operation acting on a double $t$ and a register, such that $U^t$ is applied to the given register, where $U$ is the unitary whose phase is to be estimated, and where $t$ is the integer power given to the oracle</span></span>


### <a name="time--double"></a><span data-ttu-id="d7243-109">시간: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d7243-109">time : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d7243-110">지정 된 단일 oracle을 적용 하는 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="d7243-110">Number of times to apply the given unitary oracle.</span></span>


### <a name="theta--double"></a><span data-ttu-id="d7243-111">테타: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d7243-111">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d7243-112">대상 상태에 대해 동작 하기 전에 컨트롤의 단계를 반전 하는 각도입니다.</span><span class="sxs-lookup"><span data-stu-id="d7243-112">Angle by which to invert the phase on the control qubit before acting on the target state.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="d7243-113">targetState: [[](xref:microsoft.quantum.lang-ref.qubit)]</span><span class="sxs-lookup"><span data-stu-id="d7243-113">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d7243-114">지정 된 단일 oracle에 의해 처리 되는 상태 등록입니다.</span><span class="sxs-lookup"><span data-stu-id="d7243-114">Register of state acted upon by the given unitary oracle.</span></span>


### <a name="controlqubit--qubit"></a><span data-ttu-id="d7243-115">Control의 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d7243-115">controlQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="d7243-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d7243-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

