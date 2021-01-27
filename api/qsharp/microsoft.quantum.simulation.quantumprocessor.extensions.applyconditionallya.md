---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyA
title: ApplyConditionallyA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyA
qsharp.summary: ''
ms.openlocfilehash: 18ea79e363c28d4fa7aacb69d53a43f6ce39df36
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847866"
---
# <a name="applyconditionallya-operation"></a><span data-ttu-id="f302c-102">ApplyConditionallyA 작업</span><span class="sxs-lookup"><span data-stu-id="f302c-102">ApplyConditionallyA operation</span></span>

<span data-ttu-id="f302c-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="f302c-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="f302c-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="f302c-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyConditionallyA<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit is Adj), equalArg : 'T), (onNonEqualOp : ('U => Unit is Adj), nonEqualArg : 'U)) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="f302c-105">입력</span><span class="sxs-lookup"><span data-stu-id="f302c-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="f302c-106">measurementResults: __잘못 <Result> 된__[]</span><span class="sxs-lookup"><span data-stu-id="f302c-106">measurementResults : __invalid<Result>__[]</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="f302c-107">resultsValues: __잘못 <Result> 된__[]</span><span class="sxs-lookup"><span data-stu-id="f302c-107">resultsValues : __invalid<Result>__[]</span></span>




### <a name="onequalop--t--unit--is-adj"></a><span data-ttu-id="f302c-108">OnAdj p: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  은입니다.</span><span class="sxs-lookup"><span data-stu-id="f302c-108">onEqualOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="equalarg--t"></a><span data-ttu-id="f302c-109">equalArg: ' '</span><span class="sxs-lookup"><span data-stu-id="f302c-109">equalArg : 'T</span></span>




### <a name="onnonequalop--u--unit--is-adj"></a><span data-ttu-id="f302c-110">Onnonp: ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="f302c-110">onNonEqualOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="nonequalarg--u"></a><span data-ttu-id="f302c-111">nonEqualArg: ' U</span><span class="sxs-lookup"><span data-stu-id="f302c-111">nonEqualArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="f302c-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f302c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f302c-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f302c-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f302c-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="f302c-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="f302c-115">' U</span><span class="sxs-lookup"><span data-stu-id="f302c-115">'U</span></span>

