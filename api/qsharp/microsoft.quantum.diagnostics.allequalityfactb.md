---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactB
title: AllEqualityFactB 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactB
qsharp.summary: Asserts that two arrays of boolean values are equal.
ms.openlocfilehash: 100aacccbfd5b45ac9f859cd89424b0ed4007f72
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713077"
---
# <a name="allequalityfactb-function"></a>AllEqualityFactB 함수

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지 [](https://nuget.org/packages/)


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

