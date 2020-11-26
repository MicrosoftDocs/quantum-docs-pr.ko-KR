---
uid: Microsoft.Quantum.Arrays.SequenceL
title: SequenceL 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 3e5c7f64825f09d82792d3e46fe3f53f5814510b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220266"
---
# <a name="sequencel-function"></a>SequenceL 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 간격의 정수 배열을 가져옵니다.

```qsharp
function SequenceL (from : BigInt, to : BigInt) : BigInt[]
```


## <a name="input"></a>입력

### <a name="from--bigint"></a>시작: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

간격의 포함 시작 인덱스입니다.


### <a name="to--bigint"></a>대상: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

보다 작은 간격의 포함 끝 인덱스입니다 `from` .



## <a name="output--bigint"></a>출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]

숫자 시퀀스 (, ...,)를 포함 하는 배열입니다. `from` `from + 1` `to`

## <a name="remarks"></a>설명

과 사이의 차이 `from` 는 `to` 값에 맞아야 합니다 `Int` .