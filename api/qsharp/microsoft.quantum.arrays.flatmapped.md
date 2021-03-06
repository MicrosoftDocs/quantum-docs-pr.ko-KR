---
uid: Microsoft.Quantum.Arrays.FlatMapped
title: FlatMapped 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: FlatMapped
qsharp.summary: Given an array and a function that maps an array element to some output array, returns the concatenated output arrays for each array element.
ms.openlocfilehash: bee7002c5a1e80cee7907ff9cb4ebaaedf8e9923
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848634"
---
# <a name="flatmapped-function"></a>FlatMapped 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열 요소를 일부 출력 배열에 매핑하는 배열과 함수가 지정 된 경우 각 배열 요소에 대해 연결 된 출력 배열을 반환 합니다.

```qsharp
function FlatMapped<'TInput, 'TOutput> (mapper : ('TInput -> 'TOutput[]), array : 'TInput[]) : 'TOutput[]
```


## <a name="input"></a>입력

### <a name="mapper--tinput---toutput"></a>매퍼: ' TInput-> ' TOutput []

배열 요소를 매핑하는 데 사용 되는에서로의 함수입니다 `'TInput` `'TOutput[]` .


### <a name="array--tinput"></a>배열: ' TInput []

요소의 배열입니다.



## <a name="output--toutput"></a>출력: ' TOutput []

`'TOutput[]`매핑 함수에 의해 생성 된 모든 배열을 연결 하는 배열입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="tinput"></a>'TInput

`array`요소의 형식입니다.
### <a name="toutput"></a>' TOutput

`mapper`함수는이 형식의 배열을 반환 합니다.

## <a name="example"></a>예제

```qsharp
let Numbers = SequenceI(1, _); // generates numbers starting from 1
let values = FlatMapped(Numbers, [1, 2, 3]);
// values = [1, 1, 2, 1, 2, 3]
```