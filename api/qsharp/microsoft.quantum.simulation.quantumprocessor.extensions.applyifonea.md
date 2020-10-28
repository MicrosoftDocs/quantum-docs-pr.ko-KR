---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfOneA
title: ApplyIfOneA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfOneA
qsharp.summary: ''
ms.openlocfilehash: c18133403a545f7dc7b9f213a42ed09cd194f2d7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725394"
---
# <a name="applyifonea-operation"></a><span data-ttu-id="a63b1-102">ApplyIfOneA 작업</span><span class="sxs-lookup"><span data-stu-id="a63b1-102">ApplyIfOneA operation</span></span>

<span data-ttu-id="a63b1-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="a63b1-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="a63b1-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a63b1-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfOneA<'T> (measurementResult : Result, (onResultOneOp : ('T => Unit is Adj), oneArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="a63b1-105">입력</span><span class="sxs-lookup"><span data-stu-id="a63b1-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="a63b1-106">measurementResult: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="a63b1-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultoneop--t--unit-adj"></a><span data-ttu-id="a63b1-107">onResultOneOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="a63b1-107">onResultOneOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>




### <a name="onearg--t"></a><span data-ttu-id="a63b1-108">oneArg: ' t</span><span class="sxs-lookup"><span data-stu-id="a63b1-108">oneArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="a63b1-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a63b1-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a63b1-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a63b1-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a63b1-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="a63b1-111">'T</span></span>

