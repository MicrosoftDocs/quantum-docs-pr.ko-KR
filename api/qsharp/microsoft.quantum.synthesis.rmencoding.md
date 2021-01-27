---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: R 코딩 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: f3c54d2e40511dacb21618b4eaf1eef9f4903f9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855337"
---
# <a name="rmencoding-function"></a>R 코딩 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


{-1,1} 부울 값 코딩

```qsharp
function RMEncoding (b : Bool) : Int
```


## <a name="input"></a>입력

### <a name="b--bool"></a>b: [Bool](xref:microsoft.quantum.lang-ref.bool)

부울 값



## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

가 false 이면 1이 고, `b` 그렇지 않으면-1입니다.