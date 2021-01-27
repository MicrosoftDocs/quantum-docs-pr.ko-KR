---
uid: Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA
title: DecomposedIntoTimeStepsCA 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DecomposedIntoTimeStepsCA
qsharp.summary: Returns an operation implementing the Trotter–Suzuki integrator for a given operation.
ms.openlocfilehash: e82df36d2e4f3767a152d5c92d7b1897c744a2ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840681"
---
# <a name="decomposedintotimestepsca-function"></a><span data-ttu-id="49c95-102">DecomposedIntoTimeStepsCA 함수</span><span class="sxs-lookup"><span data-stu-id="49c95-102">DecomposedIntoTimeStepsCA function</span></span>

<span data-ttu-id="49c95-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="49c95-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="49c95-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="49c95-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="49c95-105">지정 된 작업에 대해 Trotter – Suzuki 인티그레이터를 구현 하는 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c95-105">Returns an operation implementing the Trotter–Suzuki integrator for a given operation.</span></span>

```qsharp
function DecomposedIntoTimeStepsCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), trotterOrder : Int) : ((Double, 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="49c95-106">입력</span><span class="sxs-lookup"><span data-stu-id="49c95-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="49c95-107">n 단계: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="49c95-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="49c95-108">시간 단계로 분해할 작업 수입니다.</span><span class="sxs-lookup"><span data-stu-id="49c95-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="49c95-109">op: ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="49c95-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="49c95-110">분해를 위해 인덱스 입력 (형식 `Int` ) 및 시간 입력 (형식)을 허용 하는 작업입니다 `Double` .</span><span class="sxs-lookup"><span data-stu-id="49c95-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) for decomposition.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="49c95-111">trotterOrder: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="49c95-111">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="49c95-112">사용할 Trotter – Suzuki 통합자의 순서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c95-112">Selects the order of the Trotter–Suzuki integrator to be used.</span></span>
<span data-ttu-id="49c95-113">주문 1과 주문 2, 4, 6,... 는 현재 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49c95-113">Order 1 and even orders 2, 4, 6,... are currently supported.</span></span>



## <a name="output--doublet--unit--is-adj--ctl"></a><span data-ttu-id="49c95-114">출력: ([Double](xref:microsoft.quantum.lang-ref.double), t) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="49c95-114">Output : ([Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="49c95-115">Trotter – Suzuki 인티그레이터를 구현 하는 단일를 반환 합니다. 여기서 첫 번째 매개 변수는 `Double` 통합 단계 크기이 고, 두 번째 매개 변수는 처리 대상인 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="49c95-115">Returns a unitary implementing the Trotter–Suzuki integrator, where the first parameter `Double` is the integration step size, and the second parameter is the target acted upon.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="49c95-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="49c95-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="49c95-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="49c95-117">'T</span></span>

<span data-ttu-id="49c95-118">각 시간 단계가 작동 해야 하는 형식입니다. 일반적으로 `Qubit[]` 또는 `Qubit` 입니다.</span><span class="sxs-lookup"><span data-stu-id="49c95-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>

## <a name="remarks"></a><span data-ttu-id="49c95-119">설명</span><span class="sxs-lookup"><span data-stu-id="49c95-119">Remarks</span></span>

<span data-ttu-id="49c95-120">이 함수는와 같이 호출 될 때 `order` `1` 가장 낮은 Trotter – Suzuki 인티그레이터 $ $ \begin{align} S_1 (\lambda) = \ prod_ {j = 1} ^ {m} e ^ {H_j \lambda}에서 시뮬레이션할 수 있는 작업을 반환 합니다. \end{align} $ $ where [0508139](https://arxiv.org/abs/quant-ph/0508139) 표기법을 따르고 $ \lambda $는 진화 시간 (반환 된 작업의 첫 번째 입력으로 표시 됨)이 될 수 있습니다. 그리고 $ \{ H_j \} _ {j = 1} ^ {m} $은 `op(j, lambda, _)` 단일 연산자 $e ^ {H_j \Lambda} $에서 시뮬레이션 되는 (Hermitian) 동적 생성기 집합 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c95-120">When called with `order` equal to `1`, this function returns an operation that can be simulated by the lowest-order Trotter–Suzuki integrator $$ \begin{align} S_1(\lambda) = \prod_{j = 1}^{m} e^{H_j \lambda}, \end{align} $$ where we have followed the notation of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139) and let $\lambda$ be the evolution time (represented by the first input of the returned operation), and have let $\{H_j\}_{j = 1}^{m}$ be the set of (skew-Hermitian) dynamical generators being integrated such that `op(j, lambda, _)` is simulated by the unitary operator $e^{H_j \lambda}$.</span></span>

<span data-ttu-id="49c95-121">마찬가지로의는 `order` `2` 두 번째 순서 대칭 Trotter – Suzuki 인티그레이터 $ $ \begin{align} S_2 (\lambda) = \ prod_ {j = 1} ^ {m} e ^ {H_k \lambda} \ prod_ {j ' = m} ^ {1} e ^ {H_ {j '} \lambda/2}를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c95-121">Similarly, an `order` of `2` returns the second-order symmetric Trotter–Suzuki integrator $$ \begin{align} S_2(\lambda) = \prod_{j = 1}^{m} e^{H_k \lambda / 2} \prod_{j' = m}^{1} e^{H_{j'} \lambda / 2}.</span></span>
<span data-ttu-id="49c95-122">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="49c95-122">\end{align} $$</span></span>

<span data-ttu-id="49c95-123">의 짝수 값은 보다 높은 값을 `order` 사용 하 여 [](https://arxiv.org/abs/quant-ph/0508139)구현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49c95-123">Higher even values of `order` are implemented using the recursive construction of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span></span>

## <a name="references"></a><span data-ttu-id="49c95-124">참조</span><span class="sxs-lookup"><span data-stu-id="49c95-124">References</span></span>

- [<span data-ttu-id="49c95-125">*D. Berry, G. Ahokas, Cleve, b. Sanders*</span><span class="sxs-lookup"><span data-stu-id="49c95-125"> *D. W. Berry, G. Ahokas, R. Cleve, B. C. Sanders* </span></span>](https://arxiv.org/abs/quant-ph/0508139)