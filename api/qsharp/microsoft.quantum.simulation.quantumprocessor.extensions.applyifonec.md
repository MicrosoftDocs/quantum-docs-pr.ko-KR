---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfOneC
title: ApplyIfOneC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfOneC
qsharp.summary: ''
ms.openlocfilehash: 8456201d4ed137f3d84013f3b5170b52b27e66c5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725387"
---
# <a name="applyifonec-operation"></a><span data-ttu-id="635ea-102">ApplyIfOneC 작업</span><span class="sxs-lookup"><span data-stu-id="635ea-102">ApplyIfOneC operation</span></span>

<span data-ttu-id="635ea-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="635ea-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="635ea-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="635ea-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfOneC<'T> (measurementResult : Result, (onResultOneOp : ('T => Unit is Ctl), oneArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="635ea-105">입력</span><span class="sxs-lookup"><span data-stu-id="635ea-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="635ea-106">measurementResult: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="635ea-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultoneop--t--unit-ctl"></a><span data-ttu-id="635ea-107">onResultOneOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="635ea-107">onResultOneOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>




### <a name="onearg--t"></a><span data-ttu-id="635ea-108">oneArg: ' t</span><span class="sxs-lookup"><span data-stu-id="635ea-108">oneArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="635ea-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="635ea-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="635ea-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="635ea-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="635ea-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="635ea-111">'T</span></span>

