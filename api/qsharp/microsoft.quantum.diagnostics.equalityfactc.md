---
uid: Microsoft.Quantum.Diagnostics.EqualityFactC
title: EqualityFactC 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactC
qsharp.summary: Asserts that a complex number has the expected value.
ms.openlocfilehash: 4c7256f9a8c84b4e105b1cbff6b18d6dd99cc441
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712783"
---
# <a name="equalityfactc-function"></a>EqualityFactC 함수

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지 [](https://nuget.org/packages/)


복소수에 필요한 값이 있음을 어설션 합니다.

```qsharp
function EqualityFactC (actual : Microsoft.Quantum.Math.Complex, expected : Microsoft.Quantum.Math.Complex, message : String) : Unit
```


## <a name="input"></a>입력

### <a name="actual--complex"></a>실제: [복합](xref:Microsoft.Quantum.Math.Complex)

확인할 값입니다.


### <a name="expected--complex"></a>예상: [복합](xref:Microsoft.Quantum.Math.Complex)

예상 값입니다.


### <a name="message--string"></a>메시지: [문자열](xref:microsoft.quantum.lang-ref.string)

어설션이 트리거될 때 사용할 오류 메시지 문자열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

