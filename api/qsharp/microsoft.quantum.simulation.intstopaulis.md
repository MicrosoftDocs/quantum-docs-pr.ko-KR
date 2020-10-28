---
uid: Microsoft.Quantum.Simulation.IntsToPaulis
title: IntsToPaulis 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntsToPaulis
qsharp.summary: Converts an array of integers to an array of single-qubit Pauli operators.
ms.openlocfilehash: 605257aa7ca39e457127e3c3459b5891145b1863
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709451"
---
# <a name="intstopaulis-function"></a><span data-ttu-id="06a2d-102">IntsToPaulis 함수</span><span class="sxs-lookup"><span data-stu-id="06a2d-102">IntsToPaulis function</span></span>

<span data-ttu-id="06a2d-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="06a2d-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="06a2d-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="06a2d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="06a2d-105">정수 배열을 단일가 나 비트 Pauli 연산자의 배열로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="06a2d-105">Converts an array of integers to an array of single-qubit Pauli operators.</span></span>

```qsharp
function IntsToPaulis (ints : Int[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="06a2d-106">입력</span><span class="sxs-lookup"><span data-stu-id="06a2d-106">Input</span></span>

### <a name="ints--int"></a><span data-ttu-id="06a2d-107">정수: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="06a2d-107">ints : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="06a2d-108">`0..3`Pauli 연산자로 변환할 범위의 정수 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="06a2d-108">Array of integers in the range `0..3`  to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="06a2d-109">출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="06a2d-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="06a2d-110">`paulis`Pauli 연산자의 배열에는에 `Pauli[]` 지정 된 `ints` 의 요소와 동일한 길이가 `paulis[idxPauli]` `[PauliI, PauliX, PauliY, PauliZ]` `ints[idxPauli]` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06a2d-110">An array `paulis` of Pauli operators `Pauli[]` the same length as `ints` such that `paulis[idxPauli]` is equal to the element of `[PauliI, PauliX, PauliY, PauliZ]` given by `ints[idxPauli]`.</span></span>