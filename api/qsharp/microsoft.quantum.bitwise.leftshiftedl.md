---
uid: Microsoft.Quantum.Bitwise.LeftShiftedL
title: LeftShiftedL 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedL
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 014653011574d0fabb4b9aa04cedf58b87ddf798
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842148"
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

```qsharp
let c = a <<< b;
let c = LeftShiftedL(a, b);
```