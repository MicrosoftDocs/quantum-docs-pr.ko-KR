---
uid: Microsoft.Quantum.Simulation.EstimateEnergy
title: EstimateEnergy 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EstimateEnergy
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: ba4a5372aaf092c3ac3a1302f9715ca643be8436
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722055"
---
# <a name="estimateenergy-operation"></a><span data-ttu-id="ce2a2-102">EstimateEnergy 작업</span><span class="sxs-lookup"><span data-stu-id="ce2a2-102">EstimateEnergy operation</span></span>

<span data-ttu-id="ce2a2-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ce2a2-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ce2a2-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ce2a2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ce2a2-105">`statePrepUnitary` `qpeUnitary` 을 사용 하 여 결과 상태에 대해 자동으로 할당 된 입력 상태 단계 추정에를 적용 하 여 상태 준비를 수행 `phaseEstAlgorithm` 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2a2-105">Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.</span></span>

```qsharp
operation EstimateEnergy (nQubits : Int, statePrepUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double)) : Double
```


## <a name="input"></a><span data-ttu-id="ce2a2-106">입력</span><span class="sxs-lookup"><span data-stu-id="ce2a2-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="ce2a2-107">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ce2a2-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ce2a2-108">시뮬레이션을 수행 하는 데 사용 되는 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ce2a2-108">Number of qubits used to perform simulation.</span></span>


### <a name="stateprepunitary--qubit--unit"></a><span data-ttu-id="ce2a2-109">statePrepUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ce2a2-109">statePrepUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ce2a2-110">초기 동적 생성기에 대 한 상태 준비를 나타내는 oracle입니다.</span><span class="sxs-lookup"><span data-stu-id="ce2a2-110">An oracle representing state preparation for the initial dynamical generator.</span></span>


### <a name="qpeunitary--qubit--unit-adj--ctl"></a><span data-ttu-id="ce2a2-111">qpeUnitary: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="ce2a2-111">qpeUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="ce2a2-112">동적 생성기에서 그라운드 상태 $ \ket{\phi} $ 및 접지 상태 에너지 $E = \\ \a, \delta t $ 인 시간 $ \delta t $의 진화를 나타내는 단일 $U 연산자를 나타내는 oracle</span><span class="sxs-lookup"><span data-stu-id="ce2a2-112">An oracle representing a unitary operator $U$ representing evolution for time $\delta t$ under a dynamical generator with ground state $\ket{\phi}$ and ground state energy $E = \phi\\,\delta t$.</span></span>


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a><span data-ttu-id="ce2a2-113">phaseEstAlgorithm: ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ce2a2-113">phaseEstAlgorithm : ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span></span> 

<span data-ttu-id="ce2a2-114">지정 된 단일 작업에 대해 단계 예측을 수행 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="ce2a2-114">An operation that performs phase estimation on a given unitary operation.</span></span>
<span data-ttu-id="ce2a2-115">자세한 내용은 [반복 단계 예측](/quantum/libraries/characterization#iterative-phase-estimation) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ce2a2-115">See [iterative phase estimation](/quantum/libraries/characterization#iterative-phase-estimation) for more details.</span></span>



## <a name="output--double"></a><span data-ttu-id="ce2a2-116">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ce2a2-116">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ce2a2-117">$U $로 표시 되는 생성기의 그라운드 상태 에너지 $ \\a$의 예상 $ \hat{\phi} $입니다.</span><span class="sxs-lookup"><span data-stu-id="ce2a2-117">An estimate $\hat{\phi}$ of the ground state energy $\phi$ of the ground state energy of the generator represented by $U$.</span></span>