---
uid: Microsoft.Quantum.AmplitudeAmplification.TargetStateReflectionOracle
title: TargetStateReflectionOracle 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: TargetStateReflectionOracle
qsharp.summary: >-
  Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.

  The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.
ms.openlocfilehash: 65ad316a6ac986ebd0dc28b25859026a60aa3239
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191111"
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

### <a name="idxflagqubit--int"></a>Idx플래그 [Int](xref:microsoft.quantum.lang-ref.int)

Oracle의 플래그를 지정 하는 $f의 인덱스입니다.



## <a name="output--reflectionoracle"></a>출력: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

`ReflectionOracle`$ \Ket _f $로 표시 된 상태에 대해 반영 하는입니다 {1} .

## <a name="see-also"></a>참고 항목

- [ReflectionOracle입니다.](xref:Microsoft.Quantum.Canon.ReflectionOracle)