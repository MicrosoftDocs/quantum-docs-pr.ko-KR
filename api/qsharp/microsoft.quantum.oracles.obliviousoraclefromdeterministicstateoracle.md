---
uid: Microsoft.Quantum.Oracles.ObliviousOracleFromDeterministicStateOracle
title: ObliviousOracleFromDeterministicStateOracle 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracleFromDeterministicStateOracle
qsharp.summary: Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.
ms.openlocfilehash: 9e18776ad4d6adf0068213117c6d1d8ed5c5f126
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722223"
---
# <a name="obliviousoraclefromdeterministicstateoracle-function"></a>ObliviousOracleFromDeterministicStateOracle 함수

네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)

패키지 [](https://nuget.org/packages/)


Oracles와를 결합 합니다 `DeterministicStateOracle` `ObliviousOracle` .

```qsharp
function ObliviousOracleFromDeterministicStateOracle (ancillaOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle) : Microsoft.Quantum.Oracles.ObliviousOracle
```


## <a name="input"></a>입력

### <a name="ancillaoracle--deterministicstateoracle"></a>[DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle) Illaoracle:

등록 $a $에서 동작 하는 형식의 상태 준비 oracle $A $ `DeterministicStateOracle` .


### <a name="signaloracle--obliviousoracle"></a>signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

`ObliviousOracle`Register $a, s $에 대해 공동으로 동작 하는 유형의 oracle $U $입니다.



## <a name="output--obliviousoracle"></a>출력: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

유형의 oracle $O = UA $ `ObliviousOracle` 입니다.

## <a name="see-also"></a>참고 항목

- [Oracles. DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [Oracles. ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)