---
uid: Microsoft.Quantum.Diagnostics.EqualityFactI
title: EqualityFactI 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactI
qsharp.summary: Asserts that a classical Int variable has the expected value.
ms.openlocfilehash: c41cb5548e8dfebb4d1c1a1c052306878c85e821
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853344"
---
# <a name="equalityfacti-function"></a>EqualityFactI 함수

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


기존 Int 변수에 예상 값이 있음을 어설션 합니다.

```qsharp
function EqualityFactI (actual : Int, expected : Int, message : String) : Unit
```


## <a name="input"></a>입력

### <a name="actual--int"></a>실제: [Int](xref:microsoft.quantum.lang-ref.int)

확인할 숫자입니다.


### <a name="expected--int"></a>예상: [Int](xref:microsoft.quantum.lang-ref.int)

예상 값입니다.


### <a name="message--string"></a>메시지: [문자열](xref:microsoft.quantum.lang-ref.string)

어설션이 트리거될 때 사용할 오류 메시지 문자열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

