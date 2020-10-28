---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerClusterOperatorPQRSTerm
title: _ApplyJordanWignerClusterOperatorPQRSTerm 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerClusterOperatorPQRSTerm
qsharp.summary: Applies time-evolution by a cluster operator PQRS term described by a `GeneratorIndex`.
ms.openlocfilehash: 9f5cd58747b16d3fc755c202fd905394fc221d53
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714806"
---
# <a name="_applyjordanwignerclusteroperatorpqrsterm-operation"></a><span data-ttu-id="3aa2f-102">_ApplyJordanWignerClusterOperatorPQRSTerm 작업</span><span class="sxs-lookup"><span data-stu-id="3aa2f-102">_ApplyJordanWignerClusterOperatorPQRSTerm operation</span></span>

<span data-ttu-id="3aa2f-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="3aa2f-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="3aa2f-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3aa2f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3aa2f-105">에서 설명 하는 클러스터 연산자 PQRS 용어에의 한 시간 진화를 적용 `GeneratorIndex` 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aa2f-105">Applies time-evolution by a cluster operator PQRS term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerClusterOperatorPQRSTerm (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="3aa2f-106">입력</span><span class="sxs-lookup"><span data-stu-id="3aa2f-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="3aa2f-107">용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="3aa2f-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="3aa2f-108">`GeneratorIndex` 클러스터 운영자 PQRS 용어를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3aa2f-108">`GeneratorIndex` representing a cluster operator PQRS term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="3aa2f-109">Stsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="3aa2f-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="3aa2f-110">시간-진화 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="3aa2f-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="3aa2f-111">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3aa2f-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3aa2f-112">Hamiltonian의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="3aa2f-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3aa2f-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3aa2f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

