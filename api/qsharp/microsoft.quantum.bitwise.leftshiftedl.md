---
uid: Microsoft.Quantum.Bitwise.LeftShiftedL
title: LeftShiftedL 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedL
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 00d4f9151c620e044074930933ea2912b52534ed
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219671"
---
# <a name="leftshiftedl-function"></a>LeftShiftedL 함수

네임 스페이스: [Microsoft. 양자 비트](xref:Microsoft.Quantum.Bitwise)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 비트 수 만큼 왼쪽에 있는 숫자의 비트 표현을 이동 합니다.

```qsharp
function LeftShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a>입력

### <a name="value--bigint"></a>값: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

비트 표현이 왼쪽으로 이동 하는 숫자 (더 중요)입니다.


### <a name="amount--int"></a>amount: [Int](xref:microsoft.quantum.lang-ref.int)

`value`가 왼쪽으로 이동할 비트 수입니다.



## <a name="output--bigint"></a>출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

의 값으로 `value` , 왼쪽으로 비트를 이동 `amount` 합니다.

## <a name="remarks"></a>설명

다음은 동일 합니다.

```Q#
let c = a <<< b;
let c = LeftShiftedL(a, b);
```