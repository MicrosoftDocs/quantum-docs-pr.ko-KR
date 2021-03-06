---
uid: Microsoft.Quantum.ErrorCorrection.LogicalRegister
title: LogicalRegister 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: LogicalRegister
qsharp.summary: Type for register of physical qubits `Qubit[]` that encode the logical qubits.
ms.openlocfilehash: 96fb567814e69060707a8080749e23883ae2a860
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98825872"
---
# <a name="logicalregister-user-defined-type"></a>LogicalRegister 사용자 정의 형식

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


논리적 및 비트를 인코딩하는 실제 실제 비트의 레지스터를 입력 `Qubit[]` 합니다.

```qsharp

newtype LogicalRegister = (Qubit[]);
```

