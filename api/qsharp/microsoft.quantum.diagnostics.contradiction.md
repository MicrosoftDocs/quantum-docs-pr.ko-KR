---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: 모순 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: a5f3f26c5ada2eea9206699a2cc77575a9b5eebd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712867"
---
# <a name="contradiction-function"></a>모순 함수

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지 [](https://nuget.org/packages/)


는 기존 조건이 false 임을 선언 합니다.

```qsharp
function Contradiction (actual : Bool, message : String) : Unit
```


## <a name="input"></a>입력

### <a name="actual--bool"></a>actual: [Bool](xref:microsoft.quantum.lang-ref.bool)

선언 될 조건입니다.


### <a name="message--string"></a>메시지: [문자열](xref:microsoft.quantum.lang-ref.string)

고전 조건이 true 인 경우 인쇄 될 실패 메시지 문자열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [Microsoft 양자 진단 팩트](xref:Microsoft.Quantum.Diagnostics.Fact)