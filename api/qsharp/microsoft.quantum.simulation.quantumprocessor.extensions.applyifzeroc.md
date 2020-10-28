---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroC
title: ApplyIfZeroC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroC
qsharp.summary: ''
ms.openlocfilehash: 6de4fcf86495136f2caec6fb6f873a18d751c977
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725688"
---
# <a name="applyifzeroc-operation"></a><span data-ttu-id="d5cfc-102">ApplyIfZeroC 작업</span><span class="sxs-lookup"><span data-stu-id="d5cfc-102">ApplyIfZeroC operation</span></span>

<span data-ttu-id="d5cfc-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="d5cfc-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="d5cfc-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d5cfc-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfZeroC<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl), zeroArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="d5cfc-105">입력</span><span class="sxs-lookup"><span data-stu-id="d5cfc-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="d5cfc-106">measurementResult: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="d5cfc-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit-ctl"></a><span data-ttu-id="d5cfc-107">onResultZeroOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="d5cfc-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="d5cfc-108">zeroArg: ' '</span><span class="sxs-lookup"><span data-stu-id="d5cfc-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="d5cfc-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d5cfc-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d5cfc-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d5cfc-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d5cfc-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="d5cfc-111">'T</span></span>

