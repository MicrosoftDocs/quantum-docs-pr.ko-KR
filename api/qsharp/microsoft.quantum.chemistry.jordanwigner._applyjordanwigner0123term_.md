---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWigner0123Term_
title: _ApplyJordanWigner0123Term_ 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWigner0123Term_
qsharp.summary: Applies time-evolution by a PQRS term described by a `GeneratorIndex`.
ms.openlocfilehash: 31105f1adae3c17d409dde7b48a9aac6b87fca39
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851743"
---
# <a name="_applyjordanwigner0123term_-operation"></a><span data-ttu-id="98522-102">_ApplyJordanWigner0123Term_ 작업</span><span class="sxs-lookup"><span data-stu-id="98522-102">_ApplyJordanWigner0123Term_ operation</span></span>

<span data-ttu-id="98522-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="98522-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="98522-104">패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="98522-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="98522-105">에 설명 된 PQRS 용어의 시간 진화를 적용 `GeneratorIndex` 합니다.</span><span class="sxs-lookup"><span data-stu-id="98522-105">Applies time-evolution by a PQRS term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWigner0123Term_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="98522-106">입력</span><span class="sxs-lookup"><span data-stu-id="98522-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="98522-107">용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="98522-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="98522-108">`GeneratorIndex` PQRS 용어를 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="98522-108">`GeneratorIndex` representing a PQRS term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="98522-109">Stsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="98522-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="98522-110">시간-진화 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="98522-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="98522-111">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="98522-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="98522-112">Hamiltonian의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="98522-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="98522-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="98522-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

