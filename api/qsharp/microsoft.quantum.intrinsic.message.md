---
uid: Microsoft.Quantum.Intrinsic.Message
title: Message 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Message
qsharp.summary: Logs a message.
ms.openlocfilehash: 652e33de69ffb725f117db3beeffa66558776f49
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849371"
---
# <a name="message-function"></a>Message 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


메시지를 기록 합니다.

```qsharp
function Message (msg : String) : Unit
```


## <a name="input"></a>입력

### <a name="msg--string"></a>msg: [문자열](xref:microsoft.quantum.lang-ref.string)

보고할 메시지입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

이 함수의 특정 동작은 시뮬레이터에 종속 되지만 대부분의 경우 지정 된 메시지가 콘솔에 기록 됩니다.