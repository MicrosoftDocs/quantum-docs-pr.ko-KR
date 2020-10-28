---
uid: Microsoft.Quantum.Intrinsic.Measure
title: 측정 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Measure
qsharp.summary: >-
  Performs a joint measurement of one or more qubits in the specified Pauli bases.

  The output result is given by the distribution: \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \frac12 \braket{ \psi \mid| \left( \boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_{N-1} \right) \mid| \psi }, \end{align} where $P_i$ is the $i$th element of `bases`, and where $N = \texttt{Length}(\texttt{bases})$. That is, measurement returns a `Result` $d$ such that the eigenvalue of the observed measurement effect is $(-1)^d$.
ms.openlocfilehash: 56ddfbe5e63692e477ad75bde6b1b16269ed20c0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711453"
---
# <a name="measure-operation"></a><span data-ttu-id="1ece7-102">측정 작업</span><span class="sxs-lookup"><span data-stu-id="1ece7-102">Measure operation</span></span>

<span data-ttu-id="1ece7-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="1ece7-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="1ece7-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1ece7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1ece7-105">지정 된 Pauli 기반에서 하나 이상의 값에 대 한 공동 측정을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ece7-105">Performs a joint measurement of one or more qubits in the specified Pauli bases.</span></span>

<span data-ttu-id="1ece7-106">출력 결과는 배포에 의해 제공 됩니다. \begin{align} \Pr (\texttt{Zero} | \ket{\psi}) = \frac12 \braket{\pr \pr | \pr (\boldone + P_0 \otime P_1 \ost\oatimes P_ {N-1} \pr) \pr | \pr}, \end{align} 여기서 $P _i $은의 $i $ th 요소이 `bases` 고 where $N = \texttt{Length} (\texttt{bases}) $입니다.</span><span class="sxs-lookup"><span data-stu-id="1ece7-106">The output result is given by the distribution: \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \frac12 \braket{ \psi \mid| \left( \boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_{N-1} \right) \mid| \psi }, \end{align} where $P_i$ is the $i$th element of `bases`, and where $N = \texttt{Length}(\texttt{bases})$.</span></span>
<span data-ttu-id="1ece7-107">즉, 측정값은 `Result` 관찰 된 측정 효과의 eigenvalue가 $ (-1) ^ d $ 인 $d $를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ece7-107">That is, measurement returns a `Result` $d$ such that the eigenvalue of the observed measurement effect is $(-1)^d$.</span></span>

```qsharp
operation Measure (bases : Pauli[], qubits : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="1ece7-108">입력</span><span class="sxs-lookup"><span data-stu-id="1ece7-108">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="1ece7-109">기본: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="1ece7-109">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="1ece7-110">각 텐서에 대 한 제품 요소를 나타내는 단일 값의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="1ece7-110">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="1ece7-111">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="1ece7-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="1ece7-112">측정할 비트의 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="1ece7-112">Register of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="1ece7-113">출력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="1ece7-113">Output : __invalid<Result>__</span></span>

<span data-ttu-id="1ece7-114">`Zero` $ + $1 eigenvalue가 관찰 되 면이 고, `One` $-$1 eigenvalue가 관찰 되 면입니다.</span><span class="sxs-lookup"><span data-stu-id="1ece7-114">`Zero` if the $+1$ eigenvalue is observed, and `One` if the $-1$ eigenvalue is observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ece7-115">설명</span><span class="sxs-lookup"><span data-stu-id="1ece7-115">Remarks</span></span>

<span data-ttu-id="1ece7-116">기본 배열 및 기본 비트 배열의 길이가 다른 경우 작업이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ece7-116">If the basis array and qubit array are different lengths, then the operation will fail.</span></span>