---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfOneCA
title: ApplyIfOneCA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfOneCA
qsharp.summary: ''
ms.openlocfilehash: e997cf4b20fdd2c52285191b732297ca99886c22
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230942"
---
# <a name="applyifoneca-operation"></a><span data-ttu-id="206d5-102">ApplyIfOneCA 작업</span><span class="sxs-lookup"><span data-stu-id="206d5-102">ApplyIfOneCA operation</span></span>

<span data-ttu-id="206d5-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="206d5-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="206d5-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="206d5-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfOneCA<'T> (measurementResult : Result, (onResultOneOp : ('T => Unit is Ctl + Adj), oneArg : 'T)) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="206d5-105">입력</span><span class="sxs-lookup"><span data-stu-id="206d5-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="206d5-106">measurementResult: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="206d5-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultoneop--t--unit--is-adj--ctl"></a><span data-ttu-id="206d5-107">onResultOneOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="206d5-107">onResultOneOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="onearg--t"></a><span data-ttu-id="206d5-108">oneArg: ' t</span><span class="sxs-lookup"><span data-stu-id="206d5-108">oneArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="206d5-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="206d5-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="206d5-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="206d5-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="206d5-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="206d5-111">'T</span></span>

