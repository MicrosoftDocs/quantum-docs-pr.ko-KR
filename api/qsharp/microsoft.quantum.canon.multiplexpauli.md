---
uid: Microsoft.Quantum.Canon.MultiplexPauli
title: MultiplexPauli 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexPauli
qsharp.summary: Applies a Pauli rotation conditioned on an array of qubits.
ms.openlocfilehash: 0714e796c1e5ad097814bcf507f49f59a844e9ff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715786"
---
# <a name="multiplexpauli-operation"></a><span data-ttu-id="081f5-102">MultiplexPauli 작업</span><span class="sxs-lookup"><span data-stu-id="081f5-102">MultiplexPauli operation</span></span>

<span data-ttu-id="081f5-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="081f5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="081f5-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="081f5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="081f5-105">원하는 비트 배열에 Pauli 회전 조건 화 된을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="081f5-105">Applies a Pauli rotation conditioned on an array of qubits.</span></span>

```qsharp
operation MultiplexPauli (coefficients : Double[], pauli : Pauli, control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="081f5-106">Description</span><span class="sxs-lookup"><span data-stu-id="081f5-106">Description</span></span>

<span data-ttu-id="081f5-107">이렇게 하면 $ \ theta_j $ 각도에 따라 회전을 수행 하는 곱하기 제어 된 단일 연산이 적용 됩니다 .이는 $n $-stbit number state $ \ket{j} $로 제어 되는 경우 $P $입니다.</span><span class="sxs-lookup"><span data-stu-id="081f5-107">This applies a multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $P$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="081f5-108">특히이 작업은 단일 작업으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="081f5-108">In particular, the action of this operation is represented by the unitary</span></span>

<span data-ttu-id="081f5-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i P \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="081f5-109">$$ \begin{align} U = \sum^{2^n - 1}_{j=0} \ket{j}\bra{j} \otimes e^{i P \theta_j}.</span></span>
<span data-ttu-id="081f5-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="081f5-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="081f5-111">입력</span><span class="sxs-lookup"><span data-stu-id="081f5-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="081f5-112">계수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="081f5-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="081f5-113">최대 $2 ^ n $ 계수 $ \ theta_j $의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="081f5-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="081f5-114">$J $ th 계수는 작은 endian 형식으로 인코딩된 number state $ \ket{j} $를 인덱싱합니다.</span><span class="sxs-lookup"><span data-stu-id="081f5-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="pauli--pauli"></a><span data-ttu-id="081f5-115">pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="081f5-115">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="081f5-116">Pauli 연산자는 회전 축을 결정 하는 $ $P 합니다.</span><span class="sxs-lookup"><span data-stu-id="081f5-116">Pauli operator $P$ that determines axis of rotation.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="081f5-117">컨트롤: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="081f5-117">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="081f5-118">숫자 상태 $ \ket{j} $를 거의 endian 형식으로 인코딩하는 $-# 컨트롤 레지스터를 $n 합니다.</span><span class="sxs-lookup"><span data-stu-id="081f5-118">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="081f5-119">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="081f5-119">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="081f5-120">$E ^ {i P \ theta_j} $로 회전 한 단일 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="081f5-120">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="081f5-121">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="081f5-121">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="081f5-122">설명</span><span class="sxs-lookup"><span data-stu-id="081f5-122">Remarks</span></span>

<span data-ttu-id="081f5-123">`coefficients` $2 ^ n $ 미만으로 지정 된 경우는 $ \ theta_j = $0.0 요소로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="081f5-123">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="081f5-124">참고 항목</span><span class="sxs-lookup"><span data-stu-id="081f5-124">See Also</span></span>

- [<span data-ttu-id="081f5-125">ApproximatelyMultiplexPauli입니다.</span><span class="sxs-lookup"><span data-stu-id="081f5-125">Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli)