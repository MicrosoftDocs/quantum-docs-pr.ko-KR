---
uid: Microsoft.Quantum.Characterization.DiscretePhaseEstimationIteration
title: DiscretePhaseEstimationIteration 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: DiscretePhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.
ms.openlocfilehash: 167b53d7108c64d11a4f258d17e90ba78d7dd8d8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715072"
---
# <a name="discretephaseestimationiteration-operation"></a><span data-ttu-id="e4f02-102">DiscretePhaseEstimationIteration 작업</span><span class="sxs-lookup"><span data-stu-id="e4f02-102">DiscretePhaseEstimationIteration operation</span></span>

<span data-ttu-id="e4f02-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="e4f02-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="e4f02-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e4f02-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e4f02-105">단일 oracle의 정수 제곱을 사용 하 여 반복적인 (일반적으로 제어) 단계 예측 알고리즘의 단일 반복을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f02-105">Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.</span></span>

```qsharp
operation DiscretePhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, power : Int, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="e4f02-106">입력</span><span class="sxs-lookup"><span data-stu-id="e4f02-106">Input</span></span>

### <a name="oracle--discreteoracle"></a><span data-ttu-id="e4f02-107">oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="e4f02-107">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="e4f02-108">$U ^ m $이 지정 된 레지스터에 적용 되는 작업 (예: ^ m $이 지정 된 레지스터에 적용 됨). 여기서 $U $은 단계가 예상 되는 단일이 고, 여기서 $m $은 oracle에 지정 된 정수 거듭제곱입니다.</span><span class="sxs-lookup"><span data-stu-id="e4f02-108">Operation acting on an integer and a register, such that $U^m$ is applied to the given register, where $U$ is the unitary whose phase is to be estimated, and where $m$ is the integer power given to the oracle</span></span>


### <a name="power--int"></a><span data-ttu-id="e4f02-109">power: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e4f02-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e4f02-110">지정 된 단일 oracle을 적용 하는 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="e4f02-110">Number of times to apply the given unitary oracle.</span></span>


### <a name="theta--double"></a><span data-ttu-id="e4f02-111">테타: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e4f02-111">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e4f02-112">대상 상태에 대해 동작 하기 전에 컨트롤의 단계를 반전 하는 각도입니다.</span><span class="sxs-lookup"><span data-stu-id="e4f02-112">Angle by which to invert the phase on the control qubit before acting on the target state.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="e4f02-113">targetState: [[](xref:microsoft.quantum.lang-ref.qubit)]</span><span class="sxs-lookup"><span data-stu-id="e4f02-113">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e4f02-114">지정 된 단일 oracle에 의해 처리 되는 상태 등록입니다.</span><span class="sxs-lookup"><span data-stu-id="e4f02-114">Register of state acted upon by the given unitary oracle.</span></span>


### <a name="controlqubit--qubit"></a><span data-ttu-id="e4f02-115">Control의 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e4f02-115">controlQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e4f02-116">지정 된 oracle의 응용 프로그램을 제어 하는 데 사용 되는 보조 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="e4f02-116">An auxiliary qubit used to control the application of the given oracle.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e4f02-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e4f02-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

