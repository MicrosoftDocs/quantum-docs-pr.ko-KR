---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: EstimateTermExpectation 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: ef689c55f966e63a2ab8bcdccf99d9cb5e6d3a4d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713728"
---
# <a name="estimatetermexpectation-operation"></a><span data-ttu-id="9f6d2-102">EstimateTermExpectation 작업</span><span class="sxs-lookup"><span data-stu-id="9f6d2-102">EstimateTermExpectation operation</span></span>

<span data-ttu-id="9f6d2-103">네임 스페이스: [JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="9f6d2-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="9f6d2-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9f6d2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9f6d2-105">지정 된 Jordan-Wigner Hamiltonian term에 연결 된 에너지를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f6d2-105">Computes the energy associated to a given Jordan-Wigner Hamiltonian term</span></span>

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="9f6d2-106">Description</span><span class="sxs-lookup"><span data-stu-id="9f6d2-106">Description</span></span>

<span data-ttu-id="9f6d2-107">이 작업은 각 측정 연산자에 연결 된 예상 값을 예측 하 고 샘플링을 사용 하 여 해당 계수를 곱합니다.</span><span class="sxs-lookup"><span data-stu-id="9f6d2-107">This operation estimates the expectation value associated to each measurement operator and multiplies it by the corresponding coefficient, using sampling.</span></span>
<span data-ttu-id="9f6d2-108">결과는 Jordan-Wigner 용어의 에너지를 포함 하는 변수로 집계 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f6d2-108">The results are aggregated into a variable containing the energy of the Jordan-Wigner term.</span></span>

## <a name="input"></a><span data-ttu-id="9f6d2-109">입력</span><span class="sxs-lookup"><span data-stu-id="9f6d2-109">Input</span></span>

### <a name="inputstateunitary--qubit--unit-adj"></a><span data-ttu-id="9f6d2-110">inputStateUnitary: Adj [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9f6d2-110">inputStateUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="9f6d2-111">상태 준비에 사용 되는 단일.</span><span class="sxs-lookup"><span data-stu-id="9f6d2-111">The unitary used for state preparation.</span></span>


### <a name="ops--pauli"></a><span data-ttu-id="9f6d2-112">ops: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="9f6d2-112">ops : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="9f6d2-113">Jordan-Wigner 용어의 측정 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="9f6d2-113">The measurement operators of the Jordan-Wigner term.</span></span>


### <a name="coeffs--double"></a><span data-ttu-id="9f6d2-114">coeffs: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="9f6d2-114">coeffs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="9f6d2-115">Jordan-Wigner 용어의 계수입니다.</span><span class="sxs-lookup"><span data-stu-id="9f6d2-115">The coefficients of the Jordan-Wigner term.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="9f6d2-116">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9f6d2-116">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9f6d2-117">분자 시스템을 시뮬레이트하는 데 필요한 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9f6d2-117">The number of qubits required to simulate the molecular system.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="9f6d2-118">nSamples: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9f6d2-118">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9f6d2-119">용어 예상을 추정 하는 데 사용할 샘플 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9f6d2-119">The number of samples to use for the estimation of the term expectation.</span></span>



## <a name="output--double"></a><span data-ttu-id="9f6d2-120">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9f6d2-120">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9f6d2-121">Jordan-Wigner 용어에 연결 된 에너지입니다.</span><span class="sxs-lookup"><span data-stu-id="9f6d2-121">The energy associated to the Jordan-Wigner term.</span></span>