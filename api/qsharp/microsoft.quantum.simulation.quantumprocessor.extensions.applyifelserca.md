---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseRCA
title: ApplyIfElseRCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseRCA
qsharp.summary: ''
ms.openlocfilehash: fb2f7ded44708a93d97d7041bf15be2c8c48990a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719893"
---
# <a name="applyifelserca-operation"></a><span data-ttu-id="fa5fa-102">ApplyIfElseRCA 작업</span><span class="sxs-lookup"><span data-stu-id="fa5fa-102">ApplyIfElseRCA operation</span></span>

<span data-ttu-id="fa5fa-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="fa5fa-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="fa5fa-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fa5fa-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfElseRCA<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Adj + Ctl), zeroArg : 'T), (onResultOneOp : ('U => Unit is Adj + Ctl), oneArg : 'U)) : Unit
```


## <a name="input"></a><span data-ttu-id="fa5fa-105">입력</span><span class="sxs-lookup"><span data-stu-id="fa5fa-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="fa5fa-106">measurementResult: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="fa5fa-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit-adj--ctl"></a><span data-ttu-id="fa5fa-107">onResultZeroOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="fa5fa-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="fa5fa-108">zeroArg: ' '</span><span class="sxs-lookup"><span data-stu-id="fa5fa-108">zeroArg : 'T</span></span>




### <a name="onresultoneop--u--unit-adj--ctl"></a><span data-ttu-id="fa5fa-109">onResultOneOp: ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="fa5fa-109">onResultOneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="onearg--u"></a><span data-ttu-id="fa5fa-110">oneArg: ' U</span><span class="sxs-lookup"><span data-stu-id="fa5fa-110">oneArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="fa5fa-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fa5fa-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="fa5fa-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="fa5fa-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fa5fa-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="fa5fa-113">'T</span></span>


### <a name="u"></a><span data-ttu-id="fa5fa-114">' U</span><span class="sxs-lookup"><span data-stu-id="fa5fa-114">'U</span></span>

