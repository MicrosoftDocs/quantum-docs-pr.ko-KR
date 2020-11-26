---
uid: Microsoft.Quantum.Simulation.EstimateEnergyWithAdiabaticEvolution
title: EstimateEnergyWithAdiabaticEvolution 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EstimateEnergyWithAdiabaticEvolution
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: b279d35418b8f013ad0d72e9a980c9bf6ce0689a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225332"
---
# <a name="estimateenergywithadiabaticevolution-operation"></a><span data-ttu-id="f595d-102">EstimateEnergyWithAdiabaticEvolution 작업</span><span class="sxs-lookup"><span data-stu-id="f595d-102">EstimateEnergyWithAdiabaticEvolution operation</span></span>

<span data-ttu-id="f595d-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="f595d-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="f595d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f595d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f595d-105">`statePrepUnitary`자동으로 할당 된 입력 상태에를 적용 하 고,를 사용 하 여 adiabatic 상태 준비를 수행 하 `adiabaticUnitary` 고,를 `qpeUnitary` 사용 하 여 결과 상태에 대 한 마지막 단계 추정치를 적용 하 여 상태 준비를 수행 합니다 `phaseEstAlgorithm` .</span><span class="sxs-lookup"><span data-stu-id="f595d-105">Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.</span></span>

```qsharp
operation EstimateEnergyWithAdiabaticEvolution (nQubits : Int, statePrepUnitary : (Qubit[] => Unit), adiabaticUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double)) : Double
```


## <a name="input"></a><span data-ttu-id="f595d-106">입력</span><span class="sxs-lookup"><span data-stu-id="f595d-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="f595d-107">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f595d-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f595d-108">시뮬레이션에 사용 되는 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f595d-108">Number of qubits used for the simulation.</span></span>


### <a name="stateprepunitary--qubit--unit"></a><span data-ttu-id="f595d-109">statePrepUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f595d-109">statePrepUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="f595d-110">초기 동적 생성기에 대 한 상태 준비를 나타내는 oracle입니다.</span><span class="sxs-lookup"><span data-stu-id="f595d-110">An oracle representing state preparation for the initial dynamical generator.</span></span>


### <a name="adiabaticunitary--qubit--unit"></a><span data-ttu-id="f595d-111">adiabaticUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f595d-111">adiabaticUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="f595d-112">알고리즘의 최종 상태에 대 한 스윕을 구현 하는 데 사용할 adiabatic 진화 알고리즘을 나타내는 oracle입니다.</span><span class="sxs-lookup"><span data-stu-id="f595d-112">An oracle representing the adiabatic evolution algorithm to be used to implement the sweeps to the final state of the algorithm.</span></span>


### <a name="qpeunitary--qubit--unit--is-adj--ctl"></a><span data-ttu-id="f595d-113">qpeUnitary: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl + Ctl</span><span class="sxs-lookup"><span data-stu-id="f595d-113">qpeUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="f595d-114">동적 생성기에서 그라운드 상태 $ \ket{\phi} $ 및 접지 상태 에너지 $E = \\ \a, \delta t $ 인 시간 $ \delta t $의 진화를 나타내는 단일 $U 연산자를 나타내는 oracle</span><span class="sxs-lookup"><span data-stu-id="f595d-114">An oracle representing a unitary operator $U$ representing evolution for time $\delta t$ under a dynamical generator with ground state $\ket{\phi}$ and ground state energy $E = \phi\\,\delta t$.</span></span>


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a><span data-ttu-id="f595d-115">phaseEstAlgorithm: ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f595d-115">phaseEstAlgorithm : ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span></span> 

<span data-ttu-id="f595d-116">지정 된 단일 작업에 대해 단계 예측을 수행 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="f595d-116">An operation that performs phase estimation on a given unitary operation.</span></span>
<span data-ttu-id="f595d-117">자세한 내용은 [반복 단계 예측](/quantum/libraries/characterization#iterative-phase-estimation) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f595d-117">See [iterative phase estimation](/quantum/libraries/characterization#iterative-phase-estimation) for more details.</span></span>



## <a name="output--double"></a><span data-ttu-id="f595d-118">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f595d-118">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f595d-119">$U $로 표시 되는 생성기의 그라운드 상태 에너지 $ \a$의 예상 $ \hat{\phi} $입니다.</span><span class="sxs-lookup"><span data-stu-id="f595d-119">An estimate $\hat{\phi}$ of the ground state energy $\phi$ of the generator represented by $U$.</span></span>