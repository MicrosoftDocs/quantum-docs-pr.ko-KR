---
uid: Microsoft.Quantum.Arrays.SequenceI
title: SequenceI 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5dc4377c696e14b505c63701c2f5ca0dadca672
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718897"
---
# <a name="sequencei-function"></a>SequenceI 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지 [](https://nuget.org/packages/)


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