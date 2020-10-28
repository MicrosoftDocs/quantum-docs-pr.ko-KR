---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: FormattedFailure 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: 0d7fb01ddf23cd6d79f722c8f6b691afa74a8885
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712678"
---
# <a name="formattedfailure-function"></a>FormattedFailure 함수

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지 [](https://nuget.org/packages/)


의미 있는 오류 메시지와 함께 실패 하는 데 사용 되는 내부 함수입니다.

```qsharp
function FormattedFailure<'T> (actual : 'T, expected : 'T, message : String) : Unit
```


## <a name="input"></a>입력

### <a name="actual--t"></a>실제: ' t




### <a name="expected--t"></a>예상: ' '




### <a name="message--string"></a>메시지: [문자열](xref:microsoft.quantum.lang-ref.string)





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="remarks"></a>설명

이 함수는 전달 형식이 지정 된 모순를 허용 하기 위해 시뮬레이션 런타임에 의해 에뮬레이트 됩니다.