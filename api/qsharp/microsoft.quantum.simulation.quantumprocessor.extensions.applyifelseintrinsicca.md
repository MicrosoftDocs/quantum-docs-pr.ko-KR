---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseIntrinsicCA
title: ApplyIfElseIntrinsicCA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseIntrinsicCA
qsharp.summary: ''
ms.openlocfilehash: 6ba83f7344c77b95f2e7397cd42f39884556547a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855690"
---
# <a name="applyifelseintrinsicca-operation"></a><span data-ttu-id="88f37-102">ApplyIfElseIntrinsicCA 작업</span><span class="sxs-lookup"><span data-stu-id="88f37-102">ApplyIfElseIntrinsicCA operation</span></span>

<span data-ttu-id="88f37-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="88f37-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="88f37-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="88f37-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfElseIntrinsicCA (measurementResult : Result, onResultZeroOp : (Unit => Unit is Ctl + Adj), onResultOneOp : (Unit => Unit is Ctl + Adj)) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="88f37-105">입력</span><span class="sxs-lookup"><span data-stu-id="88f37-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="88f37-106">measurementResult: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="88f37-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--unit--unit--is-adj--ctl"></a><span data-ttu-id="88f37-107">onResultZeroOp: [unit](xref:microsoft.quantum.lang-ref.unit) => [unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="88f37-107">onResultZeroOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="onresultoneop--unit--unit--is-adj--ctl"></a><span data-ttu-id="88f37-108">onresultoneop: [unit](xref:microsoft.quantum.lang-ref.unit) => [unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="88f37-108">onResultOneOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>





## <a name="output--unit"></a><span data-ttu-id="88f37-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="88f37-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

