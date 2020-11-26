---
uid: Microsoft.Quantum.Canon.MultiplexOperations
title: MultiplexOperations 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperations
qsharp.summary: >-
  Applies an array of operations controlled by an array of number states.

  That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: ad66b39fcfacbe5231ec3b9ba96989d6d5d449c1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206105"
---
# <a name="multiplexoperations-operation"></a><span data-ttu-id="0ba19-102">MultiplexOperations 작업</span><span class="sxs-lookup"><span data-stu-id="0ba19-102">MultiplexOperations operation</span></span>

<span data-ttu-id="0ba19-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0ba19-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0ba19-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0ba19-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0ba19-105">숫자 상태의 배열에 의해 제어 되는 작업 배열을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba19-105">Applies an array of operations controlled by an array of number states.</span></span>

<span data-ttu-id="0ba19-106">즉, $n $-\ket{j} $로 제어 될 때 단일 $V _j $를 적용 하는 곱하기 제어 된 단일 $U 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba19-106">That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="0ba19-107">$U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.</span><span class="sxs-lookup"><span data-stu-id="0ba19-107">$U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
operation MultiplexOperations<'T> (unitaries : ('T => Unit is Adj + Ctl)[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="0ba19-108">입력</span><span class="sxs-lookup"><span data-stu-id="0ba19-108">Input</span></span>

### <a name="unitaries--t--unit--is-adj--ctl"></a><span data-ttu-id="0ba19-109">unitaries: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl []</span><span class="sxs-lookup"><span data-stu-id="0ba19-109">unitaries : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>

<span data-ttu-id="0ba19-110">최대 $2 ^ n $ 단일 작업의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="0ba19-110">Array of up to $2^n$ unitary operations.</span></span> <span data-ttu-id="0ba19-111">$J $ th 연산은 작은 endian 형식으로 인코딩된 숫자 상태 $ \ket{j} $로 인덱싱됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ba19-111">The $j$th operation is indexed by the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="index--littleendian"></a><span data-ttu-id="0ba19-112">인덱스: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0ba19-112">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0ba19-113">숫자 상태 $ \ket{j} $를 거의 endian 형식으로 인코딩하는 $-# 컨트롤 레지스터를 $n 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba19-113">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--t"></a><span data-ttu-id="0ba19-114">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="0ba19-114">target : 'T</span></span>

<span data-ttu-id="0ba19-115">$V _j $가 작동 하는 일반 고 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="0ba19-115">Generic qubit register that $V_j$ acts on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0ba19-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0ba19-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0ba19-117">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0ba19-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0ba19-118">없습니다</span><span class="sxs-lookup"><span data-stu-id="0ba19-118">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="0ba19-119">설명</span><span class="sxs-lookup"><span data-stu-id="0ba19-119">Remarks</span></span>

<span data-ttu-id="0ba19-120">`coefficients` $2 ^ n $ 미만으로 지정 된 경우는 id 요소로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="0ba19-120">`coefficients` will be padded with identity elements if fewer than $2^n$ are specified.</span></span> <span data-ttu-id="0ba19-121">이 구현에서는 $n-$1 보조 비트를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba19-121">This implementation uses $n - 1$ auxiliary qubits.</span></span>

## <a name="references"></a><span data-ttu-id="0ba19-122">참조 항목</span><span class="sxs-lookup"><span data-stu-id="0ba19-122">References</span></span>

- <span data-ttu-id="0ba19-123">퀀텀 속도 향상 Andrew Childs, Dmitri Maslov, Yunseong 베트남, Neil Ross, 위안 Su를 사용 하 여 첫 번째 퀀텀 시뮬레이션을 지향 합니다. https://arxiv.org/abs/1711.10980</span><span class="sxs-lookup"><span data-stu-id="0ba19-123">Toward the first quantum simulation with quantum speedup Andrew M. Childs, Dmitri Maslov, Yunseong Nam, Neil J. Ross, Yuan Su https://arxiv.org/abs/1711.10980</span></span>