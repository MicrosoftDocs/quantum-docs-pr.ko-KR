---
uid: Microsoft.Quantum.Diagnostics.Fact
title: Fact 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Fact
qsharp.summary: Declares that a classical condition is true.
ms.openlocfilehash: 8e86000f04c01040d420c2f682fc1b4ccf35cf39
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853314"
---
# <a name="fact-function"></a>Fact 함수

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


는 기존 조건이 true 임을 선언 합니다.

```qsharp
function Fact (actual : Bool, message : String) : Unit
```


## <a name="input"></a>입력

### <a name="actual--bool"></a>actual: [Bool](xref:microsoft.quantum.lang-ref.bool)

선언 될 조건입니다.


### <a name="message--string"></a>메시지: [문자열](xref:microsoft.quantum.lang-ref.string)

클래식 조건이 false 인 경우 인쇄 될 실패 메시지 문자열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>예

다음 Q # 코드 조각이 실패 합니다.

```qsharp
Fact(false, "Expected true.");
```

## <a name="see-also"></a>참고 항목

- [Microsoft 양자 진단.](xref:Microsoft.Quantum.Diagnostics.Contradiction)