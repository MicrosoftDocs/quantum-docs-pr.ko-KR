---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: ApplyBlockEncodingByLCU 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: 1575b93b6c3242e1dffafb330c44cc017a72a8b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722125"
---
# <a name="applyblockencodingbylcu-operation"></a><span data-ttu-id="cbfe6-102">ApplyBlockEncodingByLCU 작업</span><span class="sxs-lookup"><span data-stu-id="cbfe6-102">ApplyBlockEncodingByLCU operation</span></span>

<span data-ttu-id="cbfe6-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="cbfe6-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="cbfe6-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cbfe6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cbfe6-105">`BlockEncodingByLCU`의 구현입니다.</span><span class="sxs-lookup"><span data-stu-id="cbfe6-105">Implementation of `BlockEncodingByLCU`.</span></span>

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit
```


## <a name="input"></a><span data-ttu-id="cbfe6-106">입력</span><span class="sxs-lookup"><span data-stu-id="cbfe6-106">Input</span></span>

### <a name="statepreparation--t--unit-adj--ctl"></a><span data-ttu-id="cbfe6-107">statePreparation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="cbfe6-107">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="selector--ts--unit-adj--ctl"></a><span data-ttu-id="cbfe6-108">selector: (' ' ') => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="cbfe6-108">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="auxiliary--t"></a><span data-ttu-id="cbfe6-109">보조: ' '</span><span class="sxs-lookup"><span data-stu-id="cbfe6-109">auxiliary : 'T</span></span>




### <a name="system--s"></a><span data-ttu-id="cbfe6-110">시스템:</span><span class="sxs-lookup"><span data-stu-id="cbfe6-110">system : 'S</span></span>





## <a name="output--unit"></a><span data-ttu-id="cbfe6-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cbfe6-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="cbfe6-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cbfe6-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cbfe6-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="cbfe6-113">'T</span></span>


### <a name="s"></a><span data-ttu-id="cbfe6-114">큐브의</span><span class="sxs-lookup"><span data-stu-id="cbfe6-114">'S</span></span>

