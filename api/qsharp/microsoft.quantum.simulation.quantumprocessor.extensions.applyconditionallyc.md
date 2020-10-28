---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyC
title: ApplyConditionallyC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyC
qsharp.summary: ''
ms.openlocfilehash: fc1cf50b7befd40cf20720032329438715a9b856
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720188"
---
# <a name="applyconditionallyc-operation"></a><span data-ttu-id="47ed3-102">ApplyConditionallyC 작업</span><span class="sxs-lookup"><span data-stu-id="47ed3-102">ApplyConditionallyC operation</span></span>

<span data-ttu-id="47ed3-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="47ed3-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="47ed3-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="47ed3-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyConditionallyC<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit is Ctl), equalArg : 'T), (onNonEqualOp : ('U => Unit is Ctl), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a><span data-ttu-id="47ed3-105">입력</span><span class="sxs-lookup"><span data-stu-id="47ed3-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="47ed3-106">measurementResults: __잘못 <Result> 된__ []</span><span class="sxs-lookup"><span data-stu-id="47ed3-106">measurementResults : __invalid<Result>__ []</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="47ed3-107">resultsValues: __잘못 <Result> 된__ []</span><span class="sxs-lookup"><span data-stu-id="47ed3-107">resultsValues : __invalid<Result>__ []</span></span>




### <a name="onequalop--t--unit-ctl"></a><span data-ttu-id="47ed3-108">p: t => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="47ed3-108">onEqualOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>




### <a name="equalarg--t"></a><span data-ttu-id="47ed3-109">equalArg: ' '</span><span class="sxs-lookup"><span data-stu-id="47ed3-109">equalArg : 'T</span></span>




### <a name="onnonequalop--u--unit-ctl"></a><span data-ttu-id="47ed3-110">Onnonp: ' U => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="47ed3-110">onNonEqualOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>




### <a name="nonequalarg--u"></a><span data-ttu-id="47ed3-111">nonEqualArg: ' U</span><span class="sxs-lookup"><span data-stu-id="47ed3-111">nonEqualArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="47ed3-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="47ed3-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="47ed3-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="47ed3-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="47ed3-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="47ed3-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="47ed3-115">' U</span><span class="sxs-lookup"><span data-stu-id="47ed3-115">'U</span></span>

