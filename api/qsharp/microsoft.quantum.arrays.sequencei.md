---
uid: Microsoft.Quantum.Arrays.SequenceI
title: SequenceI 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 3cf09e48cce1aeb1aac837465ee3a5e06adf5169
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851001"
---
# <a name="sequencei-function"></a>SequenceI 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 간격의 정수 배열을 가져옵니다.

```qsharp
function SequenceI (from : Int, to : Int) : Int[]
```


## <a name="input"></a>입력

### <a name="from--int"></a>시작: [Int](xref:microsoft.quantum.lang-ref.int)

간격의 포함 시작 인덱스입니다.


### <a name="to--int"></a>대상: [Int](xref:microsoft.quantum.lang-ref.int)

보다 작은 간격의 포함 끝 인덱스입니다 `from` .



## <a name="output--int"></a>Output: [Int](xref:microsoft.quantum.lang-ref.int)[]

숫자 시퀀스 (, ...,)를 포함 하는 배열입니다. `from` `from + 1` `to`

## <a name="example"></a>예제

```qsharp
let arr1 = SequenceI(0, 3); // [0, 1, 2, 3]
let arr2 = SequenceI(23, 29); // [23, 24, 25, 26, 27, 28, 29]
let arr3 = SequenceI(-5, -2); // [-5, -4, -3, -2]

let numbers = SequenceI(0, _); // function to create sequence from 0 to `to`
let naturals = SequenceI(1, _); // function to create sequence from 1 to `to`
```