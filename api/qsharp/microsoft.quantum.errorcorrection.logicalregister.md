---
uid: Microsoft.Quantum.ErrorCorrection.LogicalRegister
title: LogicalRegister 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: LogicalRegister
qsharp.summary: Type for register of physical qubits `Qubit[]` that encode the logical qubits.
ms.openlocfilehash: 3847d80c66200925758edafdc0efbd04dc2f82df
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200716"
---
# <a name="logicalregister-user-defined-type"></a>LogicalRegister 사용자 정의 형식

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


논리적 및 비트를 인코딩하는 실제 실제 비트의 레지스터를 입력 `Qubit[]` 합니다.

```qsharp

newtype LogicalRegister = (Qubit[]);
```

