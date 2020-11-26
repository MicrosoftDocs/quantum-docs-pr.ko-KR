---
uid: Microsoft.Quantum.Convert.ResultAsBool
title: ResultAsBool 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: ResultAsBool
qsharp.summary: Converts a `Result` type to a `Bool` type, where `One` is mapped to `true` and `Zero` is mapped to `false`.
ms.openlocfilehash: a170acf635e4e2b2150ffc208fabc9782ff837b0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224176"
---
# <a name="resultasbool-function"></a>ResultAsBool 함수

네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


`Result`형식을 형식으로 변환 `Bool` `One` 합니다. 여기서은로 매핑되고는 `true` `Zero` 에 매핑됩니다 `false` .

```qsharp
function ResultAsBool (input : Result) : Bool
```


## <a name="input"></a>입력

### <a name="input--__invalidresult__"></a>입력: __잘못 <Result> 됨__

`Result` 변환 될입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`input`를 나타내는 `Bool`입니다.