---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactB
title: AllEqualityFactB 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactB
qsharp.summary: Asserts that two arrays of boolean values are equal.
ms.openlocfilehash: 725291e8b5d12683ad580d5938dadd561831e88e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853551"
---
# <a name="allequalityfactb-function"></a>AllEqualityFactB 함수

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


부울 값의 두 배열이 동일한 것을 어설션 합니다.

```qsharp
function AllEqualityFactB (actual : Bool[], expected : Bool[], message : String) : Unit
```


## <a name="input"></a>입력

### <a name="actual--bool"></a>actual: [Bool](xref:microsoft.quantum.lang-ref.bool)[]

관련 테스트 사례에 의해 생성 되는 배열입니다.


### <a name="expected--bool"></a>예상: [Bool](xref:microsoft.quantum.lang-ref.bool)[]

관련 테스트 사례에서 예상 되는 배열입니다.


### <a name="message--string"></a>메시지: [문자열](xref:microsoft.quantum.lang-ref.string)

배열이 같지 않으면 인쇄할 메시지입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

