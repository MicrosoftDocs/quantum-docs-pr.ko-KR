---
uid: Microsoft.Quantum.Convert.BoolAsResult
title: BoolAsResult 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolAsResult
qsharp.summary: Converts a `Bool` type to a `Result` type, where `true` is mapped to `One` and `false` is mapped to `Zero`.
ms.openlocfilehash: 0190529dd804922a69499fbf1c2c4c916c4b720a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214248"
---
# <a name="boolasresult-function"></a>BoolAsResult 함수

네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


`Bool`형식을 형식으로 변환 `Result` `true` 합니다. 여기서은로 매핑되고는 `One` `false` 에 매핑됩니다 `Zero` .

```qsharp
function BoolAsResult (input : Bool) : Result
```


## <a name="input"></a>입력

### <a name="input--bool"></a>input: [Bool](xref:microsoft.quantum.lang-ref.bool)

`Bool` 변환 될입니다.



## <a name="output--__invalidresult__"></a>출력: __잘못 <Result> 됨__

`input`를 나타내는 `Result`입니다.