---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfOne
title: ApplyIfOne 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfOne
qsharp.summary: ''
ms.openlocfilehash: fd5ee65615e4910d60db83cb8ec4201cfff9035d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855585"
---
# <a name="applyifone-operation"></a><span data-ttu-id="4a6ca-102">ApplyIfOne 작업</span><span class="sxs-lookup"><span data-stu-id="4a6ca-102">ApplyIfOne operation</span></span>

<span data-ttu-id="4a6ca-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="4a6ca-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="4a6ca-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="4a6ca-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfOne<'T> (measurementResult : Result, (onResultOneOp : ('T => Unit), oneArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="4a6ca-105">입력</span><span class="sxs-lookup"><span data-stu-id="4a6ca-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="4a6ca-106">measurementResult: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="4a6ca-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultoneop--t--unit"></a><span data-ttu-id="4a6ca-107">onResultOneOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4a6ca-107">onResultOneOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="onearg--t"></a><span data-ttu-id="4a6ca-108">oneArg: ' t</span><span class="sxs-lookup"><span data-stu-id="4a6ca-108">oneArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="4a6ca-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4a6ca-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4a6ca-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4a6ca-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4a6ca-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="4a6ca-111">'T</span></span>

