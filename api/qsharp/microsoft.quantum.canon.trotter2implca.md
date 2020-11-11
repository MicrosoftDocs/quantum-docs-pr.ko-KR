---
uid: Microsoft.Quantum.Canon.Trotter2ImplCA
title: Trotter2ImplCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter2ImplCA
qsharp.summary: Implementation of the second-order Trotter–Suzuki integrator.
ms.openlocfilehash: 98ba4db45fa7b7e8f442ba166929142aac4fa5a4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715310"
---
# <a name="trotter2implca-operation"></a><span data-ttu-id="69c0b-102">Trotter2ImplCA 작업</span><span class="sxs-lookup"><span data-stu-id="69c0b-102">Trotter2ImplCA operation</span></span>

<span data-ttu-id="69c0b-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="69c0b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="69c0b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="69c0b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="69c0b-105">두 번째 주문 Trotter – Suzuki 통합자의 구현입니다.</span><span class="sxs-lookup"><span data-stu-id="69c0b-105">Implementation of the second-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation Trotter2ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="69c0b-106">입력</span><span class="sxs-lookup"><span data-stu-id="69c0b-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="69c0b-107">n 단계: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="69c0b-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="69c0b-108">시간 단계로 분해할 작업 수입니다.</span><span class="sxs-lookup"><span data-stu-id="69c0b-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit-adj--ctl"></a><span data-ttu-id="69c0b-109">op: ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="69c0b-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="69c0b-110">분해를 위해 인덱스 입력 (형식 `Int` ) 및 시간 입력 (형식) 및 퀀텀 레지스터 (형식)를 허용 하는 작업 `Double` `'T` 입니다.</span><span class="sxs-lookup"><span data-stu-id="69c0b-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="69c0b-111">Stsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="69c0b-111">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="69c0b-112">시뮬레이션의 각 단계 크기에 대 한 승수입니다.</span><span class="sxs-lookup"><span data-stu-id="69c0b-112">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="69c0b-113">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="69c0b-113">target : 'T</span></span>

<span data-ttu-id="69c0b-114">작업이 작동 하는 퀀텀 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="69c0b-114">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="69c0b-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="69c0b-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="69c0b-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="69c0b-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="69c0b-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="69c0b-117">'T</span></span>

<span data-ttu-id="69c0b-118">각 시간 단계가 작동 해야 하는 형식입니다. 일반적으로 `Qubit[]` 또는 `Qubit` 입니다.</span><span class="sxs-lookup"><span data-stu-id="69c0b-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>