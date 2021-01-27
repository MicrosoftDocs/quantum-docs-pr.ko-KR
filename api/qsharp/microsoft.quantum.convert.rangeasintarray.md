---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: RangeAsIntArray 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: 8c6b83d78e3b22ea1a17a48de66592950bf905a3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850095"
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

## <a name="example"></a>예제

```qsharp
// The following returns [1,3,5,7];
let array = RangeAsIntArray(1..2..8);
```