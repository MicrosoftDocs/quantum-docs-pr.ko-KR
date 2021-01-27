---
uid: Microsoft.Quantum.ErrorCorrection.EncodeOp
title: EncodeOp 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeOp
qsharp.summary: >-
  Represents an operation which encodes a physical register into a logical register, using the provided scratch qubits.

  The first argument is taken to be the physical register that will be encoded, while the second argument is taken to be the scratch register that will be used.
ms.openlocfilehash: c9959f1afbd44df974c06b79f73eccd090b17985
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826187"
---
# <a name="encodeop-user-defined-type"></a>EncodeOp 사용자 정의 형식

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


제공 된 스크래치 인스턴스를 사용 하 여 실제 레지스터를 논리적 레지스터로 인코딩하는 작업을 나타냅니다.

첫 번째 인수는 인코딩할 물리적 레지스터가 되 고 두 번째 인수는 사용 되는 스크래치 레지스터가 됩니다.

```qsharp

newtype EncodeOp = (((Qubit[], Qubit[]) => Microsoft.Quantum.ErrorCorrection.LogicalRegister));
```

