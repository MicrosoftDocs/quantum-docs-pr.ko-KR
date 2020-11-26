---
uid: Microsoft.Quantum.Logical.NotEqualR
title: NotEqualR 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 4ac6cf4b220fa42c8eb946d6fbcad4cdb191afcd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197197"
---
# <a name="notequalr-function"></a>NotEqualR 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


두 입력이 같지 않은 경우에만 true를 반환 합니다.

```qsharp
function NotEqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a>입력

### <a name="a--__invalidresult__"></a>a: __잘못 <Result> 된__

비교할 첫 번째 값입니다.


### <a name="b--__invalidresult__"></a>b: __잘못 <Result> 됨__

비교할 두 번째 값입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`true``a`가와 같지 않은 경우에만입니다 `b` .

## <a name="remarks"></a>설명

다음은 동일 합니다.

```Q#
let cond = a != b;
let cond = NotEqualR(a, b);
```