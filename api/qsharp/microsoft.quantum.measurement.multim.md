---
uid: Microsoft.Quantum.Measurement.MultiM
title: MultiM 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MultiM
qsharp.summary: Measures each qubit in a given array in the standard basis.
ms.openlocfilehash: 36de9dbdfc96f6e1698ee4537405f7cb74e44262
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711040"
---
# <a name="multim-operation"></a><span data-ttu-id="fdf09-102">MultiM 작업</span><span class="sxs-lookup"><span data-stu-id="fdf09-102">MultiM operation</span></span>

<span data-ttu-id="fdf09-103">네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="fdf09-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="fdf09-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fdf09-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fdf09-105">지정 된 배열의 각 고 비트를 표준 기준으로 측정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf09-105">Measures each qubit in a given array in the standard basis.</span></span>

```qsharp
operation MultiM (targets : Qubit[]) : Result[]
```


## <a name="input"></a><span data-ttu-id="fdf09-106">입력</span><span class="sxs-lookup"><span data-stu-id="fdf09-106">Input</span></span>

### <a name="targets--qubit"></a><span data-ttu-id="fdf09-107">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fdf09-107">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="fdf09-108">측정할 비트의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="fdf09-108">An array of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="fdf09-109">출력: __잘못 <Result> 된__ []</span><span class="sxs-lookup"><span data-stu-id="fdf09-109">Output : __invalid<Result>__ []</span></span>

<span data-ttu-id="fdf09-110">측정 결과의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="fdf09-110">An array of measurement results.</span></span>