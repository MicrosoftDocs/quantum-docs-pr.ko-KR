---
uid: Microsoft.Quantum.MachineLearning.CyclicEntanglingLayer
title: CyclicEntanglingLayer 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CyclicEntanglingLayer
qsharp.summary: Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.
ms.openlocfilehash: 5421765e36ef3e8e744e118206dafcb2bb582cc2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211936"
---
# <a name="cyclicentanglinglayer-function"></a><span data-ttu-id="e9f46-102">CyclicEntanglingLayer 함수</span><span class="sxs-lookup"><span data-stu-id="e9f46-102">CyclicEntanglingLayer function</span></span>

<span data-ttu-id="e9f46-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="e9f46-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="e9f46-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="e9f46-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="e9f46-105">지정 된 축을 따라 단일 제어 회전의 배열을 반환 하 고,이를 통해 주기적의 레지스터를 정렬 하 고, 고유 모델 매개 변수에 의해 매개 변수화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9f46-105">Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.</span></span>

```qsharp
function CyclicEntanglingLayer (nQubits : Int, axis : Pauli, stride : Int) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="e9f46-106">입력</span><span class="sxs-lookup"><span data-stu-id="e9f46-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="e9f46-107">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e9f46-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e9f46-108">지정 된 계층에 의해 처리 되는의 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f46-108">The number of qubits acted on by the given layer.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="e9f46-109">축: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="e9f46-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="e9f46-110">지정 된 계층의 각 회전에 대 한 회전 축입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f46-110">The rotation axis for each rotation in the given layer.</span></span>


### <a name="stride--int"></a><span data-ttu-id="e9f46-111">stride: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e9f46-111">stride : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e9f46-112">각 회전에 대해 대상과 컨트롤 인덱스를 분리 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f46-112">The separation between the target and control indices for each rotation.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="e9f46-113">출력: [Controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="e9f46-113">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="e9f46-114">주기적의 레지스터를 중심으로 하는 두 개의 고 비트 제어 되는 회전의 배열입니다 `nQubits` .</span><span class="sxs-lookup"><span data-stu-id="e9f46-114">An array of two-qubit controlled rotations laid out cyclically across a register of `nQubits` qubits.</span></span>