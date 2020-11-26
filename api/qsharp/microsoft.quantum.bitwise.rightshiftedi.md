---
uid: Microsoft.Quantum.Bitwise.RightShiftedI
title: RightShiftedI 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedI
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: b20a4a8c281a470af9a4828f8a5ca905a7918723
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209777"
---
# <a name="rightshiftedi-function"></a>RightShiftedI 함수

네임 스페이스: [Microsoft. 양자 비트](xref:Microsoft.Quantum.Bitwise)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


숫자의 비트 표현을 지정 된 비트 수 만큼 오른쪽으로 이동 합니다.

```qsharp
function RightShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a>입력

### <a name="value--int"></a>값: [Int](xref:microsoft.quantum.lang-ref.int)

비트 표현이 오른쪽으로 이동 하는 숫자 (낮음)입니다.


### <a name="amount--int"></a>amount: [Int](xref:microsoft.quantum.lang-ref.int)

를 `value` 오른쪽으로 이동할 비트 수입니다.



## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

`value`비트 단위로 오른쪽으로 이동 하는의 값입니다 `amount` .

## <a name="remarks"></a>설명

다음은 동일 합니다.

```Q#
let c = a >>> b;
let c = RightShiftedI(a, b);
```