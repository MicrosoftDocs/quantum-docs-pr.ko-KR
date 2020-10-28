---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerZTerm_
title: _ApplyJordanWignerZTerm_ 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerZTerm_
qsharp.summary: Applies time-evolution by a Z term described by a `GeneratorIndex`.
ms.openlocfilehash: f42c2ba7570f32d3f26ff82dd4a0ee6f9677fa30
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714729"
---
# <a name="_applyjordanwignerzterm_-operation"></a><span data-ttu-id="080ce-102">_ApplyJordanWignerZTerm_ 작업</span><span class="sxs-lookup"><span data-stu-id="080ce-102">_ApplyJordanWignerZTerm_ operation</span></span>

<span data-ttu-id="080ce-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="080ce-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="080ce-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="080ce-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="080ce-105">에서 설명 하는 Z 용어에의 한 시간 진화를 적용 `GeneratorIndex` 합니다.</span><span class="sxs-lookup"><span data-stu-id="080ce-105">Applies time-evolution by a Z term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerZTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="080ce-106">입력</span><span class="sxs-lookup"><span data-stu-id="080ce-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="080ce-107">용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="080ce-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="080ce-108">`GeneratorIndex` Z 용어를 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="080ce-108">`GeneratorIndex` representing a Z term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="080ce-109">Stsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="080ce-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="080ce-110">시간-진화 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="080ce-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="080ce-111">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="080ce-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="080ce-112">Hamiltonian의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="080ce-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="080ce-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="080ce-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

