---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: MeasurementOperators 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: 24d752c4f198764b6e7c6ea6c49669c020c1a502
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713679"
---
# <a name="measurementoperators-function"></a><span data-ttu-id="a7be8-102">MeasurementOperators 함수</span><span class="sxs-lookup"><span data-stu-id="a7be8-102">MeasurementOperators function</span></span>

<span data-ttu-id="a7be8-103">네임 스페이스: [JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="a7be8-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="a7be8-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a7be8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a7be8-105">Jordan-Wigner 용어의 예상 값을 계산 하는 데 필요한 모든 측정 연산자를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7be8-105">Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.</span></span>

```qsharp
function MeasurementOperators (nQubits : Int, indices : Int[], termType : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="a7be8-106">입력</span><span class="sxs-lookup"><span data-stu-id="a7be8-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="a7be8-107">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a7be8-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a7be8-108">분자 시스템을 시뮬레이트하는 데 필요한 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a7be8-108">The number of qubits required to simulate the molecular system.</span></span>


### <a name="indices--int"></a><span data-ttu-id="a7be8-109">인덱스: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="a7be8-109">indices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="a7be8-110">각 Pauli 연산자가 적용 되는의 인덱스를 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="a7be8-110">An array containing the indices of the qubit each Pauli operator is applied to.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="a7be8-111">termType: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a7be8-111">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a7be8-112">Jordan-Wigner 용어의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a7be8-112">The type of the Jordan-Wigner term.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="a7be8-113">출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="a7be8-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="a7be8-114">측정 연산자의 배열 (각각 Pauli의 배열)입니다.</span><span class="sxs-lookup"><span data-stu-id="a7be8-114">An array of measurement operators (each being an array of Pauli).</span></span>