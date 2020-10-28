---
uid: Microsoft.Quantum.MachineLearning.CombinedStructure
title: CombinedStructure 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CombinedStructure
qsharp.summary: Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.
ms.openlocfilehash: fbfd87761a40abe350e5f955fb53d8024eeb614e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720517"
---
# <a name="combinedstructure-function"></a>CombinedStructure 함수

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지 [](https://nuget.org/packages/)


하나 이상의 제어 되는 회전 계층이 지정 된 경우는 고유한 모델 매개 변수에 의해 고유 계층이 매개 변수화 되도록 모델 매개 변수 인덱스가 이동 된 단일 레이어를 반환 합니다.

```qsharp
function CombinedStructure (layers : Microsoft.Quantum.MachineLearning.ControlledRotation[][]) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>입력

### <a name="layers--controlledrotation"></a>레이어: [Controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[] []

결합할 계층입니다.



## <a name="output--controlledrotation"></a>출력: [Controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

다른 모든 계층의 연결을 나타내는 제어 되는 회전의 단일 계층입니다.