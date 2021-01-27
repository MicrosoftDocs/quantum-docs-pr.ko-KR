---
uid: Microsoft.Quantum.Characterization.RobustPhaseEstimation
title: RobustPhaseEstimation 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: RobustPhaseEstimation
qsharp.summary: Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.
ms.openlocfilehash: 4b37c8275a5b2aee8534bacc5831281aa498b57d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851795"
---
# <a name="robustphaseestimation-operation"></a><span data-ttu-id="2a516-102">RobustPhaseEstimation 작업</span><span class="sxs-lookup"><span data-stu-id="2a516-102">RobustPhaseEstimation operation</span></span>

<span data-ttu-id="2a516-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="2a516-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="2a516-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2a516-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2a516-105">지정 된 oracle 및 eigenstate에 대 한 강력한 비 반복적인 퀀텀 단계 예측 알고리즘 `U` 을 수행 하 고 Heisenberg 한도에 분산 배율이 지정 된 단계의 단일 실제 값을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a516-105">Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.</span></span>

```qsharp
operation RobustPhaseEstimation (bitsPrecision : Int, oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a><span data-ttu-id="2a516-106">입력</span><span class="sxs-lookup"><span data-stu-id="2a516-106">Input</span></span>

### <a name="bitsprecision--int"></a><span data-ttu-id="2a516-107">bitsPrecision: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2a516-107">bitsPrecision : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2a516-108">이는 $ \phi \phi 10.7 \phi/\texts {queries} $와 같이 많은 수의 쿼리를 사용 하는 $ \a$의 추정치를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a516-108">This provides an estimate of $\phi$ with standard deviation $\sigma \le 2\pi / 2^\text{bitsPrecision}$ using a number of queries scaling like $\sigma \le 10.7 \pi / \text{# of queries}$.</span></span>


### <a name="oracle--discreteoracle"></a><span data-ttu-id="2a516-109">oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="2a516-109">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="2a516-110">지정 된 정수에 대 한 ^ m $ $U를 구현 하는 작업은 $ $m.</span><span class="sxs-lookup"><span data-stu-id="2a516-110">An operation implementing $U^m$ for given integer powers $m$.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="2a516-111">targetState: [[](xref:microsoft.quantum.lang-ref.qubit)]</span><span class="sxs-lookup"><span data-stu-id="2a516-111">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="2a516-112">$ $U 하는 퀀텀 레지스터가 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a516-112">A quantum register that $U$ acts on.</span></span> <span data-ttu-id="2a516-113">$U $의 eigenstate $ \ket{\phi} $ $U를 저장 하는 경우 $ \phi\in (-\pi, \pi] $의 \ket{\phi} = e ^ {i\phi} \ket{\phi} $에 대해 알 수 없는 단계가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a516-113">If it stores an eigenstate $\ket{\phi}$ of $U$, then $U\ket{\phi} = e^{i\phi} \ket{\phi}$ for $\phi\in(-\pi,\pi]$ an unknown phase.</span></span>



## <a name="output--double"></a><span data-ttu-id="2a516-114">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2a516-114">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="2a516-115">설명</span><span class="sxs-lookup"><span data-stu-id="2a516-115">Remarks</span></span>

<span data-ttu-id="2a516-116">많은 수의 쿼리를 제한 하는 경우 $ \\a$의 예상 값에 대 한 표준 편차에 대 한 낮은 범위를 Cramer-Rao 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a516-116">In the limit of a large number of queries, Cramer-Rao lower bounds for the standard deviation of the estimate of $\phi$ satisfy $\sigma \ge 2 \pi / \text{# of queries}$.</span></span>

## <a name="references"></a><span data-ttu-id="2a516-117">참조</span><span class="sxs-lookup"><span data-stu-id="2a516-117">References</span></span>

- <span data-ttu-id="2a516-118">강력한 단계 추정 Shelby Kimmel, Guang Jia-hao Low, (Yoder를 통한 범용 Single-Qubit Gate-Set의 강력한 보정 https://arxiv.org/abs/1502.02677</span><span class="sxs-lookup"><span data-stu-id="2a516-118">Robust Calibration of a Universal Single-Qubit Gate-Set via Robust Phase Estimation Shelby Kimmel, Guang Hao Low, Theodore J. Yoder https://arxiv.org/abs/1502.02677</span></span>