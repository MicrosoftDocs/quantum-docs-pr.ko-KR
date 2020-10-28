---
uid: Microsoft.Quantum.Intrinsic.ExpFrac
title: ExpFrac 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ExpFrac
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.

  \begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: d11912a272387b087098f59e7ac071534b01c054
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711488"
---
# <a name="expfrac-operation"></a><span data-ttu-id="16da7-102">ExpFrac 작업</span><span class="sxs-lookup"><span data-stu-id="16da7-102">ExpFrac operation</span></span>

<span data-ttu-id="16da7-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="16da7-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="16da7-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="16da7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="16da7-105">Dyadic 분수로 지정 된 인수를 사용 하 여 다중 기능 비트 Pauli 연산자의 지 수를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="16da7-105">Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.</span></span>

<span data-ttu-id="16da7-106">\begin{align} e ^ {i \pi k [P_0 \otime P_1 \coP_ {N-1}]/2 ^ N}, \end{align} where $P _i $은의 $i $ th 요소 `paulis` 이며 where $N = $입니다 `Length(paulis)` .</span><span class="sxs-lookup"><span data-stu-id="16da7-106">\begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.</span></span>

```qsharp
operation ExpFrac (paulis : Pauli[], numerator : Int, power : Int, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="16da7-107">입력</span><span class="sxs-lookup"><span data-stu-id="16da7-107">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="16da7-108">paulis: [Paulis](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="16da7-108">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="16da7-109">각 텐서에 대 한 제품 요소를 나타내는 단일 값의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="16da7-109">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="numerator--int"></a><span data-ttu-id="16da7-110">분자: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="16da7-110">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="16da7-111">Dyadic 분수를 회전 하는 각도를 나타내는 분자 ($k $)입니다.</span><span class="sxs-lookup"><span data-stu-id="16da7-111">Numerator ($k$) in the dyadic fraction representation of the angle by which the qubit register is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="16da7-112">power: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="16da7-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="16da7-113">제곱 비트 레지스터를 회전할 각도의 분모를 지정 하는 두 ($n $)의 제곱입니다.</span><span class="sxs-lookup"><span data-stu-id="16da7-113">Power of two ($n$) specifying the denominator of the angle by which the qubit register is to be rotated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="16da7-114">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="16da7-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="16da7-115">지정 된 회전을에 적용 하려면 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="16da7-115">Register to apply the given rotation to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="16da7-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="16da7-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

