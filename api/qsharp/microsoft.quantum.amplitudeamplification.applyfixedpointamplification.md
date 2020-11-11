---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: ApplyFixedPointAmplification 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: f506be7b2e3f65cf89694e30d79c04ec30d25035
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721908"
---
# <a name="applyfixedpointamplification-operation"></a><span data-ttu-id="409ee-102">ApplyFixedPointAmplification 작업</span><span class="sxs-lookup"><span data-stu-id="409ee-102">ApplyFixedPointAmplification operation</span></span>

<span data-ttu-id="409ee-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="409ee-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="409ee-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="409ee-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="409ee-105">Fixed-Point 진폭 증폭 알고리즘</span><span class="sxs-lookup"><span data-stu-id="409ee-105">Fixed-Point Amplitude Amplification algorithm</span></span>

```qsharp
operation ApplyFixedPointAmplification (statePrepOracle : Microsoft.Quantum.Oracles.StateOracle, startQubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="409ee-106">입력</span><span class="sxs-lookup"><span data-stu-id="409ee-106">Input</span></span>

### <a name="statepreporacle--stateoracle"></a><span data-ttu-id="409ee-107">statePrepOracle: [Stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="409ee-107">statePrepOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="409ee-108">시작 상태를 준비 하는 단일 oracle.</span><span class="sxs-lookup"><span data-stu-id="409ee-108">Unitary oracle that prepares the start state.</span></span>


### <a name="startqubits--qubit"></a><span data-ttu-id="409ee-109">startQubits: [\Bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="409ee-109">startQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="409ee-110">비트율 비트 레지스터</span><span class="sxs-lookup"><span data-stu-id="409ee-110">Qubit register</span></span>



## <a name="output--unit"></a><span data-ttu-id="409ee-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="409ee-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="409ee-112">설명</span><span class="sxs-lookup"><span data-stu-id="409ee-112">Remarks</span></span>

<span data-ttu-id="409ee-113">StartQubits는 $ \ket{0 \cdots 0} $ 상태 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="409ee-113">The startQubits must be in the $\ket{0 \cdots 0}$ state.</span></span> <span data-ttu-id="409ee-114">이 작업은 최대 쿼리 수에 도달 하거나 대상 상태가 발견 될 때까지 $2 $의 거듭제곱으로 많은 쿼리를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="409ee-114">This operation iterates over a number of queries in powers of $2$ until either a maximal number of queries is reached, or the target state is found.</span></span>