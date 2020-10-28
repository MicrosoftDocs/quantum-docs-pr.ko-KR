---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace
title: AssertOperationsEqualInPlace 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlace
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).

  This assertion uses $n$ qubits and requires multiple calls of the operations being compared.
ms.openlocfilehash: 407a139da816281346eb06849f81e91b83202653
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712972"
---
# <a name="assertoperationsequalinplace-operation"></a><span data-ttu-id="ea05c-102">AssertOperationsEqualInPlace 작업</span><span class="sxs-lookup"><span data-stu-id="ea05c-102">AssertOperationsEqualInPlace operation</span></span>

<span data-ttu-id="ea05c-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="ea05c-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="ea05c-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ea05c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ea05c-105">두 작업이 지정 된 경우는 모든 입력 상태에 대해 동일 하 게 작동 한다는 것을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea05c-105">Given two operations, asserts that they act identically for all input states.</span></span>

<span data-ttu-id="ea05c-106">이 어설션은 \ket $V의 모든 상태에 대 한 작업의 동작을 확인 하 여 구현 됩니다 .이 경우에는 _0\otime ... \otimes V_ {n-1} $로 설정 합니다. 여기서 $V _k $은 $ {0} $, $ \ket {1} $, $ \ket{+} $ 및 $ \ket{i} $ (+ 1 Eigenstate)의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="ea05c-106">This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).</span></span>

<span data-ttu-id="ea05c-107">이 어설션은 $ opbits $n를 사용 하 고 비교 되는 작업을 여러 번 호출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea05c-107">This assertion uses $n$ qubits and requires multiple calls of the operations being compared.</span></span>

```qsharp
operation AssertOperationsEqualInPlace (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="ea05c-108">입력</span><span class="sxs-lookup"><span data-stu-id="ea05c-108">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="ea05c-109">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ea05c-109">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ea05c-110">작업이 수행 하 고 작동 하는 $n $의 수입니다 `givenU` `expectedU` .</span><span class="sxs-lookup"><span data-stu-id="ea05c-110">The number of qubits $n$ that the operations `givenU` and `expectedU` operate on.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="ea05c-111">givenU: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ea05c-111">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ea05c-112">검사 될 $ 이상 비트 $n에 대 한 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="ea05c-112">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit-adj"></a><span data-ttu-id="ea05c-113">Adj Unit [()](xref:microsoft.quantum.lang-ref.qubit)=> [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ea05c-113">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="ea05c-114">비교할 $로 비트 $n에 대 한 참조 연산 `givenU` 입니다.</span><span class="sxs-lookup"><span data-stu-id="ea05c-114">Reference operation on $n$ qubits that `givenU` is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ea05c-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ea05c-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="ea05c-116">참조</span><span class="sxs-lookup"><span data-stu-id="ea05c-116">References</span></span>

<span data-ttu-id="ea05c-117">$ \Ket {0} $, $ \ket {1} $, $ \ket{+} $ 및 $ \ket{i} $ 상태의 기준은 [ *Chuang,*](https://arxiv.org/abs/quant-ph/9610001)Nielsen에 설명 된 Chuang-Nielsen 기준입니다.</span><span class="sxs-lookup"><span data-stu-id="ea05c-117">The basis of states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ is the Chuang-Nielsen basis, described in [ *I. L. Chuang, M. A. Nielsen* ](https://arxiv.org/abs/quant-ph/9610001).</span></span>

## <a name="see-also"></a><span data-ttu-id="ea05c-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ea05c-118">See Also</span></span>

- [<span data-ttu-id="ea05c-119">AssertOperationsEqualReferenced.</span><span class="sxs-lookup"><span data-stu-id="ea05c-119">Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced)