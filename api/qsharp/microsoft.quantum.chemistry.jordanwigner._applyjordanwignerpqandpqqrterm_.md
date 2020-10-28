---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerPQandPQQRTerm_
title: _ApplyJordanWignerPQandPQQRTerm_ 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerPQandPQQRTerm_
qsharp.summary: Applies time-evolution by a PQ or PQQR term described by a `GeneratorIndex`.
ms.openlocfilehash: a2a74ddeb7ecefaf4aa21374302d2709ee676e5d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714792"
---
# <a name="_applyjordanwignerpqandpqqrterm_-operation"></a><span data-ttu-id="c1004-102">_ApplyJordanWignerPQandPQQRTerm_ 작업</span><span class="sxs-lookup"><span data-stu-id="c1004-102">_ApplyJordanWignerPQandPQQRTerm_ operation</span></span>

<span data-ttu-id="c1004-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="c1004-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="c1004-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c1004-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c1004-105">에 설명 된 PQ 또는 PQQR 용어로 시간 진화를 적용 `GeneratorIndex` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1004-105">Applies time-evolution by a PQ or PQQR term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerPQandPQQRTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="c1004-106">입력</span><span class="sxs-lookup"><span data-stu-id="c1004-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="c1004-107">용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="c1004-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="c1004-108">`GeneratorIndex` PQ 또는 PQQR term을 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="c1004-108">`GeneratorIndex` representing a PQ or PQQR term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="c1004-109">Stsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c1004-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c1004-110">시간-진화 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="c1004-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="c1004-111">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c1004-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c1004-112">Hamiltonian의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="c1004-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c1004-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c1004-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

