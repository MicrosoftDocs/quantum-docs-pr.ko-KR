---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracle
title: DeterministicStateOracle 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracle
qsharp.summary: >-
  Represents an oracle for deterministic state preparation.

  The input to the oracle $O$ is:

  - The register that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 10ae9e52f298cdfb92dd6a9e5cf85960bece6800
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842586"
---
# <a name="deterministicstateoracle-user-defined-type"></a>DeterministicStateOracle 사용자 정의 형식

네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


결정적 상태 준비를 위한 oracle을 나타냅니다.

Oracle $O $에 대 한 입력은 다음과 같습니다.

- 원하는 퀀텀 상태 $ \ket{\psi} s $를 저장할 레지스터입니다 \_ .

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a>설명

$O \ket = \ket{\psi} $에서 정의한이 oracle {0} 은 {0} 상태 $ \ket{\psi} $를 만들기 위해 계산 기준 상태 $ \ket $에 대해 작동 합니다.
첫 번째 매개 변수는 $ \ket{\psi} $의 기본 비트 레지스터입니다.