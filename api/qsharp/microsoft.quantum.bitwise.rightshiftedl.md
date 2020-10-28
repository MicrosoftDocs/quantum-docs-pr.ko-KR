---
uid: Microsoft.Quantum.Bitwise.RightShiftedL
title: RightShiftedL 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedL
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 2929ba58b636847257391930e1019769fd2c2580
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718573"
---
# <a name="rightshiftedl-function"></a>RightShiftedL 함수

네임 스페이스: [Microsoft. 양자 비트](xref:Microsoft.Quantum.Bitwise)

패키지 [](https://nuget.org/packages/)


숫자의 비트 표현을 지정 된 비트 수 만큼 오른쪽으로 이동 합니다.

```qsharp
function RightShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a>입력

### <a name="value--bigint"></a>값: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

비트 표현이 오른쪽으로 이동 하는 숫자 (낮음)입니다.


### <a name="amount--int"></a>amount: [Int](xref:microsoft.quantum.lang-ref.int)

를 `value` 오른쪽으로 이동할 비트 수입니다.



## <a name="output--bigint"></a>출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

`value`비트 단위로 오른쪽으로 이동 하는의 값입니다 `amount` .

## <a name="remarks"></a>설명

다음은 동일 합니다.

```Q#
let c = a >>> b;
let c = RightShiftedL(a, b);
```