---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: EstimateTermExpectation 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: 3f0ff5037b1424abb6fb318bd49ffd89f545822d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224652"
---
# <a name="estimatetermexpectation-operation"></a><span data-ttu-id="b739f-102">EstimateTermExpectation 작업</span><span class="sxs-lookup"><span data-stu-id="b739f-102">EstimateTermExpectation operation</span></span>

<span data-ttu-id="b739f-103">네임 스페이스: [JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="b739f-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="b739f-104">패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="b739f-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="b739f-105">지정 된 Jordan-Wigner Hamiltonian term에 연결 된 에너지를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="b739f-105">Computes the energy associated to a given Jordan-Wigner Hamiltonian term</span></span>

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="b739f-106">Description</span><span class="sxs-lookup"><span data-stu-id="b739f-106">Description</span></span>

<span data-ttu-id="b739f-107">이 작업은 각 측정 연산자에 연결 된 예상 값을 예측 하 고 샘플링을 사용 하 여 해당 계수를 곱합니다.</span><span class="sxs-lookup"><span data-stu-id="b739f-107">This operation estimates the expectation value associated to each measurement operator and multiplies it by the corresponding coefficient, using sampling.</span></span>
<span data-ttu-id="b739f-108">결과는 Jordan-Wigner 용어의 에너지를 포함 하는 변수로 집계 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b739f-108">The results are aggregated into a variable containing the energy of the Jordan-Wigner term.</span></span>

## <a name="input"></a><span data-ttu-id="b739f-109">입력</span><span class="sxs-lookup"><span data-stu-id="b739f-109">Input</span></span>

### <a name="inputstateunitary--qubit--unit--is-adj"></a><span data-ttu-id="b739f-110">inputStateUnitary: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="b739f-110">inputStateUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="b739f-111">상태 준비에 사용 되는 단일.</span><span class="sxs-lookup"><span data-stu-id="b739f-111">The unitary used for state preparation.</span></span>


### <a name="ops--pauli"></a><span data-ttu-id="b739f-112">ops: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="b739f-112">ops : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="b739f-113">Jordan-Wigner 용어의 측정 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="b739f-113">The measurement operators of the Jordan-Wigner term.</span></span>


### <a name="coeffs--double"></a><span data-ttu-id="b739f-114">coeffs: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="b739f-114">coeffs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="b739f-115">Jordan-Wigner 용어의 계수입니다.</span><span class="sxs-lookup"><span data-stu-id="b739f-115">The coefficients of the Jordan-Wigner term.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="b739f-116">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b739f-116">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b739f-117">분자 시스템을 시뮬레이트하는 데 필요한 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b739f-117">The number of qubits required to simulate the molecular system.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="b739f-118">nSamples: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b739f-118">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b739f-119">용어 예상을 추정 하는 데 사용할 샘플 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b739f-119">The number of samples to use for the estimation of the term expectation.</span></span>



## <a name="output--double"></a><span data-ttu-id="b739f-120">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b739f-120">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b739f-121">Jordan-Wigner 용어에 연결 된 에너지입니다.</span><span class="sxs-lookup"><span data-stu-id="b739f-121">The energy associated to the Jordan-Wigner term.</span></span>