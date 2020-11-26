---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: R 코딩 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: a506ccb637b331a392ea75383c8bd605114af059
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202943"
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