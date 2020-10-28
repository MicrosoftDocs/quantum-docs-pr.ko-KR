---
uid: Microsoft.Quantum.Canon.WeightOnePaulis
title: WeightOnePaulis 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: WeightOnePaulis
qsharp.summary: Returns an array of all weight-1 Pauli operators on a given number of qubits.
ms.openlocfilehash: 89802c1bc6f3da8edef27b698eb61098e47dfc85
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715198"
---
# <a name="weightonepaulis-function"></a><span data-ttu-id="c1483-102">WeightOnePaulis 함수</span><span class="sxs-lookup"><span data-stu-id="c1483-102">WeightOnePaulis function</span></span>

<span data-ttu-id="c1483-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c1483-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c1483-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c1483-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c1483-105">지정 된 수의 값에 대 한 모든 무게 1 Pauli 연산자의 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1483-105">Returns an array of all weight-1 Pauli operators on a given number of qubits.</span></span>

```qsharp
function WeightOnePaulis (nQubits : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="c1483-106">입력</span><span class="sxs-lookup"><span data-stu-id="c1483-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="c1483-107">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c1483-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c1483-108">반환 된 Pauli 연산자가 정의 된 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c1483-108">The number of qubits on which the returned Pauli operators are defined.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="c1483-109">출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="c1483-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="c1483-110">각각 길이가 인 배열로 표시 되는 여러 개의 여러 비트 Pauli 연산자의 배열입니다 `nQubits` .</span><span class="sxs-lookup"><span data-stu-id="c1483-110">An array of multi-qubit Pauli operators, each of which is represented as an array with length `nQubits`.</span></span>