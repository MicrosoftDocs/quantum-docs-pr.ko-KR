---
uid: Microsoft.Quantum.Canon.ApplyDiagonalUnitary
title: ApplyDiagonalUnitary 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyDiagonalUnitary
qsharp.summary: Applies an array of complex phases to numeric basis states of a register of qubits.
ms.openlocfilehash: 6ecacf6e4fe2c505036de208c8aeb5350e479e3c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718285"
---
# <a name="applydiagonalunitary-operation"></a><span data-ttu-id="b70a9-102">ApplyDiagonalUnitary 작업</span><span class="sxs-lookup"><span data-stu-id="b70a9-102">ApplyDiagonalUnitary operation</span></span>

<span data-ttu-id="b70a9-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b70a9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b70a9-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b70a9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b70a9-105">일련의 복잡 한 단계 배열을 다양 한 양의 레지스터의 숫자 기반 상태에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b70a9-105">Applies an array of complex phases to numeric basis states of a register of qubits.</span></span>

```qsharp
operation ApplyDiagonalUnitary (coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="b70a9-106">Description</span><span class="sxs-lookup"><span data-stu-id="b70a9-106">Description</span></span>

<span data-ttu-id="b70a9-107">이 작업에서는 $n $-stbit number state $ \ket{j} $에 $e ^ {i \ theta_j} $ 복합 단계를 적용 하는 대각선을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="b70a9-107">This operation implements a diagonal unitary that applies a complex phase $e^{i \theta_j}$ on the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="b70a9-108">특히이 작업은 단일 개체로 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b70a9-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="b70a9-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} e ^ {i \ theta_j} \ket{j}\bra{j}.</span><span class="sxs-lookup"><span data-stu-id="b70a9-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0}e^{i\theta_j}\ket{j}\bra{j}.</span></span>
<span data-ttu-id="b70a9-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="b70a9-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="b70a9-111">입력</span><span class="sxs-lookup"><span data-stu-id="b70a9-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="b70a9-112">계수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="b70a9-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="b70a9-113">최대 $2 ^ n $ 계수 $ \ theta_j $의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="b70a9-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="b70a9-114">$J $ th 계수는 작은 endian 형식으로 인코딩된 number state $ \ket{j} $를 인덱싱합니다.</span><span class="sxs-lookup"><span data-stu-id="b70a9-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="b70a9-115">작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b70a9-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b70a9-116">숫자 상태 $ \ket{j} $를 거의 endian 형식으로 인코딩하는 $-# 컨트롤 레지스터를 $n 합니다.</span><span class="sxs-lookup"><span data-stu-id="b70a9-116">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b70a9-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b70a9-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b70a9-118">설명</span><span class="sxs-lookup"><span data-stu-id="b70a9-118">Remarks</span></span>

<span data-ttu-id="b70a9-119">`coefficients` $2 ^ n $ 미만으로 지정 된 경우는 $ \ theta_j = $0.0 요소로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="b70a9-119">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="b70a9-120">참조</span><span class="sxs-lookup"><span data-stu-id="b70a9-120">References</span></span>

- <span data-ttu-id="b70a9-121">퀀텀 논리 회로 Vivek Shende, Stephen S. Markov, Igor, Igor L. https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="b70a9-121">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="b70a9-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b70a9-122">See Also</span></span>

- [<span data-ttu-id="b70a9-123">ApproximatelyApplyDiagonalUnitary입니다.</span><span class="sxs-lookup"><span data-stu-id="b70a9-123">Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary)