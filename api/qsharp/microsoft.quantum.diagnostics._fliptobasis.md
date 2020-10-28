---
uid: Microsoft.Quantum.Diagnostics._flipToBasis
title: _flipToBasis 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _flipToBasis
qsharp.summary: >-
  Applies unitaries that map $\ket{0}\otimes\cdots\ket{0}$ to $\ket{\psi_0} \otimes \ket{\psi_{n - 1}}$, where $\ket{\psi_k}$ depends on `basis[k]`.

  The correspondence between value of `basis[k]` and $\ket{\psi_k}$ is the following:

  - `basis[k]=0` $\rightarrow \ket{0}$. - `basis[k]=1` $\rightarrow \ket{1}$. - `basis[k]=2` $\rightarrow \ket{+}$. - `basis[k]=3` $\rightarrow \ket{i}$ ( +1 eigenstate of Pauli Y ).
ms.openlocfilehash: e074ed2ae259f6aef49a8d327ce518a9e2caebfa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713147"
---
# <a name="_fliptobasis-operation"></a><span data-ttu-id="d48e1-102">_flipToBasis 작업</span><span class="sxs-lookup"><span data-stu-id="d48e1-102">_flipToBasis operation</span></span>

<span data-ttu-id="d48e1-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="d48e1-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="d48e1-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d48e1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d48e1-105">$ \Ket {0} \otimes\cdots\ket {0} $를 $ \ket{\ psi_0} \otimes \ket{\ psi_ {n-1}} $로 매핑하는 unitaries을 적용 합니다. 여기서 $ \ket{\ psi_k} $은에 종속 `basis[k]` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d48e1-105">Applies unitaries that map $\ket{0}\otimes\cdots\ket{0}$ to $\ket{\psi_0} \otimes \ket{\psi_{n - 1}}$, where $\ket{\psi_k}$ depends on `basis[k]`.</span></span>

<span data-ttu-id="d48e1-106">Value `basis[k]` 와 $ \ket{\ psi_k} $ 사이의 대응은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d48e1-106">The correspondence between value of `basis[k]` and $\ket{\psi_k}$ is the following:</span></span>

- <span data-ttu-id="d48e1-107">`basis[k]=0` $ \rightarrow \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="d48e1-107">`basis[k]=0` $\rightarrow \ket{0}$.</span></span>
- <span data-ttu-id="d48e1-108">`basis[k]=1` $ \rightarrow \ket {1} $.</span><span class="sxs-lookup"><span data-stu-id="d48e1-108">`basis[k]=1` $\rightarrow \ket{1}$.</span></span>
- <span data-ttu-id="d48e1-109">`basis[k]=2` $ \rightarrow \ket{+} $.</span><span class="sxs-lookup"><span data-stu-id="d48e1-109">`basis[k]=2` $\rightarrow \ket{+}$.</span></span>
- <span data-ttu-id="d48e1-110">`basis[k]=3` $ \rightarrow \ket{i} $ (+ 1 eigenstate Y의 1 eigenstate)</span><span class="sxs-lookup"><span data-stu-id="d48e1-110">`basis[k]=3` $\rightarrow \ket{i}$ ( +1 eigenstate of Pauli Y ).</span></span>

```qsharp
operation _flipToBasis (basis : Int[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d48e1-111">입력</span><span class="sxs-lookup"><span data-stu-id="d48e1-111">Input</span></span>

### <a name="basis--int"></a><span data-ttu-id="d48e1-112">기본: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d48e1-112">basis : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="d48e1-113">단일 비트 기준 상태 Id의 배열 (0 <= id <= 3), 각 요소에 대해 하나씩입니다.</span><span class="sxs-lookup"><span data-stu-id="d48e1-113">Array of single-qubit basis state IDs (0 <= id <= 3), one for each element of qubits.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="d48e1-114">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d48e1-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d48e1-115">연산을 수행할 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="d48e1-115">Qubit to be operated on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d48e1-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d48e1-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

