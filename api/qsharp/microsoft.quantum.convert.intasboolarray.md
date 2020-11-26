---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: IntAsBoolArray 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a positive integer, using the little-endian representation for the returned array.
ms.openlocfilehash: f89cb3d7ca29d7deaaf49573b2670534166caded
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224346"
---
# <a name="intasboolarray-function"></a>IntAsBoolArray 함수

네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


반환 된 배열에 대 한 작은 endian 표현을 사용 하 여 양의 정수의 이진 표현을 생성 합니다.

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a>입력

### <a name="number--int"></a>number: [Int](xref:microsoft.quantum.lang-ref.int)

부울 값의 배열로 변환할 양의 정수입니다.


### <a name="bits--int"></a>비트: [Int](xref:microsoft.quantum.lang-ref.int)

의 이진 표현에서 비트 수입니다 `number` .



## <a name="output--bool"></a>Output: [Bool](xref:microsoft.quantum.lang-ref.bool)[]

를 나타내는 부울 값의 배열입니다 `number` .

## <a name="remarks"></a>설명

입력은 `bits` 0에서 63 사이 여야 합니다.
입력은 `number` 0에서 $2 ^ {\texttt{bits}}-$1 사이 여야 합니다.