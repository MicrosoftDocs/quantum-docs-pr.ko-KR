---
uid: Microsoft.Quantum.Canon.TrotterArbitraryImplCA
title: TrotterArbitraryImplCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterArbitraryImplCA
qsharp.summary: Recursive implementation of even-order Trotter–Suzuki integrator.
ms.openlocfilehash: 1c094d09ac8bdd71a59ef57d8715a6f90f18efc6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715289"
---
# <a name="trotterarbitraryimplca-operation"></a><span data-ttu-id="13194-102">TrotterArbitraryImplCA 작업</span><span class="sxs-lookup"><span data-stu-id="13194-102">TrotterArbitraryImplCA operation</span></span>

<span data-ttu-id="13194-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="13194-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="13194-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="13194-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="13194-105">짝수 order Trotter – Suzuki 통합자의 재귀 구현입니다.</span><span class="sxs-lookup"><span data-stu-id="13194-105">Recursive implementation of even-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation TrotterArbitraryImplCA<'T> (order : Int, (nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="13194-106">입력</span><span class="sxs-lookup"><span data-stu-id="13194-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="13194-107">순서: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="13194-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="13194-108">Trotter-Suzuki 통합자의 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="13194-108">Order of Trotter-Suzuki integrator.</span></span>


### <a name="nsteps--int"></a><span data-ttu-id="13194-109">n 단계: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="13194-109">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="13194-110">시간 단계로 분해할 작업 수입니다.</span><span class="sxs-lookup"><span data-stu-id="13194-110">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit-adj--ctl"></a><span data-ttu-id="13194-111">op: ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="13194-111">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="13194-112">분해를 위해 인덱스 입력 (형식 `Int` ) 및 시간 입력 (형식) 및 퀀텀 레지스터 (형식)를 허용 하는 작업 `Double` `'T` 입니다.</span><span class="sxs-lookup"><span data-stu-id="13194-112">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="13194-113">Stsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="13194-113">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="13194-114">시뮬레이션의 각 단계 크기에 대 한 승수입니다.</span><span class="sxs-lookup"><span data-stu-id="13194-114">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="13194-115">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="13194-115">target : 'T</span></span>

<span data-ttu-id="13194-116">작업이 작동 하는 퀀텀 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="13194-116">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="13194-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="13194-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="13194-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="13194-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="13194-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="13194-119">'T</span></span>

<span data-ttu-id="13194-120">각 시간 단계가 작동 해야 하는 형식입니다. 일반적으로 `Qubit[]` 또는 `Qubit` 입니다.</span><span class="sxs-lookup"><span data-stu-id="13194-120">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>