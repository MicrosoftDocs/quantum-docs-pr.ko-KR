---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseRA
title: ApplyIfElseRA operation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseRA
qsharp.summary: ''
ms.openlocfilehash: 48819440bf0d55f9a44ca8f76927692d48925e50
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192709"
---
# <a name="applyifelsera-operation"></a><span data-ttu-id="d2364-102">ApplyIfElseRA operation</span><span class="sxs-lookup"><span data-stu-id="d2364-102">ApplyIfElseRA operation</span></span>

<span data-ttu-id="d2364-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="d2364-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="d2364-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="d2364-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfElseRA<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Adj), zeroArg : 'T), (onResultOneOp : ('U => Unit is Adj), oneArg : 'U)) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="d2364-105">입력</span><span class="sxs-lookup"><span data-stu-id="d2364-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="d2364-106">measurementResult: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="d2364-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit--is-adj"></a><span data-ttu-id="d2364-107">onResultZeroOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="d2364-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="d2364-108">zeroArg: ' '</span><span class="sxs-lookup"><span data-stu-id="d2364-108">zeroArg : 'T</span></span>




### <a name="onresultoneop--u--unit--is-adj"></a><span data-ttu-id="d2364-109">onResultOneOp: ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="d2364-109">onResultOneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="onearg--u"></a><span data-ttu-id="d2364-110">oneArg: ' U</span><span class="sxs-lookup"><span data-stu-id="d2364-110">oneArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="d2364-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d2364-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d2364-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d2364-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d2364-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="d2364-113">'T</span></span>


### <a name="u"></a><span data-ttu-id="d2364-114">' U</span><span class="sxs-lookup"><span data-stu-id="d2364-114">'U</span></span>

