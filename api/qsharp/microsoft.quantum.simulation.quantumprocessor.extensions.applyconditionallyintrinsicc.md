---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyIntrinsicC
title: ApplyConditionallyIntrinsicC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyIntrinsicC
qsharp.summary: ''
ms.openlocfilehash: 54367d89636eb69462040e83cc3c4b6a9f734c0c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720140"
---
# <a name="applyconditionallyintrinsicc-operation"></a><span data-ttu-id="b1c0e-102">ApplyConditionallyIntrinsicC 작업</span><span class="sxs-lookup"><span data-stu-id="b1c0e-102">ApplyConditionallyIntrinsicC operation</span></span>

<span data-ttu-id="b1c0e-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="b1c0e-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="b1c0e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b1c0e-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyConditionallyIntrinsicC (measurementResults : Result[], resultsValues : Result[], onEqualOp : (Unit => Unit is Ctl), onNonEqualOp : (Unit => Unit is Ctl)) : Unit
```


## <a name="input"></a><span data-ttu-id="b1c0e-105">입력</span><span class="sxs-lookup"><span data-stu-id="b1c0e-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="b1c0e-106">measurementResults: __잘못 <Result> 된__ []</span><span class="sxs-lookup"><span data-stu-id="b1c0e-106">measurementResults : __invalid<Result>__ []</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="b1c0e-107">resultsValues: __잘못 <Result> 된__ []</span><span class="sxs-lookup"><span data-stu-id="b1c0e-107">resultsValues : __invalid<Result>__ []</span></span>




### <a name="onequalop--unit--unit-ctl"></a><span data-ttu-id="b1c0e-108">아웃: [유닛](xref:microsoft.quantum.lang-ref.unit) => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="b1c0e-108">onEqualOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>




### <a name="onnonequalop--unit--unit-ctl"></a><span data-ttu-id="b1c0e-109">onnonp: [단위](xref:microsoft.quantum.lang-ref.unit) => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="b1c0e-109">onNonEqualOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>





## <a name="output--unit"></a><span data-ttu-id="b1c0e-110">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b1c0e-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

