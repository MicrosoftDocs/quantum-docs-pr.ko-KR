---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroC
title: ApplyIfZeroC 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroC
qsharp.summary: ''
ms.openlocfilehash: 9a73ea9ec607bec89c996c096b235a72185b453d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230840"
---
# <a name="applyifzeroc-operation"></a><span data-ttu-id="08037-102">ApplyIfZeroC 작업</span><span class="sxs-lookup"><span data-stu-id="08037-102">ApplyIfZeroC operation</span></span>

<span data-ttu-id="08037-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="08037-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="08037-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="08037-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfZeroC<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl), zeroArg : 'T)) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="08037-105">입력</span><span class="sxs-lookup"><span data-stu-id="08037-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="08037-106">measurementResult: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="08037-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit--is-ctl"></a><span data-ttu-id="08037-107">onResultZeroOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="08037-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="08037-108">zeroArg: ' '</span><span class="sxs-lookup"><span data-stu-id="08037-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="08037-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="08037-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="08037-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="08037-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="08037-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="08037-111">'T</span></span>

