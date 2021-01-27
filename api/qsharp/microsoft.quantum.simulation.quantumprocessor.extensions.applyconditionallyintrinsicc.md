---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyIntrinsicC
title: ApplyConditionallyIntrinsicC 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyIntrinsicC
qsharp.summary: ''
ms.openlocfilehash: 64c6693181704d229e36a3e3748258f66e093d96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855741"
---
# <a name="applyconditionallyintrinsicc-operation"></a><span data-ttu-id="436ec-102">ApplyConditionallyIntrinsicC 작업</span><span class="sxs-lookup"><span data-stu-id="436ec-102">ApplyConditionallyIntrinsicC operation</span></span>

<span data-ttu-id="436ec-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="436ec-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="436ec-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="436ec-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyConditionallyIntrinsicC (measurementResults : Result[], resultsValues : Result[], onEqualOp : (Unit => Unit is Ctl), onNonEqualOp : (Unit => Unit is Ctl)) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="436ec-105">입력</span><span class="sxs-lookup"><span data-stu-id="436ec-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="436ec-106">measurementResults: __잘못 <Result> 된__[]</span><span class="sxs-lookup"><span data-stu-id="436ec-106">measurementResults : __invalid<Result>__[]</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="436ec-107">resultsValues: __잘못 <Result> 된__[]</span><span class="sxs-lookup"><span data-stu-id="436ec-107">resultsValues : __invalid<Result>__[]</span></span>




### <a name="onequalop--unit--unit--is-ctl"></a><span data-ttu-id="436ec-108">끄기: [단위](xref:microsoft.quantum.lang-ref.unit) => [단위가](xref:microsoft.quantum.lang-ref.unit)  Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="436ec-108">onEqualOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="onnonequalop--unit--unit--is-ctl"></a><span data-ttu-id="436ec-109">onnonp: [단위](xref:microsoft.quantum.lang-ref.unit) => [단위가](xref:microsoft.quantum.lang-ref.unit)  Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="436ec-109">onNonEqualOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>





## <a name="output--unit"></a><span data-ttu-id="436ec-110">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="436ec-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

