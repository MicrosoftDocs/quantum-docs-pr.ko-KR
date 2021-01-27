---
uid: Microsoft.Quantum.MachineLearning.PartialRotationsLayer
title: PartialRotationsLayer 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: PartialRotationsLayer
qsharp.summary: Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.
ms.openlocfilehash: e230df9b28c59e1d532d5b36adf90efa01f0f33e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852930"
---
# <a name="partialrotationslayer-function"></a><span data-ttu-id="ced92-102">PartialRotationsLayer 함수</span><span class="sxs-lookup"><span data-stu-id="ced92-102">PartialRotationsLayer function</span></span>

<span data-ttu-id="ced92-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ced92-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="ced92-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ced92-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="ced92-105">고유 모델 매개 변수에 의해 매개 변수화 된 지정 된 축을 따라 단일가 비트 회전의 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ced92-105">Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.</span></span>

```qsharp
function PartialRotationsLayer (idxsQubits : Int[], axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="ced92-106">입력</span><span class="sxs-lookup"><span data-stu-id="ced92-106">Input</span></span>

### <a name="idxsqubits--int"></a><span data-ttu-id="ced92-107">idxsQubits: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ced92-107">idxsQubits : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ced92-108">각 회전의 대상으로 사용할 비트의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="ced92-108">Indices for the qubits to be used as the targets for each rotation.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="ced92-109">축: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="ced92-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="ced92-110">지정 된 계층의 각 회전에 대 한 회전 축입니다.</span><span class="sxs-lookup"><span data-stu-id="ced92-110">The rotation axis for each rotation in the given layer.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="ced92-111">출력: [Controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="ced92-111">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="ced92-112">지정 된 축에 대 한 제어 되는 회전의 배열입니다. 각 비트에 하나씩 `nQubits` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ced92-112">An array of controlled rotations about the given axis, one on each of `nQubits` qubits.</span></span>