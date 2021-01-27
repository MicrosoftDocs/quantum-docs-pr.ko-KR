---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseRC
title: ApplyIfElseRC 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseRC
qsharp.summary: ''
ms.openlocfilehash: 97536f2071918bec7129d8157e8750a5c310767f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855638"
---
# <a name="applyifelserc-operation"></a><span data-ttu-id="b09ae-102">ApplyIfElseRC 작업</span><span class="sxs-lookup"><span data-stu-id="b09ae-102">ApplyIfElseRC operation</span></span>

<span data-ttu-id="b09ae-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="b09ae-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="b09ae-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="b09ae-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfElseRC<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl), zeroArg : 'T), (onResultOneOp : ('U => Unit is Ctl), oneArg : 'U)) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="b09ae-105">입력</span><span class="sxs-lookup"><span data-stu-id="b09ae-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="b09ae-106">measurementResult: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="b09ae-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit--is-ctl"></a><span data-ttu-id="b09ae-107">onResultZeroOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="b09ae-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="b09ae-108">zeroArg: ' '</span><span class="sxs-lookup"><span data-stu-id="b09ae-108">zeroArg : 'T</span></span>




### <a name="onresultoneop--u--unit--is-ctl"></a><span data-ttu-id="b09ae-109">onResultOneOp: ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="b09ae-109">onResultOneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="onearg--u"></a><span data-ttu-id="b09ae-110">oneArg: ' U</span><span class="sxs-lookup"><span data-stu-id="b09ae-110">oneArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="b09ae-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b09ae-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b09ae-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b09ae-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b09ae-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="b09ae-113">'T</span></span>


### <a name="u"></a><span data-ttu-id="b09ae-114">' U</span><span class="sxs-lookup"><span data-stu-id="b09ae-114">'U</span></span>

