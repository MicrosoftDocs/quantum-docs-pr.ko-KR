---
uid: Microsoft.Quantum.Logical.GreaterThanI
title: GreaterThanI 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanI
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 06cae04150f9f0164b06a4e3d4bb78242b41dc0b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197996"
---
# <a name="greaterthani-function"></a>GreaterThanI 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


숫자가 다른 숫자 보다 큰 경우에만 true를 반환 합니다.

```qsharp
function GreaterThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a>입력

### <a name="a--int"></a>a: [Int](xref:microsoft.quantum.lang-ref.int)

비교할 첫 번째 값입니다.


### <a name="b--int"></a>b: [Int](xref:microsoft.quantum.lang-ref.int)

비교할 두 번째 값입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`true``a`가 보다 엄격 하 게 큰 경우에만 `b` 입니다.

## <a name="remarks"></a>설명

다음은 동일 합니다.

```Q#
let cond = a > b;
let cond = GreaterThanI(a, b);
```