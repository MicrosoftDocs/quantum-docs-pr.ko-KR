---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: AssertProbInt 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: a8e4217e18528adc0aa9923f1c0dcfb59e1d2488
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721364"
---
# <a name="assertprobint-operation"></a><span data-ttu-id="0ad14-102">AssertProbInt 작업</span><span class="sxs-lookup"><span data-stu-id="0ad14-102">AssertProbInt operation</span></span>

<span data-ttu-id="0ad14-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0ad14-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0ad14-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0ad14-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0ad14-105">퀀텀 레지스터의 특정 상태에 대 한 확률이 예상 값을 가지는 것을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad14-105">Asserts that the probability of a specific state of a quantum register has the expected value.</span></span>

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="0ad14-106">Description</span><span class="sxs-lookup"><span data-stu-id="0ad14-106">Description</span></span>

<span data-ttu-id="0ad14-107">$N $-stbit 퀀텀 상태 $ \ket{\psi} = \sum ^ {2 ^ n-1} _ {j = 0} \ alpha_j \ket{j} $로 지정 된 상태 $ \ket{j} $ $j 인덱싱된 상태 $ $의 확률 $ | \ alpha_j | ^ 2 $에 필요한 값이 있음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad14-107">Given an $n$-qubit quantum state $\ket{\psi}=\sum^{2^n-1}_{j=0}\alpha_j \ket{j}$, asserts that the probability $|\alpha_j|^2$ of the state $\ket{j}$ indexed by $j$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="0ad14-108">입력</span><span class="sxs-lookup"><span data-stu-id="0ad14-108">Input</span></span>

### <a name="stateindex--int"></a><span data-ttu-id="0ad14-109">stateIndex: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0ad14-109">stateIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0ad14-110">레지스터가 나타내는 $ \ket{j} $ 상태의 인덱스 $j $입니다 `LittleEndian` .</span><span class="sxs-lookup"><span data-stu-id="0ad14-110">The index $j$ of the state $\ket{j}$ represented by a `LittleEndian` register.</span></span>


### <a name="expected--double"></a><span data-ttu-id="0ad14-111">예상: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0ad14-111">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0ad14-112">예상 값은 $ | \ alpha_j | ^ 2 $입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad14-112">The expected value of $|\alpha_j|^2$.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="0ad14-113">작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0ad14-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0ad14-114">$ \Ket{\psi} $를 거의 endian 형식으로 저장 하는?</span><span class="sxs-lookup"><span data-stu-id="0ad14-114">The qubit register that stores $\ket{\psi}$ in little-endian format.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="0ad14-115">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0ad14-115">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0ad14-116">실제 및 예상의 차이에 대 한 절대 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad14-116">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0ad14-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0ad14-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

