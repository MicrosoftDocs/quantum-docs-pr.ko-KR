---
uid: Microsoft.Quantum.Diagnostics.EqualityFactR
title: EqualityFactR 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactR
qsharp.summary: Asserts that a classical Result variable has the expected value.
ms.openlocfilehash: 2b293dc581ed58f7e3864a952fb3ecafa68e759c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712741"
---
# <a name="equalityfactr-function"></a>EqualityFactR 함수

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지 [](https://nuget.org/packages/)


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

