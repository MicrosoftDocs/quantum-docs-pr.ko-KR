---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: RangeAsIntArray 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: f756e42aef7dc600e1fc6943a02513ac791f2320
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214010"
---
# <a name="rangeasintarray-function"></a>RangeAsIntArray 함수

네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


`arr`Start .로 열거 된 정수 배열을 만듭니다. 단계. 종단.

```qsharp
function RangeAsIntArray (range : Range) : Int[]
```


## <a name="input"></a>입력

### <a name="range--range"></a>범위: [범위](xref:microsoft.quantum.lang-ref.range)

`Range`배열로 변환할 값의입니다 `start..step..end` .



## <a name="output--int"></a>Output: [Int](xref:microsoft.quantum.lang-ref.int)[]

에 의해 반복 되는 값에 해당 하는 정수의 새 배열입니다 `range` .