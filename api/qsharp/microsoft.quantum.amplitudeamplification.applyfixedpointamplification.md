---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: ApplyFixedPointAmplification 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: fa19c3bb06ae91a2fa18acb6f853020830e749f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847225"
---
# <a name="applyfixedpointamplification-operation"></a><span data-ttu-id="f89b3-102">ApplyFixedPointAmplification 작업</span><span class="sxs-lookup"><span data-stu-id="f89b3-102">ApplyFixedPointAmplification operation</span></span>

<span data-ttu-id="f89b3-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="f89b3-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="f89b3-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f89b3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f89b3-105">Fixed-Point 진폭 증폭 알고리즘</span><span class="sxs-lookup"><span data-stu-id="f89b3-105">Fixed-Point Amplitude Amplification algorithm</span></span>

```qsharp
operation ApplyFixedPointAmplification (statePrepOracle : Microsoft.Quantum.Oracles.StateOracle, startQubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="f89b3-106">입력</span><span class="sxs-lookup"><span data-stu-id="f89b3-106">Input</span></span>

### <a name="statepreporacle--stateoracle"></a><span data-ttu-id="f89b3-107">statePrepOracle: [Stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="f89b3-107">statePrepOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="f89b3-108">시작 상태를 준비 하는 단일 oracle.</span><span class="sxs-lookup"><span data-stu-id="f89b3-108">Unitary oracle that prepares the start state.</span></span>


### <a name="startqubits--qubit"></a><span data-ttu-id="f89b3-109">startQubits: [\Bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f89b3-109">startQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f89b3-110">비트율 비트 레지스터</span><span class="sxs-lookup"><span data-stu-id="f89b3-110">Qubit register</span></span>



## <a name="output--unit"></a><span data-ttu-id="f89b3-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f89b3-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f89b3-112">설명</span><span class="sxs-lookup"><span data-stu-id="f89b3-112">Remarks</span></span>

<span data-ttu-id="f89b3-113">StartQubits는 $ \ket{0 \cdots 0} $ 상태 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89b3-113">The startQubits must be in the $\ket{0 \cdots 0}$ state.</span></span> <span data-ttu-id="f89b3-114">이 작업은 최대 쿼리 수에 도달 하거나 대상 상태가 발견 될 때까지 $2 $의 거듭제곱으로 많은 쿼리를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89b3-114">This operation iterates over a number of queries in powers of $2$ until either a maximal number of queries is reached, or the target state is found.</span></span>