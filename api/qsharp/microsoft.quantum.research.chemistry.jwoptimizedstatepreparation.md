---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedStatePreparation
title: JWOptimizedStatePreparation 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedStatePreparation
qsharp.summary: Simple state preparation of trial state by occupying spin-orbitals
ms.openlocfilehash: a2e0c24eaa1f5326f2d531b4e7e55b2c440bc795
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229854"
---
# <a name="jwoptimizedstatepreparation-operation"></a><span data-ttu-id="25f94-102">JWOptimizedStatePreparation 작업</span><span class="sxs-lookup"><span data-stu-id="25f94-102">JWOptimizedStatePreparation operation</span></span>

<span data-ttu-id="25f94-103">네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Chemistry) .</span><span class="sxs-lookup"><span data-stu-id="25f94-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="25f94-104">패키지: [Microsoft](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry) .</span><span class="sxs-lookup"><span data-stu-id="25f94-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="25f94-105">Spin orbitals를 실행 하 여 시험 상태의 단순 상태 준비</span><span class="sxs-lookup"><span data-stu-id="25f94-105">Simple state preparation of trial state by occupying spin-orbitals</span></span>

```qsharp
operation JWOptimizedStatePreparation (qubitIndices : Int[], qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="25f94-106">입력</span><span class="sxs-lookup"><span data-stu-id="25f94-106">Input</span></span>

### <a name="qubitindices--int"></a><span data-ttu-id="25f94-107">Bit인덱스: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="25f94-107">qubitIndices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="25f94-108">파괴가 차지 하는 비트의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="25f94-108">Indices of qubits to be occupied by electrons.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="25f94-109">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="25f94-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="25f94-110">Hamiltonian의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="25f94-110">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="25f94-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="25f94-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

