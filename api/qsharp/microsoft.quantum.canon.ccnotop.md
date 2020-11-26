---
uid: Microsoft.Quantum.Canon.CCNOTop
title: CCNOTop 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CCNOTop
qsharp.summary: The signature type of CCNOT gate.
ms.openlocfilehash: 533ea87e137aabf6f75e6096dc710ca15c984f25
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207482"
---
# <a name="ccnotop-user-defined-type"></a>CCNOTop 사용자 정의 형식

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


CCNOT gate의 서명 유형입니다.

```qsharp

newtype CCNOTop = (Apply : ((Qubit, Qubit, Qubit) => Unit is Adj));
```



## <a name="named-items"></a>명명 된 항목

### <a name="apply--qubitqubitqubit--unit--is-adj"></a>Apply[: (Adj bit,](xref:microsoft.quantum.lang-ref.qubit) [bit](xref:microsoft.quantum.lang-ref.qubit), [bit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is

