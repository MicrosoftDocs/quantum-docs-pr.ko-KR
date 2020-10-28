---
uid: Microsoft.Quantum.Chemistry.JordanWigner.PrepareSingleConfigurationalStateSingleSiteOccupation
title: PrepareSingleConfigurationalStateSingleSiteOccupation 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: PrepareSingleConfigurationalStateSingleSiteOccupation
qsharp.summary: Simple state preparation of trial state by occupying spin-orbitals
ms.openlocfilehash: de385b7ffd76c1deaa41cf0cd3338d3243feb1fd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713868"
---
# <a name="preparesingleconfigurationalstatesinglesiteoccupation-operation"></a><span data-ttu-id="59bf9-102">PrepareSingleConfigurationalStateSingleSiteOccupation 작업</span><span class="sxs-lookup"><span data-stu-id="59bf9-102">PrepareSingleConfigurationalStateSingleSiteOccupation operation</span></span>

<span data-ttu-id="59bf9-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="59bf9-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="59bf9-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="59bf9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="59bf9-105">Spin orbitals를 실행 하 여 시험 상태의 단순 상태 준비</span><span class="sxs-lookup"><span data-stu-id="59bf9-105">Simple state preparation of trial state by occupying spin-orbitals</span></span>

```qsharp
operation PrepareSingleConfigurationalStateSingleSiteOccupation (qubitIndices : Int[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="59bf9-106">입력</span><span class="sxs-lookup"><span data-stu-id="59bf9-106">Input</span></span>

### <a name="qubitindices--int"></a><span data-ttu-id="59bf9-107">Bit인덱스: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="59bf9-107">qubitIndices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="59bf9-108">파괴가 차지 하는 비트의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="59bf9-108">Indices of qubits to be occupied by electrons.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="59bf9-109">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="59bf9-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="59bf9-110">Hamiltonian의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="59bf9-110">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="59bf9-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="59bf9-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

