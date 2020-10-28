---
uid: Microsoft.Quantum.Canon.MultiplexOperationsBruteForceFromGenerator
title: MultiplexOperationsBruteForceFromGenerator 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsBruteForceFromGenerator
qsharp.summary: >-
  Applies multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 2a9bb083b121745bd556aac692d5dc85ffec3791
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715821"
---
# <a name="multiplexoperationsbruteforcefromgenerator-operation"></a><span data-ttu-id="fac88-102">MultiplexOperationsBruteForceFromGenerator 작업</span><span class="sxs-lookup"><span data-stu-id="fac88-102">MultiplexOperationsBruteForceFromGenerator operation</span></span>

<span data-ttu-id="fac88-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fac88-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fac88-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fac88-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fac88-105">N-\ket{j} $로 제어 될 때 단일 $V _j $를 적용 하는 곱하기 제어 된 단일 $U 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fac88-105">Applies multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="fac88-106">$U = \sum ^ {N-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $입니다.</span><span class="sxs-lookup"><span data-stu-id="fac88-106">$U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
operation MultiplexOperationsBruteForceFromGenerator<'T> (unitaryGenerator : (Int, (Int -> ('T => Unit is Adj + Ctl))), index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="fac88-107">입력</span><span class="sxs-lookup"><span data-stu-id="fac88-107">Input</span></span>

### <a name="unitarygenerator--intint---t--unit-adj--ctl"></a><span data-ttu-id="fac88-108">Unit Arygenerator: ([int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl)</span><span class="sxs-lookup"><span data-stu-id="fac88-108">unitaryGenerator : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl)</span></span>

<span data-ttu-id="fac88-109">첫 번째 요소가 `Int` unitaries $N $의 수이 고 두 번째 요소는 $ `(Int -> ('T => () is Adj + Ctl))` [0, N-1] $의 정수 $j $를 사용 하는 함수 이며 _j $ $V 단일 작업을 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="fac88-109">A tuple where the first element `Int` is the number of unitaries $N$, and the second element `(Int -> ('T => () is Adj + Ctl))` is a function that takes an integer $j$ in $[0,N-1]$ and outputs the unitary operation $V_j$.</span></span>


### <a name="index--littleendian"></a><span data-ttu-id="fac88-110">인덱스: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="fac88-110">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="fac88-111">숫자 상태 $ \ket{j} $를 거의 endian 형식으로 인코딩하는 $-# 컨트롤 레지스터를 $n 합니다.</span><span class="sxs-lookup"><span data-stu-id="fac88-111">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--t"></a><span data-ttu-id="fac88-112">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="fac88-112">target : 'T</span></span>

<span data-ttu-id="fac88-113">$V _j $가 작동 하는 일반 고 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="fac88-113">Generic qubit register that $V_j$ acts on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fac88-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fac88-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="fac88-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="fac88-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fac88-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="fac88-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="fac88-117">설명</span><span class="sxs-lookup"><span data-stu-id="fac88-117">Remarks</span></span>

<span data-ttu-id="fac88-118">`coefficients` $2 ^ n $ 미만으로 지정 된 경우는 id 요소로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="fac88-118">`coefficients` will be padded with identity elements if fewer than $2^n$ are specified.</span></span> <span data-ttu-id="fac88-119">이 버전은 n 제어 된 단일 연산자를 반복 하 여 직접 구현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fac88-119">This version is implemented directly by looping through n-controlled unitary operators.</span></span>