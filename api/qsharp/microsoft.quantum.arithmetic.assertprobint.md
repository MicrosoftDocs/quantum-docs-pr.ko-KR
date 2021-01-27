---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: AssertProbInt 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: 85ff04bbad9dc2ed0f803db65508fdfbb0d22c56
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843397"
---
# <a name="assertprobint-operation"></a><span data-ttu-id="0f5df-102">AssertProbInt 작업</span><span class="sxs-lookup"><span data-stu-id="0f5df-102">AssertProbInt operation</span></span>

<span data-ttu-id="0f5df-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0f5df-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0f5df-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0f5df-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0f5df-105">퀀텀 레지스터의 특정 상태에 대 한 확률이 예상 값을 가지는 것을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5df-105">Asserts that the probability of a specific state of a quantum register has the expected value.</span></span>

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="0f5df-106">설명</span><span class="sxs-lookup"><span data-stu-id="0f5df-106">Description</span></span>

<span data-ttu-id="0f5df-107">$N $-stbit 퀀텀 상태 $ \ket{\psi} = \sum ^ {2 ^ n-1} _ {j = 0} \ alpha_j \ket{j} $로 지정 된 상태 $ \ket{j} $ $j 인덱싱된 상태 $ $의 확률 $ | \ alpha_j | ^ 2 $에 필요한 값이 있음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5df-107">Given an $n$-qubit quantum state $\ket{\psi}=\sum^{2^n-1}_{j=0}\alpha_j \ket{j}$, asserts that the probability $|\alpha_j|^2$ of the state $\ket{j}$ indexed by $j$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="0f5df-108">입력</span><span class="sxs-lookup"><span data-stu-id="0f5df-108">Input</span></span>

### <a name="stateindex--int"></a><span data-ttu-id="0f5df-109">stateIndex: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0f5df-109">stateIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0f5df-110">레지스터가 나타내는 $ \ket{j} $ 상태의 인덱스 $j $입니다 `LittleEndian` .</span><span class="sxs-lookup"><span data-stu-id="0f5df-110">The index $j$ of the state $\ket{j}$ represented by a `LittleEndian` register.</span></span>


### <a name="expected--double"></a><span data-ttu-id="0f5df-111">예상: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0f5df-111">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0f5df-112">예상 값은 $ | \ alpha_j | ^ 2 $입니다.</span><span class="sxs-lookup"><span data-stu-id="0f5df-112">The expected value of $|\alpha_j|^2$.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="0f5df-113">작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0f5df-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0f5df-114">$ \Ket{\psi} $를 거의 endian 형식으로 저장 하는?</span><span class="sxs-lookup"><span data-stu-id="0f5df-114">The qubit register that stores $\ket{\psi}$ in little-endian format.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="0f5df-115">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0f5df-115">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0f5df-116">실제 및 예상의 차이에 대 한 절대 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="0f5df-116">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0f5df-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0f5df-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="0f5df-118">예</span><span class="sxs-lookup"><span data-stu-id="0f5df-118">Example</span></span>

<span data-ttu-id="0f5df-119">`qubits`레지스터가 3abit 퀀텀 상태 $ \ket{\psi} = \ sqrt {1/8} \ k {0} + \ sqrt {7/8} \ k $를 거의 endian 형식으로 인코드 한다고 가정 합니다 {6} .</span><span class="sxs-lookup"><span data-stu-id="0f5df-119">Suppose that the `qubits` register encodes a 3-qubit quantum state $\ket{\psi}=\sqrt{1/8}\ket{0}+\sqrt{7/8}\ket{6}$ in little-endian format.</span></span>
<span data-ttu-id="0f5df-120">즉, 숫자는 $ \ket {0} \equiv\ket {0} \ket {0} \ket {0} $ 및 $ \ket \equiv\ket \ket {6} {0} \ket $로 표시 {1} {1} 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f5df-120">This means that the number states $\ket{0}\equiv\ket{0}\ket{0}\ket{0}$ and $\ket{6}\equiv\ket{0}\ket{1}\ket{1}$.</span></span> <span data-ttu-id="0f5df-121">그러면 다음 어설션이 성공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5df-121">Then the following asserts succeed:</span></span>

```qsharp
AssertProbInt(0, 0.125, qubits, 10e-10);
AssertProbInt(6, 0.875, qubits, 10e-10);
```