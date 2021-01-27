---
uid: Microsoft.Quantum.AmplitudeAmplification.TargetStateReflectionOracle
title: TargetStateReflectionOracle 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: TargetStateReflectionOracle
qsharp.summary: >-
  Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.

  The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.
ms.openlocfilehash: 4169ccf3e210e27f779311553b845ea04f2c7dc6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843901"
---
# <a name="targetstatereflectionoracle-function"></a>TargetStateReflectionOracle 함수

네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


플래그에 `ReflectionOracle` 따라 고유 하 게 표시 되는 대상 상태에 대 한를 생성 합니다.

대상 상태에는 1로 설정 된 단일 비트와 다른 모든 0: $ \ket {1} _f $가 있습니다.

```qsharp
function TargetStateReflectionOracle (idxFlagQubit : Int) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="input"></a>입력

### <a name="idxflagqubit--int"></a>Idx플래그 [](xref:microsoft.quantum.lang-ref.int)

Oracle의 플래그를 지정 하는 $f의 인덱스입니다.



## <a name="output--reflectionoracle"></a>출력: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

`ReflectionOracle`$ \Ket _f $로 표시 된 상태에 대해 반영 하는입니다 {1} .

## <a name="see-also"></a>참고 항목

- [ReflectionOracle입니다.](xref:Microsoft.Quantum.Canon.ReflectionOracle)