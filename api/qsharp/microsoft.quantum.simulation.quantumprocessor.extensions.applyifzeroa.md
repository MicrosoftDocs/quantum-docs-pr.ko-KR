---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroA
title: ApplyIfZeroA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroA
qsharp.summary: ''
ms.openlocfilehash: 124c5bbabc9e22804734ddbde955312db9655187
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725702"
---
# <a name="applyifzeroa-operation"></a><span data-ttu-id="015bb-102">ApplyIfZeroA 작업</span><span class="sxs-lookup"><span data-stu-id="015bb-102">ApplyIfZeroA operation</span></span>

<span data-ttu-id="015bb-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="015bb-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="015bb-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="015bb-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfZeroA<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Adj), zeroArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="015bb-105">입력</span><span class="sxs-lookup"><span data-stu-id="015bb-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="015bb-106">measurementResult: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="015bb-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit-adj"></a><span data-ttu-id="015bb-107">onResultZeroOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="015bb-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="015bb-108">zeroArg: ' '</span><span class="sxs-lookup"><span data-stu-id="015bb-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="015bb-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="015bb-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="015bb-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="015bb-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="015bb-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="015bb-111">'T</span></span>

