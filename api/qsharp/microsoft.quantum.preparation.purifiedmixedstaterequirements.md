---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements
title: PurifiedMixedStateRequirements 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateRequirements
qsharp.summary: Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".
ms.openlocfilehash: 9b8861a4112c4e6c9db994339353c771a3de81a6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229990"
---
# <a name="purifiedmixedstaterequirements-function"></a>PurifiedMixedStateRequirements 함수

네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


에서 반환 하는 작업을 적용 하기 위해 할당 해야 하는 총 비트 수를 반환 합니다 @"microsoft.quantum.preparation.purifiedmixedstate" .

```qsharp
function PurifiedMixedStateRequirements (targetError : Double, nCoefficients : Int) : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
```


## <a name="input"></a>입력

### <a name="targeterror--double"></a>targetError: [Double](xref:microsoft.quantum.lang-ref.double)

$ \Epsilon $ 대상 오류입니다.


### <a name="ncoefficients--int"></a>nCoefficients: [Int](xref:microsoft.quantum.lang-ref.int)

혼합 상태를 준비할 때 지정할 계수 수입니다.



## <a name="output--mixedstatepreparationrequirements"></a>출력: [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)

함수에서 사용 하는 각 인덱스 및 가비지 레지스터와 총에 필요한 수의 수에 대 한 설명입니다 @"microsoft.quantum.preparation.purifiedmixedstate" .

## <a name="see-also"></a>참고 항목

- [PurifiedMixedState.](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)