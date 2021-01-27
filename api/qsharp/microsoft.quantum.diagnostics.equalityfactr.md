---
uid: Microsoft.Quantum.Diagnostics.EqualityFactR
title: EqualityFactR 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactR
qsharp.summary: Asserts that a classical Result variable has the expected value.
ms.openlocfilehash: 86d2ddff79f0bca7badd95a2fe2156c558fa7f86
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853325"
---
# <a name="equalityfactr-function"></a>EqualityFactR 함수

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


기존 결과 변수가 예상 값을 가지는 것을 어설션 합니다.

```qsharp
function EqualityFactR (actual : Result, expected : Result, message : String) : Unit
```


## <a name="input"></a>입력

### <a name="actual--__invalidresult__"></a>실제: __유효 <Result> 하지 않음__

검사할 변수입니다.


### <a name="expected--__invalidresult__"></a>예상: __잘못 <Result> 됨__

예상 값입니다.


### <a name="message--string"></a>메시지: [문자열](xref:microsoft.quantum.lang-ref.string)

어설션이 트리거될 때 사용할 오류 메시지 문자열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

