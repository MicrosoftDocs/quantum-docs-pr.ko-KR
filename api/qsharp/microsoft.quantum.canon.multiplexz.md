---
uid: Microsoft.Quantum.Canon.MultiplexZ
title: MultiplexZ 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexZ
qsharp.summary: Applies a Pauli Z rotation conditioned on an array of qubits.
ms.openlocfilehash: 364d23a0e57a2510f069b6db66b085368f20162e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206071"
---
# <a name="multiplexz-operation"></a><span data-ttu-id="3a208-102">MultiplexZ 작업</span><span class="sxs-lookup"><span data-stu-id="3a208-102">MultiplexZ operation</span></span>

<span data-ttu-id="3a208-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3a208-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3a208-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3a208-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3a208-105">조건 화 된 배열에 Pauli Z 회전을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a208-105">Applies a Pauli Z rotation conditioned on an array of qubits.</span></span>

```qsharp
operation MultiplexZ (coefficients : Double[], control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="3a208-106">Description</span><span class="sxs-lookup"><span data-stu-id="3a208-106">Description</span></span>

<span data-ttu-id="3a208-107">이렇게 하면 $ \ theta_j $ 각도에 따라 회전을 수행 하는 곱하기 제어 된 단일 연산이 적용 됩니다 ($n $-stbit number state $ \ket{j} $로 제어 되는 경우 $Z).</span><span class="sxs-lookup"><span data-stu-id="3a208-107">This applies the multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $Z$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="3a208-108">특히이 작업은 단일 개체로 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a208-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="3a208-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i Z \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="3a208-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0} \ket{j}\bra{j} \otimes e^{i Z \theta_j}.</span></span>
<span data-ttu-id="3a208-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="3a208-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="3a208-111">입력</span><span class="sxs-lookup"><span data-stu-id="3a208-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="3a208-112">계수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="3a208-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="3a208-113">최대 $2 ^ n $ 계수 $ \ theta_j $의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="3a208-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="3a208-114">$J $ th 계수는 작은 endian 형식으로 인코딩된 number state $ \ket{j} $를 인덱싱합니다.</span><span class="sxs-lookup"><span data-stu-id="3a208-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="3a208-115">컨트롤: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3a208-115">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3a208-116">숫자 상태 $ \ket{j} $를 거의 endian 형식으로 인코딩하는 $-# 컨트롤 레지스터를 $n 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a208-116">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="3a208-117">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3a208-117">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3a208-118">$E ^ {i P \ theta_j} $로 회전 한 단일 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="3a208-118">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3a208-119">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3a208-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3a208-120">설명</span><span class="sxs-lookup"><span data-stu-id="3a208-120">Remarks</span></span>

<span data-ttu-id="3a208-121">`coefficients` $2 ^ n $ 미만으로 지정 된 경우는 $ \ theta_j = $0.0 요소로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="3a208-121">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="3a208-122">참조 항목</span><span class="sxs-lookup"><span data-stu-id="3a208-122">References</span></span>

- <span data-ttu-id="3a208-123">퀀텀 논리 회로 Vivek Shende, Stephen S. Markov, Igor, Igor L. https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="3a208-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="3a208-124">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3a208-124">See Also</span></span>

- [<span data-ttu-id="3a208-125">ApproximatelyMultiplexZ입니다.</span><span class="sxs-lookup"><span data-stu-id="3a208-125">Microsoft.Quantum.Canon.ApproximatelyMultiplexZ</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyMultiplexZ)