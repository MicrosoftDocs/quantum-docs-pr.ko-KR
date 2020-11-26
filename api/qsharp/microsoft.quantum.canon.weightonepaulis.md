---
uid: Microsoft.Quantum.Canon.WeightOnePaulis
title: WeightOnePaulis 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: WeightOnePaulis
qsharp.summary: Returns an array of all weight-1 Pauli operators on a given number of qubits.
ms.openlocfilehash: 904c606393131d51eaa44d464ad52bec509eaf72
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204541"
---
# <a name="weightonepaulis-function"></a><span data-ttu-id="c56c0-102">WeightOnePaulis 함수</span><span class="sxs-lookup"><span data-stu-id="c56c0-102">WeightOnePaulis function</span></span>

<span data-ttu-id="c56c0-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c56c0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c56c0-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c56c0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c56c0-105">지정 된 수의 값에 대 한 모든 무게 1 Pauli 연산자의 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c56c0-105">Returns an array of all weight-1 Pauli operators on a given number of qubits.</span></span>

```qsharp
function WeightOnePaulis (nQubits : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="c56c0-106">입력</span><span class="sxs-lookup"><span data-stu-id="c56c0-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="c56c0-107">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c56c0-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c56c0-108">반환 된 Pauli 연산자가 정의 된 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c56c0-108">The number of qubits on which the returned Pauli operators are defined.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="c56c0-109">출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="c56c0-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="c56c0-110">각각 길이가 인 배열로 표시 되는 여러 개의 여러 비트 Pauli 연산자의 배열입니다 `nQubits` .</span><span class="sxs-lookup"><span data-stu-id="c56c0-110">An array of multi-qubit Pauli operators, each of which is represented as an array with length `nQubits`.</span></span>