---
uid: Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator
title: MultiplexOperationsFromGenerator 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsFromGenerator
qsharp.summary: >-
  Applies a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 2fde0bf391568f39128e6dca4b535aa6b78407c2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715800"
---
# <a name="multiplexoperationsfromgenerator-operation"></a><span data-ttu-id="9148e-102">MultiplexOperationsFromGenerator 작업</span><span class="sxs-lookup"><span data-stu-id="9148e-102">MultiplexOperationsFromGenerator operation</span></span>

<span data-ttu-id="9148e-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9148e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9148e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9148e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9148e-105">N-\ket{j} $로 제어 될 때 단일 $V _j $를 적용 하는 곱하기 제어 된 단일 $U 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9148e-105">Applies a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="9148e-106">$U = \sum ^ {N-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $입니다.</span><span class="sxs-lookup"><span data-stu-id="9148e-106">$U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
operation MultiplexOperationsFromGenerator<'T> (unitaryGenerator : (Int, (Int -> ('T => Unit is Adj + Ctl))), index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="9148e-107">입력</span><span class="sxs-lookup"><span data-stu-id="9148e-107">Input</span></span>

### <a name="unitarygenerator--intint---t--unit-adj--ctl"></a><span data-ttu-id="9148e-108">Unit Arygenerator: ([int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl)</span><span class="sxs-lookup"><span data-stu-id="9148e-108">unitaryGenerator : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl)</span></span>

<span data-ttu-id="9148e-109">첫 번째 요소가 `Int` unitaries $N $의 수이 고 두 번째 요소는 $ `(Int -> ('T => () is Adj + Ctl))` [0, N-1] $의 정수 $j $를 사용 하는 함수 이며 _j $ $V 단일 작업을 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="9148e-109">A tuple where the first element `Int` is the number of unitaries $N$, and the second element `(Int -> ('T => () is Adj + Ctl))` is a function that takes an integer $j$ in $[0,N-1]$ and outputs the unitary operation $V_j$.</span></span>


### <a name="index--littleendian"></a><span data-ttu-id="9148e-110">인덱스: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9148e-110">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9148e-111">숫자 상태 $ \ket{j} $를 거의 endian 형식으로 인코딩하는 $-# 컨트롤 레지스터를 $n 합니다.</span><span class="sxs-lookup"><span data-stu-id="9148e-111">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--t"></a><span data-ttu-id="9148e-112">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="9148e-112">target : 'T</span></span>

<span data-ttu-id="9148e-113">$V _j $가 작동 하는 일반 고 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="9148e-113">Generic qubit register that $V_j$ acts on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9148e-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9148e-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9148e-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9148e-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9148e-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="9148e-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="9148e-117">설명</span><span class="sxs-lookup"><span data-stu-id="9148e-117">Remarks</span></span>

<span data-ttu-id="9148e-118">`coefficients` $2 ^ n $ 미만으로 지정 된 경우는 id 요소로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="9148e-118">`coefficients` will be padded with identity elements if fewer than $2^n$ are specified.</span></span> <span data-ttu-id="9148e-119">이 구현에서는 $n-$1 보조 비트를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9148e-119">This implementation uses $n-1$ auxiliary qubits.</span></span>

## <a name="references"></a><span data-ttu-id="9148e-120">참조</span><span class="sxs-lookup"><span data-stu-id="9148e-120">References</span></span>

- [<span data-ttu-id="9148e-121">*Andrew Childs, Dmitri Maslov, Yunseong 베트남, Neil Ross, 위안 Su* , arxiv: 1711.10980</span><span class="sxs-lookup"><span data-stu-id="9148e-121"> *Andrew M. Childs, Dmitri Maslov, Yunseong Nam, Neil J. Ross, Yuan Su* , arXiv:1711.10980</span></span>](https://arxiv.org/abs/1711.10980)