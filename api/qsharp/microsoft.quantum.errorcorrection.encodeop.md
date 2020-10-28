---
uid: Microsoft.Quantum.ErrorCorrection.EncodeOp
title: EncodeOp 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeOp
qsharp.summary: >-
  Represents an operation which encodes a physical register into a logical register, using the provided scratch qubits.

  The first argument is taken to be the physical register that will be encoded, while the second argument is taken to be the scratch register that will be used.
ms.openlocfilehash: da947cdc25cb0edd3a4144022bbfc6ecb84c647f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712349"
---
# <a name="encodeop-user-defined-type"></a>EncodeOp 사용자 정의 형식

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지 [](https://nuget.org/packages/)


제공 된 스크래치 인스턴스를 사용 하 여 실제 레지스터를 논리적 레지스터로 인코딩하는 작업을 나타냅니다.

첫 번째 인수는 인코딩할 물리적 레지스터가 되 고 두 번째 인수는 사용 되는 스크래치 레지스터가 됩니다.

```qsharp

newtype EncodeOp = (((Qubit[], Qubit[]) => Microsoft.Quantum.ErrorCorrection.LogicalRegister));
```

