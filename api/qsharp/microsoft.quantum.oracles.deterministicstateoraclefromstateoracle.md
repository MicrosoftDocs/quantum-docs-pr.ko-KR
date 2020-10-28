---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: DeterministicStateOracleFromStateOracle 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: 539cc56e7ae4ead6654aaaae5353a771e06d2bfb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724253"
---
# <a name="deterministicstateoraclefromstateoracle-function"></a>DeterministicStateOracleFromStateOracle 함수

네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)

패키지 [](https://nuget.org/packages/)


형식의 oracle `StateOracle` 을로 변환 `DeterministicStateOracle` 합니다.

```qsharp
function DeterministicStateOracleFromStateOracle (idxFlagQubit : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle) : Microsoft.Quantum.Oracles.DeterministicStateOracle
```


## <a name="input"></a>입력

### <a name="idxflagqubit--int"></a>Idx플래그 [Int](xref:microsoft.quantum.lang-ref.int)

`stateOracle`두 레지스터에 대해 명시적으로 동작 하는 $A $의 플래그의 인덱스입니다. 플래그 $f $와 system $s $ (예: $A \ket {0} \_ f\ket {\ psi} \_ s $)입니다.


### <a name="stateoracle--stateoracle"></a>stateOracle: [Stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)

형식의 상태 준비 oracle $A `StateOracle` 입니다.



## <a name="output--deterministicstateoracle"></a>출력: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Oracle $A $와 같은 상태를 준비 하지만, 이제는 `DeterministicStateOracle` $a, s $는 더 이상 명시적으로 구분 되지 않습니다. 예를 들어  $A \ket{0\psi} \_ {as} $입니다.

## <a name="see-also"></a>참고 항목

- [Oracles. StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)
- [Oracles. DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)