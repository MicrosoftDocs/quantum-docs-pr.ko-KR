---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseR
title: ApplyIfElseR 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseR
qsharp.summary: ''
ms.openlocfilehash: 9e391b61aa4d22ad02bf657a866f959d35b6628f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192675"
---
# <a name="applyifelser-operation"></a><span data-ttu-id="0861b-102">ApplyIfElseR 작업</span><span class="sxs-lookup"><span data-stu-id="0861b-102">ApplyIfElseR operation</span></span>

<span data-ttu-id="0861b-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="0861b-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="0861b-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="0861b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfElseR<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit), zeroArg : 'T), (onResultOneOp : ('U => Unit), oneArg : 'U)) : Unit
```


## <a name="input"></a><span data-ttu-id="0861b-105">입력</span><span class="sxs-lookup"><span data-stu-id="0861b-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="0861b-106">measurementResult: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="0861b-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit"></a><span data-ttu-id="0861b-107">onResultZeroOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0861b-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="zeroarg--t"></a><span data-ttu-id="0861b-108">zeroArg: ' '</span><span class="sxs-lookup"><span data-stu-id="0861b-108">zeroArg : 'T</span></span>




### <a name="onresultoneop--u--unit"></a><span data-ttu-id="0861b-109">onResultOneOp: ' U => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0861b-109">onResultOneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="onearg--u"></a><span data-ttu-id="0861b-110">oneArg: ' U</span><span class="sxs-lookup"><span data-stu-id="0861b-110">oneArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="0861b-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0861b-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0861b-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0861b-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0861b-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="0861b-113">'T</span></span>


### <a name="u"></a><span data-ttu-id="0861b-114">' U</span><span class="sxs-lookup"><span data-stu-id="0861b-114">'U</span></span>

