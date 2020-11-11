---
uid: Microsoft.Quantum.Preparation.PrepareUniformSuperposition
title: PrepareUniformSuperposition 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareUniformSuperposition
qsharp.summary: >-
  Creates a uniform superposition over states that encode 0 through `nIndices - 1`.

  That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$. In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}. \end{align} $$.
ms.openlocfilehash: 8b57a7a02e9f704cf9677574824dfdc93fff25b0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709458"
---
# <a name="prepareuniformsuperposition-operation"></a><span data-ttu-id="2075a-102">PrepareUniformSuperposition 작업</span><span class="sxs-lookup"><span data-stu-id="2075a-102">PrepareUniformSuperposition operation</span></span>

<span data-ttu-id="2075a-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="2075a-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="2075a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2075a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2075a-105">0부터까지 인코딩하는 상태에 대 한 균일 한 superposition를 만듭니다 `nIndices - 1` .</span><span class="sxs-lookup"><span data-stu-id="2075a-105">Creates a uniform superposition over states that encode 0 through `nIndices - 1`.</span></span>

<span data-ttu-id="2075a-106">즉,이 단일 $U $는 입력 상태가 $ \ket{0\cdots 0} $ 인 경우 $0 $에서 $1 $M까지 모든 숫자 상태에 대 한 균일 한 superposition를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2075a-106">That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$.</span></span> <span data-ttu-id="2075a-107">즉, $ $ \begin{align} U\ket {0} = \frac {1} {\sqrt{m}}\ sum_ {j = 0} ^ {M-1} \ket{j}.</span><span class="sxs-lookup"><span data-stu-id="2075a-107">In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}.</span></span>
<span data-ttu-id="2075a-108">\end{align} $ $.</span><span class="sxs-lookup"><span data-stu-id="2075a-108">\end{align} $$.</span></span>

```qsharp
operation PrepareUniformSuperposition (nIndices : Int, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="2075a-109">입력</span><span class="sxs-lookup"><span data-stu-id="2075a-109">Input</span></span>

### <a name="nindices--int"></a><span data-ttu-id="2075a-110">n 인덱스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2075a-110">nIndices : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2075a-111">Uniform superposition에서 원하는 상태 수 $M $입니다.</span><span class="sxs-lookup"><span data-stu-id="2075a-111">The desired number of states $M$ in the uniform superposition.</span></span>


### <a name="indexregister--littleendian"></a><span data-ttu-id="2075a-112">indexRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="2075a-112">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="2075a-113">숫자 상태를 형식으로 저장 하는? `LittleEndian`</span><span class="sxs-lookup"><span data-stu-id="2075a-113">The qubit register that stores the number states in `LittleEndian` format.</span></span>
<span data-ttu-id="2075a-114">이 레지스터는 $M-$1 수를 저장할 수 있어야 하며, $ \ket{0\cdots 0} $ 상태에서 초기화 되는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2075a-114">This register must be able to store the number $M-1$, and is assumed to be initialized in the state $\ket{0\cdots 0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2075a-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2075a-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="2075a-116">설명</span><span class="sxs-lookup"><span data-stu-id="2075a-116">Remarks</span></span>

<span data-ttu-id="2075a-117">작업은 adjointable 이지만, `indexRegister` 이 경우에는 첫 번째 기준 상태에서가 균일 한 superposition에 있어야 `nIndices` 합니다.</span><span class="sxs-lookup"><span data-stu-id="2075a-117">The operation is adjointable, but requires that `indexRegister` is in a uniform superposition over the first `nIndices` basis states in that case.</span></span>