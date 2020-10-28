---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimized0123Term
title: _JWOptimized0123Term 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimized0123Term
qsharp.summary: Applies time-evolution by a PQRS term described by a `GeneratorIndex`.
ms.openlocfilehash: 7382f3167055bbc2a499fa9490f89a0eb147e3e2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710844"
---
# <a name="_jwoptimized0123term-operation"></a><span data-ttu-id="ba8c6-102">_JWOptimized0123Term 작업</span><span class="sxs-lookup"><span data-stu-id="ba8c6-102">_JWOptimized0123Term operation</span></span>

<span data-ttu-id="ba8c6-103">네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Chemistry) .</span><span class="sxs-lookup"><span data-stu-id="ba8c6-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="ba8c6-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ba8c6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ba8c6-105">에 설명 된 PQRS 용어의 시간 진화를 적용 `GeneratorIndex` 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba8c6-105">Applies time-evolution by a PQRS term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _JWOptimized0123Term (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, parityQubit : Qubit, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="ba8c6-106">입력</span><span class="sxs-lookup"><span data-stu-id="ba8c6-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="ba8c6-107">용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="ba8c6-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="ba8c6-108">`GeneratorIndex` PQRS 용어를 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="ba8c6-108">`GeneratorIndex` representing a PQRS term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="ba8c6-109">Stsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ba8c6-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ba8c6-110">시간-진화 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="ba8c6-110">Duration of time-evolution.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="ba8c6-111">Paritybit: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ba8c6-111">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ba8c6-112">시간 진화의 부호를 결정 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="ba8c6-112">Qubit that determines the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="ba8c6-113">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ba8c6-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ba8c6-114">Hamiltonian의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="ba8c6-114">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ba8c6-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ba8c6-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

