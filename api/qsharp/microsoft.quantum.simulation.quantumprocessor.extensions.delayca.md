---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.DelayCA
title: DelayCA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: DelayCA
qsharp.summary: ''
ms.openlocfilehash: aacbf6fb595700cf0631263ddbc1925846f9ad9f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192590"
---
# <a name="delayca-operation"></a><span data-ttu-id="af5fd-102">DelayCA 작업</span><span class="sxs-lookup"><span data-stu-id="af5fd-102">DelayCA operation</span></span>

<span data-ttu-id="af5fd-103">네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="af5fd-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="af5fd-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="af5fd-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation DelayCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T, aux : Unit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="af5fd-105">입력</span><span class="sxs-lookup"><span data-stu-id="af5fd-105">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="af5fd-106">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="af5fd-106">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="arg--t"></a><span data-ttu-id="af5fd-107">인수: ' '</span><span class="sxs-lookup"><span data-stu-id="af5fd-107">arg : 'T</span></span>




### <a name="aux--unit"></a><span data-ttu-id="af5fd-108">aux: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="af5fd-108">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="af5fd-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="af5fd-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="af5fd-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="af5fd-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="af5fd-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="af5fd-111">'T</span></span>

