---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: AssertPhase 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: e042c03d2a72d9ce4816a8cdb56603e175b22807
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712951"
---
# <a name="assertphase-operation"></a><span data-ttu-id="20869-102">AssertPhase 작업</span><span class="sxs-lookup"><span data-stu-id="20869-102">AssertPhase operation</span></span>

<span data-ttu-id="20869-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="20869-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="20869-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="20869-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="20869-105">Equal superposition 상태의 단계가 예상 값을 포함 한다는 것을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="20869-105">Asserts that the phase of an equal superposition state has the expected value.</span></span>

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="20869-106">Description</span><span class="sxs-lookup"><span data-stu-id="20869-106">Description</span></span>

<span data-ttu-id="20869-107">이 작업을 수행 하면 일부 임의의 실제 $t $에 대해 $ \frac{e ^ {i t}} {\phi {2} } (e ^ {i\phi} \ {0} + e ^ {-i\eml} \ k) $로 표현 될 수 있는 퀀텀 상태의 $ \eml$ 단계가 {1} 예상 값을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="20869-107">This operation asserts that the phase $\phi$ of a quantum state that may be expressed as $\frac{e^{i t}}{\sqrt{2}}(e^{i\phi}\ket{0} + e^{-i\phi}\ket{1})$ for some arbitrary real $t$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="20869-108">입력</span><span class="sxs-lookup"><span data-stu-id="20869-108">Input</span></span>

### <a name="expected--double"></a><span data-ttu-id="20869-109">예상: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="20869-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="20869-110">예상 값은 $ \\a\in (-\phi, \phi] $입니다.</span><span class="sxs-lookup"><span data-stu-id="20869-110">The expected value of $\phi \in (-\pi,\pi]$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="20869-111">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="20869-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="20869-112">예상 상태를 저장 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="20869-112">The qubit that stores the expected state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="20869-113">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="20869-113">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="20869-114">실제 및 예상의 차이에 대 한 절대 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="20869-114">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="20869-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="20869-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

