---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: R 코딩 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: ef9be0f0628c8ba8c5f131cc558bdcda6bb6ea55
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725478"
---
# <a name="rmencoding-function"></a>R 코딩 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지 [](https://nuget.org/packages/)


{-1,1} 부울 값 코딩

```qsharp
function RMEncoding (b : Bool) : Int
```


## <a name="input"></a>입력

### <a name="b--bool"></a>b: [Bool](xref:microsoft.quantum.lang-ref.bool)

부울 값



## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

가 false 이면 1이 고, `b` 그렇지 않으면-1입니다.