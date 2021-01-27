---
uid: Microsoft.Quantum.Simulation.BlockEncoding
title: BlockEncoding 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncoding
qsharp.summary: >-
  Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.

  That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.
ms.openlocfilehash: 70cd18f04cbd449f4818ba3b40580303137f84db
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857624"
---
# <a name="blockencoding-user-defined-type"></a>BlockEncoding 사용자 정의 형식

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


관심이 있는 임의의 연산자가 왼쪽 위 블록에서 인코딩된 단일를 나타냅니다.

즉,는 `BlockEncoding` 시스템 레지스터에 대해 수행 되는 임의의 연산자 $H $ `s` \ket _a $에 해당 하는 왼쪽 위 블록에 인코딩 되는 임의의 연산자를 갖는 단일 $U $ {0} 입니다. 즉, 다음과 같습니다.

$ $ \begin{align} (\bra {0} _a \otimes I_s) U (\ket {0} _a \otimes I_s) = H \end{align} $ $.

```qsharp

newtype BlockEncoding = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

