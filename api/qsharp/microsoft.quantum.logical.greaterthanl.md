---
uid: Microsoft.Quantum.Logical.GreaterThanL
title: GreaterThanL 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanL
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 676defa7824e53578504c559c6d8f24b2ffc1a88
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711383"
---
# <a name="greaterthanl-function"></a>GreaterThanL 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)

패키지 [](https://nuget.org/packages/)


숫자가 다른 숫자 보다 큰 경우에만 true를 반환 합니다.

```qsharp
function GreaterThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a>입력

### <a name="a--bigint"></a>a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

비교할 첫 번째 값입니다.


### <a name="b--bigint"></a>b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

비교할 두 번째 값입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`true``a`가 보다 엄격 하 게 큰 경우에만 `b` 입니다.

## <a name="remarks"></a>설명

다음은 동일 합니다.

```Q#
let cond = a > b;
let cond = GreaterThanL(a, b);
```