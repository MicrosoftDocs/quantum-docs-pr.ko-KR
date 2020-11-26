---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyIntrinsicCA
title: ApplyConditionallyIntrinsicCA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyIntrinsicCA
qsharp.summary: ''
ms.openlocfilehash: 2dd7a9b6e281c62470defa64685dc58872694468
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230194"
---
# <a name="applyconditionallyintrinsicca-operation"></a><span data-ttu-id="91b26-102">ApplyConditionallyIntrinsicCA 작업</span><span class="sxs-lookup"><span data-stu-id="91b26-102">ApplyConditionallyIntrinsicCA operation</span></span>

<span data-ttu-id="91b26-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="91b26-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="91b26-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="91b26-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyConditionallyIntrinsicCA (measurementResults : Result[], resultsValues : Result[], onEqualOp : (Unit => Unit is Ctl + Adj), onNonEqualOp : (Unit => Unit is Ctl + Adj)) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="91b26-105">입력</span><span class="sxs-lookup"><span data-stu-id="91b26-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="91b26-106">measurementResults: __잘못 <Result> 된__[]</span><span class="sxs-lookup"><span data-stu-id="91b26-106">measurementResults : __invalid<Result>__[]</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="91b26-107">resultsValues: __잘못 <Result> 된__[]</span><span class="sxs-lookup"><span data-stu-id="91b26-107">resultsValues : __invalid<Result>__[]</span></span>




### <a name="onequalop--unit--unit--is-adj--ctl"></a><span data-ttu-id="91b26-108">onAdj p: [unit](xref:microsoft.quantum.lang-ref.unit) => [unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl + Ctl</span><span class="sxs-lookup"><span data-stu-id="91b26-108">onEqualOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="onnonequalop--unit--unit--is-adj--ctl"></a><span data-ttu-id="91b26-109">onnonp: [unit](xref:microsoft.quantum.lang-ref.unit) => [unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="91b26-109">onNonEqualOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>





## <a name="output--unit"></a><span data-ttu-id="91b26-110">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="91b26-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

