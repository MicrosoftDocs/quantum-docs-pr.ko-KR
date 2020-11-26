---
uid: Microsoft.Quantum.Canon.TrotterArbitraryImplCA
title: TrotterArbitraryImplCA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterArbitraryImplCA
qsharp.summary: Recursive implementation of even-order Trotter–Suzuki integrator.
ms.openlocfilehash: 2abfbb9d51a98d8ede1b0835875a3771ffda0691
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204728"
---
# <a name="trotterarbitraryimplca-operation"></a><span data-ttu-id="16577-102">TrotterArbitraryImplCA 작업</span><span class="sxs-lookup"><span data-stu-id="16577-102">TrotterArbitraryImplCA operation</span></span>

<span data-ttu-id="16577-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="16577-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="16577-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="16577-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="16577-105">짝수 order Trotter – Suzuki 통합자의 재귀 구현입니다.</span><span class="sxs-lookup"><span data-stu-id="16577-105">Recursive implementation of even-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation TrotterArbitraryImplCA<'T> (order : Int, (nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="16577-106">입력</span><span class="sxs-lookup"><span data-stu-id="16577-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="16577-107">순서: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="16577-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="16577-108">Trotter-Suzuki 통합자의 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="16577-108">Order of Trotter-Suzuki integrator.</span></span>


### <a name="nsteps--int"></a><span data-ttu-id="16577-109">n 단계: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="16577-109">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="16577-110">시간 단계로 분해할 작업 수입니다.</span><span class="sxs-lookup"><span data-stu-id="16577-110">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="16577-111">op: ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="16577-111">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="16577-112">분해를 위해 인덱스 입력 (형식 `Int` ) 및 시간 입력 (형식) 및 퀀텀 레지스터 (형식)를 허용 하는 작업 `Double` `'T` 입니다.</span><span class="sxs-lookup"><span data-stu-id="16577-112">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="16577-113">Stsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="16577-113">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="16577-114">시뮬레이션의 각 단계 크기에 대 한 승수입니다.</span><span class="sxs-lookup"><span data-stu-id="16577-114">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="16577-115">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="16577-115">target : 'T</span></span>

<span data-ttu-id="16577-116">작업이 작동 하는 퀀텀 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="16577-116">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="16577-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="16577-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="16577-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="16577-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="16577-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="16577-119">'T</span></span>

<span data-ttu-id="16577-120">각 시간 단계가 작동 해야 하는 형식입니다. 일반적으로 `Qubit[]` 또는 `Qubit` 입니다.</span><span class="sxs-lookup"><span data-stu-id="16577-120">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>