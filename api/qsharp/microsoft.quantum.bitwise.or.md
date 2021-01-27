---
uid: Microsoft.Quantum.Bitwise.Or
title: Or 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: Or
qsharp.summary: Returns the bitwise OR of two integers. This performs the same computation as the built-in `|||` operator.
ms.openlocfilehash: 811e7cf64424e8302c5745c4c71d76de50ab8c08
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845275"
---
# <a name="or-function"></a>Or 함수

네임 스페이스: [Microsoft. 양자 비트](xref:Microsoft.Quantum.Bitwise)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


두 정수의 비트 OR을 반환 합니다.
이는 기본 제공 연산자와 동일한 계산을 수행 합니다 `|||` .

```qsharp
function Or (a : Int, b : Int) : Int
```


## <a name="input"></a>입력

### <a name="a--int"></a>a: [Int](xref:microsoft.quantum.lang-ref.int)




### <a name="b--int"></a>b: [Int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)



## <a name="example"></a>예

```qsharp
let a = 248;      //                 11111000₂
let b = 63;       //                 00111111₂
let x = Or(a, b); // x : Int = 255 = 11111111₂.
```

## <a name="remarks"></a>설명

[C # | 참조 추가 정보를 확인](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/or-operator) 합니다.