---
uid: Microsoft.Quantum.MachineLearning.CombinedStructure
title: CombinedStructure 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CombinedStructure
qsharp.summary: Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.
ms.openlocfilehash: 0a7d66be8b45d6a9df95b425e66b9b6bba241136
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211970"
---
# <a name="combinedstructure-function"></a><span data-ttu-id="a3bfc-102">CombinedStructure 함수</span><span class="sxs-lookup"><span data-stu-id="a3bfc-102">CombinedStructure function</span></span>

<span data-ttu-id="a3bfc-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="a3bfc-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="a3bfc-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="a3bfc-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="a3bfc-105">하나 이상의 제어 되는 회전 계층이 지정 된 경우는 고유한 모델 매개 변수에 의해 고유 계층이 매개 변수화 되도록 모델 매개 변수 인덱스가 이동 된 단일 레이어를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3bfc-105">Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.</span></span>

```qsharp
function CombinedStructure (layers : Microsoft.Quantum.MachineLearning.ControlledRotation[][]) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="a3bfc-106">입력</span><span class="sxs-lookup"><span data-stu-id="a3bfc-106">Input</span></span>

### <a name="layers--controlledrotation"></a><span data-ttu-id="a3bfc-107">레이어: [Controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[] []</span><span class="sxs-lookup"><span data-stu-id="a3bfc-107">layers : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[][]</span></span>

<span data-ttu-id="a3bfc-108">결합할 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="a3bfc-108">The layers to be combined.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="a3bfc-109">출력: [Controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="a3bfc-109">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="a3bfc-110">다른 모든 계층의 연결을 나타내는 제어 되는 회전의 단일 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="a3bfc-110">A single layer of controlled rotations, representing the concatenation of all other layers.</span></span>