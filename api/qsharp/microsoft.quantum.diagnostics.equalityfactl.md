---
uid: Microsoft.Quantum.Diagnostics.EqualityFactL
title: EqualityFactL 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactL
qsharp.summary: Asserts that a classical BigInt variable has the expected value.
ms.openlocfilehash: 5e590af581be4e41df9d2081260409c454e3be4b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712755"
---
# <a name="equalityfactl-function"></a>EqualityFactL 함수

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지 [](https://nuget.org/packages/)


기존 BigInt 변수에 필요한 값이 있음을 어설션 합니다.

```qsharp
function EqualityFactL (actual : BigInt, expected : BigInt, message : String) : Unit
```


## <a name="input"></a>입력

### <a name="actual--bigint"></a>actual: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

확인할 숫자입니다.


### <a name="expected--bigint"></a>예상: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

예상 값입니다.


### <a name="message--string"></a>메시지: [문자열](xref:microsoft.quantum.lang-ref.string)

어설션이 트리거될 때 사용할 오류 메시지 문자열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

