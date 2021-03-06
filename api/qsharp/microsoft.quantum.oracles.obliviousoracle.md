---
uid: Microsoft.Quantum.Oracles.ObliviousOracle
title: ObliviousOracle 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracle
qsharp.summary: >-
  Represents an oracle for oblivious amplitude amplification.

  The inputs to the oracle $O$ are:

  - The ancilla register $a$ that $O$ acts on. - The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.
ms.openlocfilehash: 793e72af56e288f9b437302f9958665e92e5e763
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842557"
---
# <a name="obliviousoracle-user-defined-type"></a>ObliviousOracle 사용자 정의 형식

네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


명확한 진폭 증폭의 oracle을 나타냅니다.

Oracle $O $에 대 한 입력은 다음과 같습니다.

- $O $가 작동 하는 ancilla 레지스터 $a $입니다.
- 원하는 단일 $U $이 적용 되 고, $ \ket{t} a $ 상태에 있는 레지스터 $a $에서 게시 된 시스템 등록 $s $입니다 \_ .

```qsharp

newtype ObliviousOracle = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a>설명

$ $ O\ket {s} \_ a\ket {\ psi} \_ s = \Lambda\ket{t} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{t ^ \perp} a\cdots $ $에 의해 정의 된이 oracle은 \_ ancilla state $ \ket{s} \_ a $U $에 적용 되어 모든 시스템 상태 $ \ket{\psi} \_ s $ with 진폭 $ \lambda $를 사용 하 여 $ \ket{t} \_ a $로 플래그 지정 된 모든 시스템 상태 $
첫 번째 매개 변수는 $ \ket{s} a $의 기본 비트 레지스터입니다 \_ . 두 번째 매개 변수는 $ \ket{\psi} s $의 고 비트 레지스터입니다 \_ .