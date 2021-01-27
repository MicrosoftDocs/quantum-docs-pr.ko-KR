---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: ApplyBlockEncodingByLCU 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: a9a9e3bbd598453719f49f78392f3a92c9401b36
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852820"
---
# <a name="applyblockencodingbylcu-operation"></a><span data-ttu-id="41826-102">ApplyBlockEncodingByLCU 작업</span><span class="sxs-lookup"><span data-stu-id="41826-102">ApplyBlockEncodingByLCU operation</span></span>

<span data-ttu-id="41826-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="41826-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="41826-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="41826-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="41826-105">`BlockEncodingByLCU`의 구현입니다.</span><span class="sxs-lookup"><span data-stu-id="41826-105">Implementation of `BlockEncodingByLCU`.</span></span>

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="41826-106">입력</span><span class="sxs-lookup"><span data-stu-id="41826-106">Input</span></span>

### <a name="statepreparation--t--unit--is-adj--ctl"></a><span data-ttu-id="41826-107">statePreparation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="41826-107">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="selector--ts--unit--is-adj--ctl"></a><span data-ttu-id="41826-108">selector: (' ' ') => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="41826-108">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="auxiliary--t"></a><span data-ttu-id="41826-109">보조: ' '</span><span class="sxs-lookup"><span data-stu-id="41826-109">auxiliary : 'T</span></span>




### <a name="system--s"></a><span data-ttu-id="41826-110">시스템:</span><span class="sxs-lookup"><span data-stu-id="41826-110">system : 'S</span></span>





## <a name="output--unit"></a><span data-ttu-id="41826-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="41826-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="41826-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="41826-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="41826-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="41826-113">'T</span></span>


### <a name="s"></a><span data-ttu-id="41826-114">큐브의</span><span class="sxs-lookup"><span data-stu-id="41826-114">'S</span></span>

