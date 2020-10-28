---
uid: Microsoft.Quantum.Logical.LessThanOrEqualD
title: LessThanOrEqualD 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualD
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 7b0e9da379bd67eb78a80e7a535a15dcb8ba85c7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709948"
---
# <a name="lessthanorequald-function"></a>LessThanOrEqualD 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)

패키지 [](https://nuget.org/packages/)


숫자가 다른 숫자 보다 작거나 같은 경우에만 true를 반환 합니다.

```qsharp
function LessThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a>입력

### <a name="a--double"></a>a: [Double](xref:microsoft.quantum.lang-ref.double)

비교할 첫 번째 값입니다.


### <a name="b--double"></a>b: [Double](xref:microsoft.quantum.lang-ref.double)

비교할 두 번째 값입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`true``a`가 보다 작거나 같은 경우에만입니다 `b` .

## <a name="remarks"></a>설명

다음은 동일 합니다.

```Q#
let cond = a <= b;
let cond = LessThanOrEqualD(a, b);
```