---
uid: Microsoft.Quantum.Intrinsic.Exp
title: Exp 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Exp
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator.

  \begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: b923374a954f90aba2deaead79dd419fbf67fea3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711523"
---
# <a name="exp-operation"></a><span data-ttu-id="744a9-102">Exp 작업</span><span class="sxs-lookup"><span data-stu-id="744a9-102">Exp operation</span></span>

<span data-ttu-id="744a9-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="744a9-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="744a9-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="744a9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="744a9-105">다중값 비트 Pauli 연산자의 지 수를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="744a9-105">Applies the exponential of a multi-qubit Pauli operator.</span></span>

<span data-ttu-id="744a9-106">\begin{align} e ^ {i \theta [P_0 \otime P_1 \coP_ {N-1}]}, \end{align} $P _i $은의 $i $ th 요소 `paulis` 이며 where $N = $입니다 `Length(paulis)` .</span><span class="sxs-lookup"><span data-stu-id="744a9-106">\begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.</span></span>

```qsharp
operation Exp (paulis : Pauli[], theta : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="744a9-107">입력</span><span class="sxs-lookup"><span data-stu-id="744a9-107">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="744a9-108">paulis: [Paulis](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="744a9-108">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="744a9-109">각 텐서에 대 한 제품 요소를 나타내는 단일 값의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="744a9-109">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="theta--double"></a><span data-ttu-id="744a9-110">테타: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="744a9-110">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="744a9-111">대상 레지스터를 회전 하는 데 사용한 지정 된 다중 기능 비트 Pauli 연산자의 각도입니다.</span><span class="sxs-lookup"><span data-stu-id="744a9-111">Angle about the given multi-qubit Pauli operator by which the target register is to be rotated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="744a9-112">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="744a9-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="744a9-113">지정 된 회전을에 적용 하려면 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="744a9-113">Register to apply the given rotation to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="744a9-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="744a9-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

