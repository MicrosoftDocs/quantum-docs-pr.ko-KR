---
uid: Microsoft.Quantum.Convert.ResultAsBool
title: ResultAsBool 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: ResultAsBool
qsharp.summary: Converts a `Result` type to a `Bool` type, where `One` is mapped to `true` and `Zero` is mapped to `false`.
ms.openlocfilehash: 34fca15faf79f706b398e3fdfc537ea91b28da86
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713343"
---
# <a name="resultasbool-function"></a>ResultAsBool 함수

네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)

패키지 [](https://nuget.org/packages/)


`Result`형식을 형식으로 변환 `Bool` `One` 합니다. 여기서은로 매핑되고는 `true` `Zero` 에 매핑됩니다 `false` .

```qsharp
function ResultAsBool (input : Result) : Bool
```


## <a name="input"></a>입력

### <a name="input--__invalidresult__"></a>입력: __잘못 <Result> 됨__

`Result` 변환 될입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`input`를 나타내는 `Bool`입니다.