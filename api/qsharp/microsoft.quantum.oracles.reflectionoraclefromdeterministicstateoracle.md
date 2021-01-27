---
uid: Microsoft.Quantum.Oracles.ReflectionOracleFromDeterministicStateOracle
title: ReflectionOracleFromDeterministicStateOracle 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracleFromDeterministicStateOracle
qsharp.summary: Constructs reflection about a given state from an oracle.
ms.openlocfilehash: c260bdbcdb2ce53ad602bf84e0d31ef4fec24a79
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842518"
---
# <a name="reflectionoraclefromdeterministicstateoracle-function"></a>ReflectionOracleFromDeterministicStateOracle 함수

네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


Oracle에서 지정 된 상태에 대 한 리플렉션을 생성 합니다.

```qsharp
function ReflectionOracleFromDeterministicStateOracle (oracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="description"></a>설명

단일 행렬 $O $로 표시 되는 결정적 상태 준비를 고려 하 여이 함수의 결과는 oracle $O $에서 준비한 상태 $ \ket{\psi} $에 대 한 반사를 적용 하는 oracle입니다. 즉, $ \ket{\psi} $ 상태를 $O \ket {0} = \ket{\psi} $입니다.

## <a name="input"></a>입력

### <a name="oracle--deterministicstateoracle"></a>oracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

$ \Ket{\psi} $ 상태의 복사본을 준비 하는 oracle입니다.



## <a name="output--reflectionoracle"></a>출력: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

$ \Ket{\psi} $ 상태에 대 한 정보를 반영 하는 oracle입니다.

## <a name="see-also"></a>참고 항목

- [Oracles. DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [Oracles. ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)