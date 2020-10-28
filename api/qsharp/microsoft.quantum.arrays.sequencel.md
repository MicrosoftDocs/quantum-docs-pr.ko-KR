---
uid: Microsoft.Quantum.Arrays.SequenceL
title: SequenceL 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5ce63575e703341fce42c0be393765c342bbd89
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718880"
---
# <a name="sequencel-function"></a>SequenceL 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지 [](https://nuget.org/packages/)


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