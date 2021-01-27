---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedPQandPQQRTerm
title: _JWOptimizedPQandPQQRTerm 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedPQandPQQRTerm
qsharp.summary: Applies time-evolution by a PQ or PQQR term described by a `GeneratorIndex`.
ms.openlocfilehash: 97ae285ede38883f058b3e7609f9a26fb9e4340a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854770"
---
# <a name="_jwoptimizedpqandpqqrterm-operation"></a><span data-ttu-id="5a686-102">_JWOptimizedPQandPQQRTerm 작업</span><span class="sxs-lookup"><span data-stu-id="5a686-102">_JWOptimizedPQandPQQRTerm operation</span></span>

<span data-ttu-id="5a686-103">네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Chemistry) .</span><span class="sxs-lookup"><span data-stu-id="5a686-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="5a686-104">패키지: [Microsoft](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry) .</span><span class="sxs-lookup"><span data-stu-id="5a686-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="5a686-105">에 설명 된 PQ 또는 PQQR 용어로 시간 진화를 적용 `GeneratorIndex` 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a686-105">Applies time-evolution by a PQ or PQQR term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _JWOptimizedPQandPQQRTerm (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, parityQubit : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="5a686-106">입력</span><span class="sxs-lookup"><span data-stu-id="5a686-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="5a686-107">용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="5a686-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="5a686-108">`GeneratorIndex` PQ 또는 PQQr term을 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="5a686-108">`GeneratorIndex` representing a PQ or PQQr term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="5a686-109">Stsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5a686-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5a686-110">시간-진화 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="5a686-110">Duration of time-evolution.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="5a686-111">Paritybit: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5a686-111">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5a686-112">시간 진화의 부호를 결정 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="5a686-112">Qubit that determines the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="5a686-113">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5a686-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5a686-114">Hamiltonian의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="5a686-114">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5a686-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5a686-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

