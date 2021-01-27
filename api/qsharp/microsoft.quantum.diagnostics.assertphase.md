---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: AssertPhase 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: 59fa0f2f68b4de271b972aef776ee5097fd5c201
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830071"
---
# <a name="assertphase-operation"></a><span data-ttu-id="0767d-102">AssertPhase 작업</span><span class="sxs-lookup"><span data-stu-id="0767d-102">AssertPhase operation</span></span>

<span data-ttu-id="0767d-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="0767d-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="0767d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0767d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0767d-105">Equal superposition 상태의 단계가 예상 값을 포함 한다는 것을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="0767d-105">Asserts that the phase of an equal superposition state has the expected value.</span></span>

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="0767d-106">설명</span><span class="sxs-lookup"><span data-stu-id="0767d-106">Description</span></span>

<span data-ttu-id="0767d-107">이 작업을 수행 하면 일부 임의의 실제 $t $에 대해 $ \frac{e ^ {i t}} {\phi {2} } (e ^ {i\phi} \ {0} + e ^ {-i\eml} \ k) $로 표현 될 수 있는 퀀텀 상태의 $ \eml$ 단계가 {1} 예상 값을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="0767d-107">This operation asserts that the phase $\phi$ of a quantum state that may be expressed as $\frac{e^{i t}}{\sqrt{2}}(e^{i\phi}\ket{0} + e^{-i\phi}\ket{1})$ for some arbitrary real $t$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="0767d-108">입력</span><span class="sxs-lookup"><span data-stu-id="0767d-108">Input</span></span>

### <a name="expected--double"></a><span data-ttu-id="0767d-109">예상: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0767d-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0767d-110">예상 값은 $ \\a\in (-\phi, \phi] $입니다.</span><span class="sxs-lookup"><span data-stu-id="0767d-110">The expected value of $\phi \in (-\pi,\pi]$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="0767d-111">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0767d-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0767d-112">예상 상태를 저장 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="0767d-112">The qubit that stores the expected state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="0767d-113">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0767d-113">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0767d-114">실제 및 예상의 차이에 대 한 절대 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="0767d-114">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0767d-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0767d-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="0767d-116">예</span><span class="sxs-lookup"><span data-stu-id="0767d-116">Example</span></span>

<span data-ttu-id="0767d-117">다음 어설션이 성공 합니다. `qubit` 는 상태 $ \ket{\psi} = e ^ {i 0.5} \ sqrt {1/2} \ k {0} + e ^ {i 0.5} \ a 1/2} \ k {1} $;입니다.</span><span class="sxs-lookup"><span data-stu-id="0767d-117">The following assert succeeds: `qubit` is in state $\ket{\psi}=e^{i 0.5}\sqrt{1/2}\ket{0}+e^{i 0.5}\sqrt{1/2}\ket{1}$;</span></span>

- `AssertPhase(0.0,qubit,10e-10);`

<span data-ttu-id="0767d-118">`qubit` 상태 $ \ket{\psi} = e ^ {i 0.5} \ sqrt {1/2} \ k {0} + e ^ {-i 0.5} \ sqrt {1/2} \ k {1} $;</span><span class="sxs-lookup"><span data-stu-id="0767d-118">`qubit` is in state $\ket{\psi}=e^{i 0.5}\sqrt{1/2}\ket{0}+e^{-i 0.5}\sqrt{1/2}\ket{1}$;</span></span>

- `AssertPhase(0.5,qubit,10e-10);`

<span data-ttu-id="0767d-119">`qubit` 상태 $ \ket{\psi} = e ^ {-i 2.2} \ sqrt {1/2} \ k {0} + e ^ {i 0.2} \ a s t 1/2} \ k {1} $;입니다.</span><span class="sxs-lookup"><span data-stu-id="0767d-119">`qubit` is in state $\ket{\psi}=e^{-i 2.2}\sqrt{1/2}\ket{0}+e^{i 0.2}\sqrt{1/2}\ket{1}$;</span></span>

- `AssertPhase(-1.2,qubit,10e-10);`