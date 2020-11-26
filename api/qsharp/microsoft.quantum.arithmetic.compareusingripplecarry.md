---
uid: Microsoft.Quantum.Arithmetic.CompareUsingRippleCarry
title: CompareUsingRippleCarry 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareUsingRippleCarry
qsharp.summary: This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.
ms.openlocfilehash: e2d6e5a663f8c4e101c7e2ab1346d10cade3f4e0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223462"
---
# <a name="compareusingripplecarry-operation"></a><span data-ttu-id="9fa47-102">CompareUsingRippleCarry 작업</span><span class="sxs-lookup"><span data-stu-id="9fa47-102">CompareUsingRippleCarry operation</span></span>

<span data-ttu-id="9fa47-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9fa47-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9fa47-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9fa47-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9fa47-105">이 연산은 값의 XOR를 출력의 비트에 적용 하 여, 값의 레지스터가 나타내는 정수가 다른 정수 보다 큰지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa47-105">This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.</span></span>

```qsharp
operation CompareUsingRippleCarry (x : Microsoft.Quantum.Arithmetic.LittleEndian, y : Microsoft.Quantum.Arithmetic.LittleEndian, output : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="9fa47-106">설명</span><span class="sxs-lookup"><span data-stu-id="9fa47-106">Description</span></span>

<span data-ttu-id="9fa47-107">두 개의 정수가 지정 되 `x` 고 `y` 동일한 크기의 비트 레지스터에 저장 된 경우이 작업은 충족 되는지 확인 `x > y` 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa47-107">Given two integers `x` and `y` stored in equal-size qubit registers, this operation checks if they satisfy `x > y`.</span></span> <span data-ttu-id="9fa47-108">True 이면 1이 XORed 출력으로 변환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fa47-108">If true, 1 is XORed into an output qubit.</span></span> <span data-ttu-id="9fa47-109">그렇지 않으면 0이 출력의 XORed 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fa47-109">Otherwise, 0 is XORed into an output qubit.</span></span>
<span data-ttu-id="9fa47-110">즉,이 작업은 단일 $ $ \begin{align} U\ket {x} \ k {y} \ k {z} = \ket{x}\ket{y}\ket{z\oplus (x>y)}로 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9fa47-110">In other words, this operation can be represented by the unitary $$ \begin{align} U\ket{x}\ket{y}\ket{z} = \ket{x}\ket{y}\ket{z\oplus (x>y)}.</span></span>
<span data-ttu-id="9fa47-111">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="9fa47-111">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="9fa47-112">입력</span><span class="sxs-lookup"><span data-stu-id="9fa47-112">Input</span></span>

### <a name="x--littleendian"></a><span data-ttu-id="9fa47-113">x: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9fa47-113">x : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9fa47-114">지정 된 형식으로 저장 되는 첫 번째 숫자 `LittleEndian` 는 이상 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa47-114">First number to be compared stored in `LittleEndian` format in a qubit register.</span></span>


### <a name="y--littleendian"></a><span data-ttu-id="9fa47-115">y: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9fa47-115">y : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9fa47-116">지정 된 형식에 저장 된 두 번째 숫자 `LittleEndian` 입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa47-116">Second number to be compared stored in `LittleEndian` format in a qubit register.</span></span>


### <a name="output--qubit"></a><span data-ttu-id="9fa47-117">출력: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9fa47-117">output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9fa47-118">비교 결과를 저장 하 $x y $>입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa47-118">Qubit that stores the result of the comparison $x>y$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9fa47-119">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9fa47-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="9fa47-120">참조 항목</span><span class="sxs-lookup"><span data-stu-id="9fa47-120">References</span></span>

- <span data-ttu-id="9fa47-121">새 퀀텀 ripple-A. Cuccaro, Thomas G. Draper, Samuel, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184</span><span class="sxs-lookup"><span data-stu-id="9fa47-121">A new quantum ripple-carry addition circuit Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184</span></span>