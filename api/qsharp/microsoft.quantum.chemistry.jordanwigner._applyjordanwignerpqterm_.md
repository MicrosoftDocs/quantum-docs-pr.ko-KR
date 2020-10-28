---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerPQTerm_
title: _ApplyJordanWignerPQTerm_ 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerPQTerm_
qsharp.summary: Applies time-evolution by a PQ term described by a `GeneratorIndex`.
ms.openlocfilehash: 8a9b41e17bcc46c5aff2b18455e1eac25620fe35
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714778"
---
# <a name="_applyjordanwignerpqterm_-operation"></a><span data-ttu-id="c1c06-102">_ApplyJordanWignerPQTerm_ 작업</span><span class="sxs-lookup"><span data-stu-id="c1c06-102">_ApplyJordanWignerPQTerm_ operation</span></span>

<span data-ttu-id="c1c06-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="c1c06-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="c1c06-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c1c06-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c1c06-105">에 설명 된 PQ 용어의 시간 진화를 적용 `GeneratorIndex` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1c06-105">Applies time-evolution by a PQ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerPQTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, extraParityQubits : Qubit[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="c1c06-106">입력</span><span class="sxs-lookup"><span data-stu-id="c1c06-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="c1c06-107">용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="c1c06-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="c1c06-108">`GeneratorIndex` PQ 용어를 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="c1c06-108">`GeneratorIndex` representing a PQ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="c1c06-109">Stsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c1c06-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c1c06-110">시간-진화 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="c1c06-110">Duration of time-evolution.</span></span>


### <a name="extraparityqubits--qubit"></a><span data-ttu-id="c1c06-111">extraParityQubits: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c1c06-111">extraParityQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c1c06-112">시간 진화의 부호를 대칭 이동 하는 선택적 패리티의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="c1c06-112">Optional parity qubits that flip the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="c1c06-113">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c1c06-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c1c06-114">Hamiltonian의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="c1c06-114">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c1c06-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c1c06-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

