---
uid: Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary
title: ApproximatelyApplyDiagonalUnitary 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyApplyDiagonalUnitary
qsharp.summary: Applies an array of complex phases to numeric basis states of a register of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: 9d9b1ced320b142aef2a2cd8f3335f855d37048f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716822"
---
# <a name="approximatelyapplydiagonalunitary-operation"></a><span data-ttu-id="525f1-102">ApproximatelyApplyDiagonalUnitary 작업</span><span class="sxs-lookup"><span data-stu-id="525f1-102">ApproximatelyApplyDiagonalUnitary operation</span></span>

<span data-ttu-id="525f1-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="525f1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="525f1-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="525f1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="525f1-105">지정 된 허용 오차에 따라 작은 회전 각도를 잘라내는 상위 비트 레지스터의 숫자 기반 상태에 복잡 한 단계의 배열을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="525f1-105">Applies an array of complex phases to numeric basis states of a register of qubits, truncating small rotation angles according to a given tolerance.</span></span>

```qsharp
operation ApproximatelyApplyDiagonalUnitary (tolerance : Double, coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="525f1-106">Description</span><span class="sxs-lookup"><span data-stu-id="525f1-106">Description</span></span>

<span data-ttu-id="525f1-107">이 작업에서는 $n $-stbit number state $ \ket{j} $에 $e ^ {i \ theta_j} $ 복합 단계를 적용 하는 대각선을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="525f1-107">This operation implements a diagonal unitary that applies a complex phase $e^{i \theta_j}$ on the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="525f1-108">특히이 작업은 단일 개체로 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="525f1-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="525f1-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} e ^ {i \ theta_j} \ket{j}\bra{j}.</span><span class="sxs-lookup"><span data-stu-id="525f1-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0}e^{i\theta_j}\ket{j}\bra{j}.</span></span>
<span data-ttu-id="525f1-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="525f1-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="525f1-111">입력</span><span class="sxs-lookup"><span data-stu-id="525f1-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="525f1-112">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="525f1-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="525f1-113">작은 계수를 잘라내는 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="525f1-113">A tolerance below which small coefficients are truncated.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="525f1-114">계수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="525f1-114">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="525f1-115">최대 $2 ^ n $ 계수 $ \ theta_j $의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="525f1-115">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="525f1-116">$J $ th 계수는 작은 endian 형식으로 인코딩된 number state $ \ket{j} $를 인덱싱합니다.</span><span class="sxs-lookup"><span data-stu-id="525f1-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="525f1-117">작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="525f1-117">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="525f1-118">숫자 상태 $ \ket{j} $를 거의 endian 형식으로 인코딩하는 $-# 컨트롤 레지스터를 $n 합니다.</span><span class="sxs-lookup"><span data-stu-id="525f1-118">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="525f1-119">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="525f1-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="525f1-120">설명</span><span class="sxs-lookup"><span data-stu-id="525f1-120">Remarks</span></span>

<span data-ttu-id="525f1-121">`coefficients` $2 ^ n $ 미만으로 지정 된 경우는 $ \ theta_j = $0.0 요소로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="525f1-121">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="525f1-122">참조</span><span class="sxs-lookup"><span data-stu-id="525f1-122">References</span></span>

- <span data-ttu-id="525f1-123">퀀텀 논리 회로 Vivek Shende, Stephen S. Markov, Igor, Igor L. https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="525f1-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="525f1-124">참고 항목</span><span class="sxs-lookup"><span data-stu-id="525f1-124">See Also</span></span>

- [<span data-ttu-id="525f1-125">ApplyDiagonalUnitary입니다.</span><span class="sxs-lookup"><span data-stu-id="525f1-125">Microsoft.Quantum.Canon.ApplyDiagonalUnitary</span></span>](xref:Microsoft.Quantum.Canon.ApplyDiagonalUnitary)