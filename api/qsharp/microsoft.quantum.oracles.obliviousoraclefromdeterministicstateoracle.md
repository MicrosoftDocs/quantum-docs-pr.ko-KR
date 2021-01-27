---
uid: Microsoft.Quantum.Oracles.ObliviousOracleFromDeterministicStateOracle
title: ObliviousOracleFromDeterministicStateOracle 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracleFromDeterministicStateOracle
qsharp.summary: Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.
ms.openlocfilehash: c7aa80feda67d68216f318073ee8c6a5eb0653c0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854520"
---
# <a name="obliviousoraclefromdeterministicstateoracle-function"></a>ObliviousOracleFromDeterministicStateOracle 함수

네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


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