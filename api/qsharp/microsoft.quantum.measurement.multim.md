---
uid: Microsoft.Quantum.Measurement.MultiM
title: MultiM 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MultiM
qsharp.summary: Measures each qubit in a given array in the standard basis.
ms.openlocfilehash: c39601f3e8b272b9341f1789b4c8e7230cb4182c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226998"
---
# <a name="multim-operation"></a><span data-ttu-id="830c9-102">MultiM 작업</span><span class="sxs-lookup"><span data-stu-id="830c9-102">MultiM operation</span></span>

<span data-ttu-id="830c9-103">네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="830c9-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="830c9-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="830c9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="830c9-105">지정 된 배열의 각 고 비트를 표준 기준으로 측정 합니다.</span><span class="sxs-lookup"><span data-stu-id="830c9-105">Measures each qubit in a given array in the standard basis.</span></span>

```qsharp
operation MultiM (targets : Qubit[]) : Result[]
```


## <a name="input"></a><span data-ttu-id="830c9-106">입력</span><span class="sxs-lookup"><span data-stu-id="830c9-106">Input</span></span>

### <a name="targets--qubit"></a><span data-ttu-id="830c9-107">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="830c9-107">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="830c9-108">측정할 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="830c9-108">An array of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="830c9-109">출력: __잘못 <Result> 된__[]</span><span class="sxs-lookup"><span data-stu-id="830c9-109">Output : __invalid<Result>__[]</span></span>

<span data-ttu-id="830c9-110">측정 결과의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="830c9-110">An array of measurement results.</span></span>