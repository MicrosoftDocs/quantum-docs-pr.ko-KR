---
uid: Microsoft.Quantum.Canon.CCNOTop
title: CCNOTop 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CCNOTop
qsharp.summary: The signature type of CCNOT gate.
ms.openlocfilehash: 026a368b753a1b3e74b8e4352cf65835546df4bc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716598"
---
# <a name="ccnotop-user-defined-type"></a>CCNOTop 사용자 정의 형식

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


CCNOT gate의 서명 유형입니다.

```qsharp

newtype CCNOTop = (Apply : ((Qubit, Qubit, Qubit) => Unit is Adj));
```



## <a name="named-items"></a>명명 된 항목

### <a name="apply--qubitqubitqubit--unit-adj"></a>Apply[: (Adj 비트](xref:microsoft.quantum.lang-ref.qubit),[고 비트, 고](xref:microsoft.quantum.lang-ref.qubit)[비트](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)

