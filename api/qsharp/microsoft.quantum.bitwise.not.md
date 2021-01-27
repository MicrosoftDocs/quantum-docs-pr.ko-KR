---
uid: Microsoft.Quantum.Bitwise.Not
title: Not 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: Not
qsharp.summary: Returns the bitwise NOT of an integer. This performs the same computation as the built-in `~~~` operator.
ms.openlocfilehash: 9c7642770c4f1db4878ccc1aba288fb9254e017e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842105"
---
# <a name="not-function"></a>Not 함수

네임 스페이스: [Microsoft. 양자 비트](xref:Microsoft.Quantum.Bitwise)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


정수의 비트 NOT을 반환 합니다.
이는 기본 제공 연산자와 동일한 계산을 수행 합니다 `~~~` .

```qsharp
function Not (a : Int) : Int
```


## <a name="input"></a>입력

### <a name="a--int"></a>a: [Int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)



## <a name="example"></a>예

```qsharp
let a = 248;
let x = Not(a); // x : Int = -249, due to two's complement representation.
```

## <a name="remarks"></a>설명

자세한 내용은 [c # ~ 연산자](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/bitwise-complement-operator) 를 참조 하세요.