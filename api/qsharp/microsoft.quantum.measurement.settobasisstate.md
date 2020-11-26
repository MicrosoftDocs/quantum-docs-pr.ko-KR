---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: SetToBasisState 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: 2612bfe488c830abd835be89b2f8ea6795abf675
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194154"
---
# <a name="settobasisstate-operation"></a><span data-ttu-id="7003e-102">SetToBasisState 작업</span><span class="sxs-lookup"><span data-stu-id="7003e-102">SetToBasisState operation</span></span>

<span data-ttu-id="7003e-103">네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="7003e-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="7003e-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="7003e-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="7003e-105">필요에 따라 비트를 측정 하 고 비트 대칭을 적용 하 여 지정 된 계산 기준 상태로 원하는 비트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7003e-105">Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.</span></span>

```qsharp
operation SetToBasisState (desired : Result, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="7003e-106">입력</span><span class="sxs-lookup"><span data-stu-id="7003e-106">Input</span></span>

### <a name="desired--__invalidresult__"></a><span data-ttu-id="7003e-107">desired: __유효 <Result> 하지 않음__</span><span class="sxs-lookup"><span data-stu-id="7003e-107">desired : __invalid<Result>__</span></span>

<span data-ttu-id="7003e-108">원하는 비트를 설정 해야 하는 기본 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="7003e-108">The basis state that the qubit should be set to.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="7003e-109">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7003e-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7003e-110">상태를 설정할의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="7003e-110">The qubit whose state is to be set.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7003e-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7003e-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7003e-112">설명</span><span class="sxs-lookup"><span data-stu-id="7003e-112">Remarks</span></span>

<span data-ttu-id="7003e-113">이 작업의 invariant로 직후를 호출 하면 `M(q)` `SetToBasisState(result, q)` 가 반환 됩니다 `result` .</span><span class="sxs-lookup"><span data-stu-id="7003e-113">As an invariant of this operation, calling `M(q)` immediately after `SetToBasisState(result, q)` will return `result`.</span></span>