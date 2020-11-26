---
uid: Microsoft.Quantum.Diagnostics._flipToBasis
title: _flipToBasis 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _flipToBasis
qsharp.summary: >-
  Applies unitaries that map $\ket{0}\otimes\cdots\ket{0}$ to $\ket{\psi_0} \otimes \ket{\psi_{n - 1}}$, where $\ket{\psi_k}$ depends on `basis[k]`.

  The correspondence between value of `basis[k]` and $\ket{\psi_k}$ is the following:

  - `basis[k]=0` $\rightarrow \ket{0}$. - `basis[k]=1` $\rightarrow \ket{1}$. - `basis[k]=2` $\rightarrow \ket{+}$. - `basis[k]=3` $\rightarrow \ket{i}$ ( +1 eigenstate of Pauli Y ).
ms.openlocfilehash: 1581a1267902ceee81d6f01348f4ee718e49ee47
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223989"
---
# <a name="_fliptobasis-operation"></a><span data-ttu-id="1a3cd-102">_flipToBasis 작업</span><span class="sxs-lookup"><span data-stu-id="1a3cd-102">_flipToBasis operation</span></span>

<span data-ttu-id="1a3cd-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="1a3cd-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="1a3cd-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="1a3cd-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="1a3cd-105">$ \Ket {0} \otimes\cdots\ket {0} $를 $ \ket{\ psi_0} \otimes \ket{\ psi_ {n-1}} $로 매핑하는 unitaries을 적용 합니다. 여기서 $ \ket{\ psi_k} $은에 종속 `basis[k]` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3cd-105">Applies unitaries that map $\ket{0}\otimes\cdots\ket{0}$ to $\ket{\psi_0} \otimes \ket{\psi_{n - 1}}$, where $\ket{\psi_k}$ depends on `basis[k]`.</span></span>

<span data-ttu-id="1a3cd-106">Value `basis[k]` 와 $ \ket{\ psi_k} $ 사이의 대응은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3cd-106">The correspondence between value of `basis[k]` and $\ket{\psi_k}$ is the following:</span></span>

- <span data-ttu-id="1a3cd-107">`basis[k]=0` $ \rightarrow \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="1a3cd-107">`basis[k]=0` $\rightarrow \ket{0}$.</span></span>
- <span data-ttu-id="1a3cd-108">`basis[k]=1` $ \rightarrow \ket {1} $.</span><span class="sxs-lookup"><span data-stu-id="1a3cd-108">`basis[k]=1` $\rightarrow \ket{1}$.</span></span>
- <span data-ttu-id="1a3cd-109">`basis[k]=2` $ \rightarrow \ket{+} $.</span><span class="sxs-lookup"><span data-stu-id="1a3cd-109">`basis[k]=2` $\rightarrow \ket{+}$.</span></span>
- <span data-ttu-id="1a3cd-110">`basis[k]=3` $ \rightarrow \ket{i} $ (+ 1 eigenstate Y의 1 eigenstate)</span><span class="sxs-lookup"><span data-stu-id="1a3cd-110">`basis[k]=3` $\rightarrow \ket{i}$ ( +1 eigenstate of Pauli Y ).</span></span>

```qsharp
operation _flipToBasis (basis : Int[], qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="1a3cd-111">입력</span><span class="sxs-lookup"><span data-stu-id="1a3cd-111">Input</span></span>

### <a name="basis--int"></a><span data-ttu-id="1a3cd-112">기본: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1a3cd-112">basis : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="1a3cd-113">단일 비트 기준 상태 Id의 배열 (0 <= id <= 3), 각 요소에 대해 하나씩입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3cd-113">Array of single-qubit basis state IDs (0 <= id <= 3), one for each element of qubits.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="1a3cd-114">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="1a3cd-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="1a3cd-115">연산을 수행할 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3cd-115">Qubit to be operated on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1a3cd-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1a3cd-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

