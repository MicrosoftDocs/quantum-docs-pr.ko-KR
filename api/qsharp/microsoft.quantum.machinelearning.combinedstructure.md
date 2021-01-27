---
uid: Microsoft.Quantum.MachineLearning.CombinedStructure
title: CombinedStructure 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CombinedStructure
qsharp.summary: Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.
ms.openlocfilehash: b8ec007202c8e63dc2e98d0c752f6ba1a453e236
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847411"
---
# <a name="combinedstructure-function"></a><span data-ttu-id="462a4-102">CombinedStructure 함수</span><span class="sxs-lookup"><span data-stu-id="462a4-102">CombinedStructure function</span></span>

<span data-ttu-id="462a4-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="462a4-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="462a4-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="462a4-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="462a4-105">하나 이상의 제어 되는 회전 계층이 지정 된 경우는 고유한 모델 매개 변수에 의해 고유 계층이 매개 변수화 되도록 모델 매개 변수 인덱스가 이동 된 단일 레이어를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="462a4-105">Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.</span></span>

```qsharp
function CombinedStructure (layers : Microsoft.Quantum.MachineLearning.ControlledRotation[][]) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="462a4-106">입력</span><span class="sxs-lookup"><span data-stu-id="462a4-106">Input</span></span>

### <a name="layers--controlledrotation"></a><span data-ttu-id="462a4-107">레이어: [Controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[] []</span><span class="sxs-lookup"><span data-stu-id="462a4-107">layers : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[][]</span></span>

<span data-ttu-id="462a4-108">결합할 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="462a4-108">The layers to be combined.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="462a4-109">출력: [Controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="462a4-109">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="462a4-110">다른 모든 계층의 연결을 나타내는 제어 되는 회전의 단일 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="462a4-110">A single layer of controlled rotations, representing the concatenation of all other layers.</span></span>

## <a name="example"></a><span data-ttu-id="462a4-111">예</span><span class="sxs-lookup"><span data-stu-id="462a4-111">Example</span></span>

<span data-ttu-id="462a4-112">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="462a4-112">The following are equivalent:</span></span>

```qsharp
let structure = CombinedStructure([
    LocalRotationLayer(2, PauliY),
    CyclicEntanglingLayer(3, PauliX, 2)
]);
let structure = [
    ControlledRotation((0, new Int[0]), PauliY, 0),
    ControlledRotation((1, new Int[0]), PauliY, 1),
    ControlledRotation((0, [2]), PauliX, 2),
    ControlledRotation((1, [0]), PauliX, 3),
    ControlledRotation((2, [1]), PauliX, 4)
];
```