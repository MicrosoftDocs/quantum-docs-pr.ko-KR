---
uid: Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance
title: AssertQubitIsInStateWithinTolerance 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitIsInStateWithinTolerance
qsharp.summary: >-
  Asserts that a qubit in the expected state.

  `expected` represents a complex vector, $\ket{\psi} = \begin{bmatrix}a & b\end{bmatrix}^{\mathrm{T}}$. The first element of the tuples representing each of $a$, $b$ is the real part of the complex number, while the second one is the imaginary part. The last argument defines the tolerance with which assertion is made.
ms.openlocfilehash: 5d34bdac53870326dacb5a11c27c857793c3f420
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712937"
---
# <a name="assertqubitisinstatewithintolerance-operation"></a><span data-ttu-id="529c8-102">AssertQubitIsInStateWithinTolerance 작업</span><span class="sxs-lookup"><span data-stu-id="529c8-102">AssertQubitIsInStateWithinTolerance operation</span></span>

<span data-ttu-id="529c8-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="529c8-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="529c8-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="529c8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="529c8-105">예상 상태에서의 비트를 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="529c8-105">Asserts that a qubit in the expected state.</span></span>

<span data-ttu-id="529c8-106">`expected` 복합 벡터, $ \ket{\psi} = \begin{bmatrix}a & b\end {bmatrix} ^ {\mathrm{T}} $를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="529c8-106">`expected` represents a complex vector, $\ket{\psi} = \begin{bmatrix}a & b\end{bmatrix}^{\mathrm{T}}$.</span></span>
<span data-ttu-id="529c8-107">$A $, $b $를 나타내는 튜플의 첫 번째 요소는 복소수의 실수부 이며 두 번째 요소는 허수 부분입니다.</span><span class="sxs-lookup"><span data-stu-id="529c8-107">The first element of the tuples representing each of $a$, $b$ is the real part of the complex number, while the second one is the imaginary part.</span></span>
<span data-ttu-id="529c8-108">마지막 인수는 어설션이 만들어지는 허용 오차를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="529c8-108">The last argument defines the tolerance with which assertion is made.</span></span>

```qsharp
operation AssertQubitIsInStateWithinTolerance (expected : (Microsoft.Quantum.Math.Complex, Microsoft.Quantum.Math.Complex), register : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="529c8-109">입력</span><span class="sxs-lookup"><span data-stu-id="529c8-109">Input</span></span>

### <a name="expected--complexcomplex"></a><span data-ttu-id="529c8-110">예상: ([복합](xref:Microsoft.Quantum.Math.Complex),[복합](xref:Microsoft.Quantum.Math.Complex))</span><span class="sxs-lookup"><span data-stu-id="529c8-110">expected : ([Complex](xref:Microsoft.Quantum.Math.Complex),[Complex](xref:Microsoft.Quantum.Math.Complex))</span></span>

<span data-ttu-id="529c8-111">각각 $ \ket {0} $ 및 $ \ket $에 대 한 복잡 한 amplitudes {1} 이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="529c8-111">Expected complex amplitudes for $\ket{0}$ and $\ket{1}$, respectively.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="529c8-112">등록: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="529c8-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="529c8-113">상태를 어설션할의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="529c8-113">Qubit whose state is to be asserted.</span></span> <span data-ttu-id="529c8-114">이 원하는 비트는 할당 되지 않은 다른 것으로 간주 되는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="529c8-114">Note that this qubit is assumed to be separable from other allocated qubits, and not entangled.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="529c8-115">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="529c8-115">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="529c8-116">실제 amplitudes이 예상 대로 벗어날 수 있는 추가 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="529c8-116">Additive tolerance by which actual amplitudes are allowed to deviate from expected.</span></span>
<span data-ttu-id="529c8-117">자세한 내용은 아래 설명 부분을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="529c8-117">See remarks below for details.</span></span>



## <a name="output--unit"></a><span data-ttu-id="529c8-118">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="529c8-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="529c8-119">설명</span><span class="sxs-lookup"><span data-stu-id="529c8-119">Remarks</span></span>

<span data-ttu-id="529c8-120">다음 Mathematica 코드를 사용 하 여 mi, mx, my, mz에 대 한 식을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="529c8-120">The following Mathematica code can be used to verify expressions for mi, mx, my, mz:</span></span>

```mathematica
{Id, X, Y, Z} = Table[PauliMatrix[k], {k, 0, 3}];
st = {{ reA + I imA }, { reB + I imB} };
M = st . ConjugateTranspose[st];
mx = Tr[M.X] // ComplexExpand;
my = Tr[M.Y] // ComplexExpand;
mz = Tr[M.Z] // ComplexExpand;
mi = Tr[M.Id] // ComplexExpand;
2 m == Id mi + X mx + Z mz + Y my // ComplexExpand // Simplify
```

<span data-ttu-id="529c8-121">허용 $L 오차는 \_ 3 차원 실제 벡터 (x ₂, \infty} $ distance x ₃, x ₄)에 의해 정의 된 $ \langle\psi | \psi\rangle = x \_ 1 I + x \_ 2 x + x \_ 3 y + x \_ 4 z $ 및 real vector (y ₂, y ₃, y ₄)에 의해 정의 됩니다. 여기서 ρ는 레지스터의 상태에 해당 하는 밀도 행렬입니다.</span><span class="sxs-lookup"><span data-stu-id="529c8-121">The tolerance is the $L\_{\infty}$ distance between 3 dimensional real vector (x₂,x₃,x₄) defined by $\langle\psi|\psi\rangle = x\_1 I + x\_2 X + x\_3 Y + x\_4 Z$ and real vector (y₂,y₃,y₄) defined by ρ = y₁I + y₂X + y₃Y + y₄Z where ρ is the density matrix corresponding to the state of the register.</span></span>
<span data-ttu-id="529c8-122">이는 Tr (ρ) 및 Tr (| ψ ⟩ ⟨ ψ |)이 모두 1 (예: x ₁ = 1/2, y ₁ = 1/2) 이라는 가정 하에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="529c8-122">This is only true under the assumption that Tr(ρ) and Tr(|ψ⟩⟨ψ|) are both 1 (e.g. x₁ = 1/2, y₁ = 1/2).</span></span>
<span data-ttu-id="529c8-123">그렇지 않은 경우 함수는 l ∞ distance between (x ₂-x ₁, x ₃-x ₁, x ₄-x ₁, x ₄ + x ₁) 및 (y ₂-y ₁, y ₃-y ₁ ₄, y ₁ + y ₄)이 허용 오차 매개 변수 보다 작음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="529c8-123">If this is not the case, the function asserts that l∞ distance between (x₂-x₁,x₃-x₁,x₄-x₁,x₄+x₁) and (y₂-y₁,y₃-y₁,y₄-y₁,y₄+y₁) is less than the tolerance parameter.</span></span>