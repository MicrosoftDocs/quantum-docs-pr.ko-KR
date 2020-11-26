---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: MeasurementOperators 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: a5ea9a776f522e927f2f4545bd417d35bda83994
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214350"
---
# <a name="measurementoperators-function"></a><span data-ttu-id="f3ee1-102">MeasurementOperators 함수</span><span class="sxs-lookup"><span data-stu-id="f3ee1-102">MeasurementOperators function</span></span>

<span data-ttu-id="f3ee1-103">네임 스페이스: [JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="f3ee1-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="f3ee1-104">패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f3ee1-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="f3ee1-105">Jordan-Wigner 용어의 예상 값을 계산 하는 데 필요한 모든 측정 연산자를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-105">Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.</span></span>

```qsharp
function MeasurementOperators (nQubits : Int, indices : Int[], termType : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="f3ee1-106">입력</span><span class="sxs-lookup"><span data-stu-id="f3ee1-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="f3ee1-107">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f3ee1-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f3ee1-108">분자 시스템을 시뮬레이트하는 데 필요한 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-108">The number of qubits required to simulate the molecular system.</span></span>


### <a name="indices--int"></a><span data-ttu-id="f3ee1-109">인덱스: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f3ee1-109">indices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f3ee1-110">각 Pauli 연산자가 적용 되는의 인덱스를 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-110">An array containing the indices of the qubit each Pauli operator is applied to.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="f3ee1-111">termType: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f3ee1-111">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f3ee1-112">Jordan-Wigner 용어의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-112">The type of the Jordan-Wigner term.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="f3ee1-113">출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="f3ee1-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="f3ee1-114">측정 연산자의 배열 (각각 Pauli의 배열)입니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-114">An array of measurement operators (each being an array of Pauli).</span></span>