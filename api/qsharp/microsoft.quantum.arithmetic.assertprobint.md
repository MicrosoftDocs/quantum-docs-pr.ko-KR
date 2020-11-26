---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: AssertProbInt 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: b95c2c6294dd5a95b7215c22bd6c50a41635f432
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223700"
---
# <a name="assertprobint-operation"></a><span data-ttu-id="9fba5-102">AssertProbInt 작업</span><span class="sxs-lookup"><span data-stu-id="9fba5-102">AssertProbInt operation</span></span>

<span data-ttu-id="9fba5-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9fba5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9fba5-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9fba5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9fba5-105">퀀텀 레지스터의 특정 상태에 대 한 확률이 예상 값을 가지는 것을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fba5-105">Asserts that the probability of a specific state of a quantum register has the expected value.</span></span>

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="9fba5-106">Description</span><span class="sxs-lookup"><span data-stu-id="9fba5-106">Description</span></span>

<span data-ttu-id="9fba5-107">$N $-stbit 퀀텀 상태 $ \ket{\psi} = \sum ^ {2 ^ n-1} _ {j = 0} \ alpha_j \ket{j} $로 지정 된 상태 $ \ket{j} $ $j 인덱싱된 상태 $ $의 확률 $ | \ alpha_j | ^ 2 $에 필요한 값이 있음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fba5-107">Given an $n$-qubit quantum state $\ket{\psi}=\sum^{2^n-1}_{j=0}\alpha_j \ket{j}$, asserts that the probability $|\alpha_j|^2$ of the state $\ket{j}$ indexed by $j$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="9fba5-108">입력</span><span class="sxs-lookup"><span data-stu-id="9fba5-108">Input</span></span>

### <a name="stateindex--int"></a><span data-ttu-id="9fba5-109">stateIndex: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9fba5-109">stateIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9fba5-110">레지스터가 나타내는 $ \ket{j} $ 상태의 인덱스 $j $입니다 `LittleEndian` .</span><span class="sxs-lookup"><span data-stu-id="9fba5-110">The index $j$ of the state $\ket{j}$ represented by a `LittleEndian` register.</span></span>


### <a name="expected--double"></a><span data-ttu-id="9fba5-111">예상: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9fba5-111">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9fba5-112">예상 값은 $ | \ alpha_j | ^ 2 $입니다.</span><span class="sxs-lookup"><span data-stu-id="9fba5-112">The expected value of $|\alpha_j|^2$.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="9fba5-113">작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9fba5-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9fba5-114">$ \Ket{\psi} $를 거의 endian 형식으로 저장 하는?</span><span class="sxs-lookup"><span data-stu-id="9fba5-114">The qubit register that stores $\ket{\psi}$ in little-endian format.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="9fba5-115">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9fba5-115">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9fba5-116">실제 및 예상의 차이에 대 한 절대 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="9fba5-116">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9fba5-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9fba5-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

