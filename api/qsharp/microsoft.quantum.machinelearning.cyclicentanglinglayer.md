---
uid: Microsoft.Quantum.MachineLearning.CyclicEntanglingLayer
title: CyclicEntanglingLayer 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CyclicEntanglingLayer
qsharp.summary: Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.
ms.openlocfilehash: 5d0af0a60217b69dc7eb8ece8952f2a7f0c09280
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847375"
---
# <a name="cyclicentanglinglayer-function"></a><span data-ttu-id="d19cc-102">CyclicEntanglingLayer 함수</span><span class="sxs-lookup"><span data-stu-id="d19cc-102">CyclicEntanglingLayer function</span></span>

<span data-ttu-id="d19cc-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d19cc-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="d19cc-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d19cc-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="d19cc-105">지정 된 축을 따라 단일 제어 회전의 배열을 반환 하 고,이를 통해 주기적의 레지스터를 정렬 하 고, 고유 모델 매개 변수에 의해 매개 변수화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d19cc-105">Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.</span></span>

```qsharp
function CyclicEntanglingLayer (nQubits : Int, axis : Pauli, stride : Int) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="d19cc-106">입력</span><span class="sxs-lookup"><span data-stu-id="d19cc-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="d19cc-107">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d19cc-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d19cc-108">지정 된 계층에 의해 처리 되는의 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d19cc-108">The number of qubits acted on by the given layer.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="d19cc-109">축: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="d19cc-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="d19cc-110">지정 된 계층의 각 회전에 대 한 회전 축입니다.</span><span class="sxs-lookup"><span data-stu-id="d19cc-110">The rotation axis for each rotation in the given layer.</span></span>


### <a name="stride--int"></a><span data-ttu-id="d19cc-111">stride: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d19cc-111">stride : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d19cc-112">각 회전에 대해 대상과 컨트롤 인덱스를 분리 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d19cc-112">The separation between the target and control indices for each rotation.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="d19cc-113">출력: [Controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="d19cc-113">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="d19cc-114">주기적의 레지스터를 중심으로 하는 두 개의 고 비트 제어 되는 회전의 배열입니다 `nQubits` .</span><span class="sxs-lookup"><span data-stu-id="d19cc-114">An array of two-qubit controlled rotations laid out cyclically across a register of `nQubits` qubits.</span></span>

## <a name="example"></a><span data-ttu-id="d19cc-115">예</span><span class="sxs-lookup"><span data-stu-id="d19cc-115">Example</span></span>

<span data-ttu-id="d19cc-116">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="d19cc-116">The following are equivalent:</span></span>

```qsharp
let layer = CyclicEntanglingLayer(3, PauliX, 2);
let layer = [
    ControlledRotation((0, [2]), PauliX, 0),
    ControlledRotation((1, [0]), PauliX, 1),
    ControlledRotation((2, [1]), PauliX, 2)
];
```