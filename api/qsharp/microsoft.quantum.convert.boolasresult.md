---
uid: Microsoft.Quantum.Convert.BoolAsResult
title: BoolAsResult 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolAsResult
qsharp.summary: Converts a `Bool` type to a `Result` type, where `true` is mapped to `One` and `false` is mapped to `Zero`.
ms.openlocfilehash: eea6c062afdbb3172e63261e52a82e2576c14011
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713588"
---
# <a name="boolasresult-function"></a>BoolAsResult 함수

네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)

패키지 [](https://nuget.org/packages/)


`Bool`형식을 형식으로 변환 `Result` `true` 합니다. 여기서은로 매핑되고는 `One` `false` 에 매핑됩니다 `Zero` .

```qsharp
function BoolAsResult (input : Bool) : Result
```


## <a name="input"></a>입력

### <a name="input--bool"></a>input: [Bool](xref:microsoft.quantum.lang-ref.bool)

`Bool` 변환 될입니다.



## <a name="output--__invalidresult__"></a>출력: __잘못 <Result> 됨__

`input`를 나타내는 `Result`입니다.