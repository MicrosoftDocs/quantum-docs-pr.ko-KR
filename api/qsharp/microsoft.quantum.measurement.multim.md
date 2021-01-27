---
uid: Microsoft.Quantum.Measurement.MultiM
title: MultiM 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MultiM
qsharp.summary: Measures each qubit in a given array in the standard basis.
ms.openlocfilehash: b7f4083bde84c204611ea33746ae351a3e27b946
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857005"
---
# <a name="multim-operation"></a><span data-ttu-id="d9442-102">MultiM 작업</span><span class="sxs-lookup"><span data-stu-id="d9442-102">MultiM operation</span></span>

<span data-ttu-id="d9442-103">네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="d9442-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="d9442-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d9442-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d9442-105">지정 된 배열의 각 고 비트를 표준 기준으로 측정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9442-105">Measures each qubit in a given array in the standard basis.</span></span>

```qsharp
operation MultiM (targets : Qubit[]) : Result[]
```


## <a name="input"></a><span data-ttu-id="d9442-106">입력</span><span class="sxs-lookup"><span data-stu-id="d9442-106">Input</span></span>

### <a name="targets--qubit"></a><span data-ttu-id="d9442-107">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d9442-107">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d9442-108">측정할 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="d9442-108">An array of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="d9442-109">출력: __잘못 <Result> 된__[]</span><span class="sxs-lookup"><span data-stu-id="d9442-109">Output : __invalid<Result>__[]</span></span>

<span data-ttu-id="d9442-110">측정 결과의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="d9442-110">An array of measurement results.</span></span>