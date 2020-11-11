---
uid: Microsoft.Quantum.Characterization.QuantumPhaseEstimation
title: QuantumPhaseEstimation 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: QuantumPhaseEstimation
qsharp.summary: Performs the quantum phase estimation algorithm for a given oracle `U` and `targetState`, reading the phase into a big-endian quantum register.
ms.openlocfilehash: 7e524477a4b2bcd8d6767441e278fbf501355e0c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714946"
---
# <a name="quantumphaseestimation-operation"></a><span data-ttu-id="acf07-102">QuantumPhaseEstimation 작업</span><span class="sxs-lookup"><span data-stu-id="acf07-102">QuantumPhaseEstimation operation</span></span>

<span data-ttu-id="acf07-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="acf07-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="acf07-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="acf07-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="acf07-105">지정 된 oracle에 대 한 퀀텀 단계 추정 알고리즘 `U` `targetState` 을 수행 하 고 해당 단계를 빅 endian 퀀텀 레지스터로 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="acf07-105">Performs the quantum phase estimation algorithm for a given oracle `U` and `targetState`, reading the phase into a big-endian quantum register.</span></span>

```qsharp
operation QuantumPhaseEstimation (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[], controlRegister : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="acf07-106">입력</span><span class="sxs-lookup"><span data-stu-id="acf07-106">Input</span></span>

### <a name="oracle--discreteoracle"></a><span data-ttu-id="acf07-107">oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="acf07-107">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="acf07-108">지정 된 정수에 대 한 ^ m $ $U를 구현 하는 작업은 m입니다.</span><span class="sxs-lookup"><span data-stu-id="acf07-108">An operation implementing $U^m$ for given integer powers m.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="acf07-109">targetState: [[](xref:microsoft.quantum.lang-ref.qubit)]</span><span class="sxs-lookup"><span data-stu-id="acf07-109">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="acf07-110">$ \Ket{\phi} $에서 처리 된 $ $ 상태를 나타내는 퀀텀 레지스터가 $U $입니다.</span><span class="sxs-lookup"><span data-stu-id="acf07-110">A quantum register representing the state $\ket{\phi}$ acted on by $U$.</span></span> <span data-ttu-id="acf07-111">$ \Ket{\phi} $가 $U $, $U \ket{\phi} = e ^ {i\emi\$의 eigenstate 인 경우 [0, 2 \ pi) $에서 알 수 없는 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="acf07-111">If $\ket{\phi}$ is an eigenstate of $U$, $U\ket{\phi} = e^{i\phi} \ket{\phi}$ for $\phi \in [0, 2\pi)$ an unknown phase.</span></span>


### <a name="controlregister--bigendian"></a><span data-ttu-id="acf07-112">controlRegister:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="acf07-112">controlRegister : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="acf07-113">제공 된 oracle을 제어 하는 데 사용할 수 있으며이 작업을 적용 한 다음에 $ \\a$의 표현을 포함 하는 빅 endian 표현 정수 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="acf07-113">A big-endian representation integer register that can be used to control the provided oracle, and that will contain the a representation of $\phi$ following the application of this operation.</span></span> <span data-ttu-id="acf07-114">ControlRegister는 초기 상태 $ \ket{00\cdots 0} $에서 시작 하는 것으로 간주 됩니다. 여기서 레지스터의 길이는 원하는 전체 자릿수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="acf07-114">The controlRegister is assumed to start in the initial state $\ket{00\cdots 0}$, where the length of the register indicates the desired precision.</span></span>



## <a name="output--unit"></a><span data-ttu-id="acf07-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="acf07-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
