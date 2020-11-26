---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: ApplyBlockEncodingByLCU 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: 8ce6eb16b1dc5a83dd3a9559592c20d6b7b999b6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225485"
---
# <a name="applyblockencodingbylcu-operation"></a><span data-ttu-id="116b0-102">ApplyBlockEncodingByLCU 작업</span><span class="sxs-lookup"><span data-stu-id="116b0-102">ApplyBlockEncodingByLCU operation</span></span>

<span data-ttu-id="116b0-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="116b0-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="116b0-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="116b0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="116b0-105">`BlockEncodingByLCU`의 구현입니다.</span><span class="sxs-lookup"><span data-stu-id="116b0-105">Implementation of `BlockEncodingByLCU`.</span></span>

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="116b0-106">입력</span><span class="sxs-lookup"><span data-stu-id="116b0-106">Input</span></span>

### <a name="statepreparation--t--unit--is-adj--ctl"></a><span data-ttu-id="116b0-107">statePreparation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="116b0-107">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="selector--ts--unit--is-adj--ctl"></a><span data-ttu-id="116b0-108">selector: (' ' ') => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="116b0-108">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="auxiliary--t"></a><span data-ttu-id="116b0-109">보조: ' '</span><span class="sxs-lookup"><span data-stu-id="116b0-109">auxiliary : 'T</span></span>




### <a name="system--s"></a><span data-ttu-id="116b0-110">시스템:</span><span class="sxs-lookup"><span data-stu-id="116b0-110">system : 'S</span></span>





## <a name="output--unit"></a><span data-ttu-id="116b0-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="116b0-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="116b0-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="116b0-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="116b0-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="116b0-113">'T</span></span>


### <a name="s"></a><span data-ttu-id="116b0-114">큐브의</span><span class="sxs-lookup"><span data-stu-id="116b0-114">'S</span></span>

