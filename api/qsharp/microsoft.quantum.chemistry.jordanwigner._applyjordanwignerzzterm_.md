---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerZZTerm_
title: _ApplyJordanWignerZZTerm_ 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerZZTerm_
qsharp.summary: Applies time-evolution by a ZZ term described by a `GeneratorIndex`.
ms.openlocfilehash: 9f03255d53f7ed7f3e79689ea53c8b95133f6cde
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714722"
---
# <a name="_applyjordanwignerzzterm_-operation"></a><span data-ttu-id="507d3-102">_ApplyJordanWignerZZTerm_ 작업</span><span class="sxs-lookup"><span data-stu-id="507d3-102">_ApplyJordanWignerZZTerm_ operation</span></span>

<span data-ttu-id="507d3-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="507d3-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="507d3-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="507d3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="507d3-105">에서 설명 하는 ZZ 용어에의 한 시간 진화를 적용 `GeneratorIndex` 합니다.</span><span class="sxs-lookup"><span data-stu-id="507d3-105">Applies time-evolution by a ZZ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerZZTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="507d3-106">입력</span><span class="sxs-lookup"><span data-stu-id="507d3-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="507d3-107">용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="507d3-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="507d3-108">`GeneratorIndex` ZZ 용어를 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="507d3-108">`GeneratorIndex` representing a ZZ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="507d3-109">Stsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="507d3-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="507d3-110">시간-진화 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="507d3-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="507d3-111">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="507d3-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="507d3-112">Hamiltonian의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="507d3-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="507d3-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="507d3-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

